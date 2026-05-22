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