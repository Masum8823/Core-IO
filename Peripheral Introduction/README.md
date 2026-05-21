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
