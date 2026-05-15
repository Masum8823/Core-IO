 🖱️ What is a Mouse?

## 📌 Definition
A mouse is an input device of a computer system.  
It is used as an X-Y position indicator on the screen.

---

## 🧱 Mouse System
A mouse system consists of:
- Hardware device (Mouse)  
- Software program (Mouse Driver)  

---
## ⚙️ Mouse Driver
The driver helps move the cursor on the screen.  
It controls cursor movement and mouse operations.

It also manages:
- Cursor position  
- Cursor shape  
- Button status  

## 🧠 Mouse Driver Details
- The driver receives the data packet.  
- It decodes the information.  
- Then it informs the application software to perform necessary actions.  


---

## 🔘 Mouse Buttons
A mouse may have:
- One button  
- Two buttons  
- Three buttons  

Two-button mouse is most common.

---

## 🖱️ Mouse Events
Mouse events include:
- Moving the mouse  
- Left or right button click  
- Double-clicking the left button  
- Dragging (holding left button and moving the mouse)  

---

## 📡 Communication
The mouse driver sends mouse event information to the computer system.

---

# 🖱️ Working of Mouse

- A mouse uses two rollers:  
  - One for X-axis movement  
  - One for Y-axis movement  

- The rollers control the movement direction.  
- Light beams pass from a source to a sensor.  
- Movement generates pulse signals.  
- These signals are converted into X and Y movements.  

---

## 📦 Mouse Encoder
The mouse encoder reads:
- Cursor position  
- Button status  

It sends this information as a data packet to the computer interface controller.

---



## 🔌 Mouse Interfaces
Different interfaces are used to connect a mouse to the computer:

- Serial Interface  
- PS/2 Port (Motherboard Mouse Port)  
- USB Interface (Most modern systems)  

---

# 🖱️ Serial Mouse

## 📌 Introduction
Previously, serial interface was widely used to connect a mouse to a computer.  
A serial mouse connects through:
- COM1 port  
- COM2 port  

These ports are RS-232C compatible.  
COM means Communication Port.

---

## ⭐ Features of Serial Mouse
- Usually uses a 9-pin connector  
- Requires a small amount of power from the serial port  
- Communication is one-way (unidirectional)  
- Mouse sends data to the computer through the RxD line  

---

## 📡 Communication Format
Uses:
- 1 Start bit  
- 7 Data bits  
- No parity  
- 1 Stop bit  

Data transfer speed is 1200 baud rate.

---

## 📦 Data Packets
- Mouse sends movement and button information as data packets  
- Usually sends 40 packets per second  
- A packet normally contains 3 bytes  
- Each byte is 7 bits wide  

---

## 📍 Movement Information
- X7–X0 → Movement in X direction  
  - Positive (+) → Right  
  - Negative (−) → Left  

- Y7–Y0 → Movement in Y direction  
  - Positive (+) → Up  
  - Negative (−) → Down  

---

## 🔘 Button Status
- LB → Left button status  
- RB → Right button status  

If a button is pressed, its bit becomes 1.

---

## ⚠️ Important Point
- If mouse position or button state changes, the mouse sends a 3-byte data packet to the system  
- The MSB of the first byte is set to 1  
- The MSB of the second and third bytes are set to 0  
- This helps identify the first byte of the packet  

---

# 🖱️ Serial Mouse – 3 Byte Data Packet (Bit Definition)

| Byte   | D6 | D5 | D4 | D3 | D2 | D1 | D0 |
|--------|----|----|----|----|----|----|----|
| Byte-1 | 1  | LB | RB | Y7 | Y6 | X7 | X6 |
| Byte-2 | 0  | X5 | X4 | X3 | X2 | X1 | X0 |
| Byte-3 | 0  | Y5 | Y4 | Y3 | Y2 | Y1 | Y0 |

---
