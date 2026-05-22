# What is a Multiprocessor System?

A parallel system where two or more processors work together to run more than one program at the same time.

---
# Why Multiprocessor System?

- DMA controller can improve performance by doing I/O while CPU keeps working  
- 8086 uses only 50-80% of available bus time, so some time is wasted  
- But DMA capability is limited  

Other solutions (complex components, multicore) also have problems:

## Complex Components
- Limited data width  
- No floating point instructions  

## Multicore
- Centralized design  
- Single point of failure  

So the solution is a Multiprocessor System.

---
# Advantages of Multiprocessor System

## Reduced Cost
- Processors share the same resources  
- No separate power supply or motherboard needed for each chip  

## Increased Reliability
- If one processor fails, others keep working  
- System slows but doesn't stop  

## Increased Throughput
- More processes = work done in less time  

## Easy to Expand
- Can add more processors as needed  

## Easy to Fix
- Tasks are divided among modules  
- Failures are easy to find and replace  
---

# Multiprocessor Issues

When multiple processors share the same memory and I/O through a common bus, extra logic is needed.

Reason:
- Only one processor should use the bus at a time  

## Two Main Problems
- Bus Contention  
- Inter-processor Communication  

---

# 8086 & 8088 in Multiprocessor

The Maximum Mode of 8086/8088 is specially designed for multiprocessor systems.  
It supports three basic configurations.

---

# Three Basic Configurations

1. Coprocessor Configuration  
2. Closely Coupled Configuration  
3. Loosely Coupled Configuration  

---

# 1. Coprocessor Configuration

- A coprocessor is connected with the main processor  
- Both work in parallel  

Example:
- 8087 is the coprocessor for 8086 — used for numeric/floating point calculations  

- 8086/8088 has no floating point instructions on its own, so 8087 helps  
- After calculation, coprocessor sends result to the main processor  

## Characteristics
- Both use the same clock generator  
- Both share the bus control logic  
- They communicate using specific instructions  

---

## How CPU & Coprocessor Interact

- CPU fetches instructions; coprocessor also receives and monitors all instructions  
- When an ESC (Escape) instruction appears, the coprocessor knows it has to execute it  
- Both decode it, but only the coprocessor executes it  
- Coprocessor sends a busy signal to CPU's TEST pin while working  
- CPU keeps running other instructions in parallel  
- When CPU needs the coprocessor's result, it executes a WAIT instruction and stops until the coprocessor finishes  
- When done, coprocessor activates the TEST pin to wake up the CPU  

---

# 2. Closely Coupled Configuration

- 8086/8088 supports an independent processor (not a coprocessor)  
- Unlike a coprocessor, this processor runs its own instruction stream  
- They share the same clock and bus control logic  
- Independent processor accesses the bus through RQ/GT lines  

---

## Interaction

- Communication happens through shared memory space  
- Host sets up a message in memory  
- Independent processor fetches the message, performs the task, then notifies the host using a status bit or interrupt  

A message includes:
- Which operation to do  
- Input parameters  
- Where to store the result  

---

# 3. Loosely Coupled Configuration

- Each CPU has its own bus control logic  
- Bus arbitration is resolved by adding external logic common to all masters  
- Multiple CPUs can form a very large system  
- Each CPU may also have its own coprocessor or independent processor attached  

---

## Advantages

- High throughput with multiple CPUs  
- Failure of one module does not crash the whole system  
- Each CPU can have a local bus for its own memory/I/O (more parallel processing)  
- System can be expanded by adding/removing modules without affecting others  

---

# Bus Arbitration Problem

When more than one bus master tries to access the shared bus at the same time — this is called the bus arbitration problem.

## Solution
Add extra bus access logic that ensures only one master controls the bus at a time.

---

# Bus Arbitration Schemes (3 types)

## 1. Daisy Chaining

- All masters use the same line for bus requests  
- Controller sends a bus grant signal which travels through masters one by one  
- First master that needs the bus grabs it and blocks the signal from going further  
- Module closest to the controller has highest priority  

### Advantages
- Simple  
- Low cost  
- Fewest control lines  
- Number of lines doesn't depend on number of modules  

### Disadvantages
- Slow (delay grows with more modules)  
- Priority is fixed by physical location  
- One module failure can crash the whole system  

---

## 2. Polling Method

- Uses address lines to identify each module  
- Controller generates a sequence of module addresses in response to a bus request  
- When a module recognizes its own address, it activates the busy line and takes the bus  

### Advantages
- Priority can be dynamically changed by changing the polling sequence  
- One module failure does not crash the system  

---