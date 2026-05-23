# Types of Data Transfer

## 1. Programmed

- Data moves between CPU and I/O device  
- A program/code in memory controls everything  

---

## 2. DMA (Direct Memory Access)

- CPU is bypassed  
- Data goes directly between memory and I/O device  

---
# Modes of Data Transfer

## Synchronous
- Sender & receiver work at same time/clock  

## Asynchronous
- No fixed timing  

## Interrupt Driven
- I/O device interrupts the CPU when ready  

---

# Interrupt Driven — How it works

- CPU sends "Get Ready" signal to I/O device  
- CPU keeps doing its own work  
- When I/O is ready → it sends an interrupt signal  
- CPU saves its current state (PC saved in stack)  
- CPU runs the ISS (Interrupt Service Subroutine)  
- After finishing → CPU restores its state and returns  

---

# DMA Mode — How it works

- DMA Controller is initialized  
- CPU sends "Get Ready" to I/O device  
- I/O device gets ready → sends DMA Request to DMA Controller  
- DMA Controller sends DMA Request to MPU  
- MPU gives DMA Grant → tristates the buses (lets go of control)  
- Data transfers directly until the whole block is done  
- DMA Controller withdraws the request → CPU takes back control  

---