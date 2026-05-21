# 🧠 Computer Hardware Organization

A computer has these main parts connected by a Common Bus (address, data & control):

- Processor — has Control Unit, ALU, and Registers  
- Memory — stores programs and data  
- Input Units — takes data in  
- Output Units — gives data out  

---

# 💻 Computer Systems

Two parts of a computer system:

- Internal — Processor + RAM  
- Peripheral — Disk, Display, Audio, etc.  

---

# 🔌 Peripherals & Interfaces

- Peripheral — the actual device (e.g. HD monitor, 5.1 speaker)  
- Interface (Hardware) — the middle hardware that connects them (e.g. Nvidia GPU card, Sound Blaster card)  
- Interface (Software) — the driver/program that makes it work (e.g. Nvidia GPU driver, Sound Blaster driver)  

---

# 📦 What is a Peripheral?

- Any auxiliary device connected to the computer but not part of it  
- Expands the computer's capabilities  
- Often depends on the host computer  

## Types:
- Input — sends data to the computer (keyboard, mouse)  
- Output — gives results to the user (monitor, speaker)  
- Storage — stores processed data (hard disk, USB)  

---

# 🔗 What is an Interface?

- A point where two systems meet and interact  
- A shared boundary where components exchange information  
- Can be between software, hardware, peripherals, or humans  
- Examples: User Interface (UI), Command Line Interface (CLI)  

---

# ⚙️ What is Interfacing?

The technique of adding extra devices to the main processor.

## Types:
- Hardware Interface  
- Software Interface  

---

# ❓ Why Interfacing is Needed?

Peripherals are very different from the CPU:

- Different data transfer rates  
- Use different codes and control signals  
- Data can be serial or parallel  
- May work at higher voltages than the CPU  
- All work much slower than the CPU  

---

# 🔧 Functions of an Interface (BHCVC)

- Buffering — temporarily holds data during transfer  

## Handling status signals:
- Off-line → not ready to receive data  
- Busy → buffer full, cannot receive data  
- Ready → online and ready  

- Converting serial ↔ parallel data  
- Voltage conversion — adjusts voltage levels  
- Converting analogue ↔ digital data  

---

# 🌐 Interface Standards

| Standard | Full Name |
|----------|----------|
| RS232 | Recommended Standard (Serial) |
| SCSI | Small Computer Systems Interface (Parallel) |
| IDE | Integrated Drive Electronics |
| SATA | Serial Advanced Technology Attachment (up to 1.5Gbps) |
| IEEE | Institute of Electrical & Electronics Engineers (e.g. FireWire) |
| MIDI | Musical Instrument Digital Interface |
| PCI | Peripheral Component Interconnect |
| PCMCIA | Personal Computer Memory Card International Association |
| USB 1, 2 & 3 | Universal Serial Bus |

Using standards makes devices compatible with each other.

---

# 🔌 Hardware Interface Types

## Parallel Interface
- Multiple lines, sends several bits at the same time  
- Example: printer connected via parallel port  

## Serial Interface
- Sends data as a series of voltage pulses on a single wire  
- Logic 1 = high voltage, Logic 0 = low voltage  

---

## Interface Device
A device that meets the interface specifications on one side of an interface.

---

# Example Block Diagram (8085 ↔ Memory)

8085 communicates with Memory through three lines:

- Address Lines — tells which memory location to access  
- Data Lines — carries the actual data  
- Control Lines — controls read/write operations  

All three together form the Interface.

---

# Interfacing I/O Devices

I/O devices transfer data between the microprocessor and the outside world.

## Parallel I/O
- 8 bits transferred at a time using the full data bus  

## Serial I/O
- 1 bit at a time using SID (Serial Input Data) and SOD pins  

---

# Types of Parallel Interface

Two ways to interface 8085 with I/O devices:
- Memory Mapped I/O  
- I/O Mapped I/O  


# 🧵 Bus

A bus is a communication system that transfers data between components inside a computer or between computers. Includes hardware (wires) and software (protocols).

## Types:

### Internal Bus
- Connects internal parts like CPU and memory to the motherboard  
- Also called: memory bus, system bus, Front-Side Bus, or local bus  

### External Bus
- Connects external devices (like a printer) to the computer  
- Also called: expansion bus  

---

# Microprocessor (μP)

- Introduced in 1971, grew incredibly fast  
- Four generations so far  
- Devices per chip increased 2000x, clock speed increased 1000x  
- Overall performance increased by hundreds of times  

---

# Definitions

## Microprocessor
Central unit of a microcomputer. Does arithmetic and logical operations. One chip can have RAM, ROM, PROM, clock, and I/O interfaces.

---

## Microprogramming
A way to control the CPU where each instruction runs a series of smaller instructions called microinstructions.

---

## Multiprocessor
A system with two or more processing units, shared memory, and shared I/O.

---