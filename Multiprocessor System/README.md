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