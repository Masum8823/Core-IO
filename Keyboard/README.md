# ⌨️ What is a Keyboard?

## 📌 Definition
A keyboard is an input device of a computer system.

It contains:
- Alphabet keys  
- Number keys  
- Special character keys  
- Control keys  

It is used to send user data and commands to the computer.

---

## 🧱 Keyboard Organization
A keyboard has many switches arranged in a matrix form.  
It also contains an electronic circuit called a keyboard encoder.

---

## ⚙️ Functions of Keyboard Encoder
- Monitors all key switches  
- Detects key press and key release  
- Encodes key information and sends it to the computer system  

---

## 🧠 Keyboard Controller
A microcontroller on the motherboard called the keyboard controller receives keyboard data.  
It decodes the data and sends it to the system for further processing.

---
## 🔘 Keyboard Switches
When a key is pressed, a switch becomes active and generates signals for communication with the computer.

---

## 📌 Types of Keyboard Switches
- Capacitive Switch  
- Mechanical Switch  
- Membrane Switch  
- Hall Effect Switch  

---

# 🔘 Capacitive Switch

## 📌 Definition
A capacitive switch has two small metal plates.  
When a key is pressed, the plates come closer.  
This changes the capacitance between the plates.  
The change in capacitance is detected and converted into logic signals to identify the key action.

---

## 👍 Advantage
It has no metal contacts.  
So, it does not get oxidized easily.

---

## ⚙️ Special Circuit Used
It requires special circuits such as:
- Oscillator  
- PLL (Phase Locked Loop)  
- Comparator  

These circuits convert switch actions into logic signals.

---

# 🔘 Mechanical Switch

## 📌 Definition
A mechanical switch uses metal contacts.  
When a key is pressed, the contact closes.  
When the key is released, the contact opens again.  
Springs help return the key to its original position.

---

## ⚠️ Problems and Solutions

### Problem 1: Key Bouncing
Small unwanted repeated signals may occur for about 5 ms or less.

**Solution**
Use a key debouncing technique.

---

### Problem 2: Oxidation
Metal contacts may become oxidized over time.

**Solution**
Use gold-plated contacts.

---

## ⭐ Additional Features
- Can last for about 10 million key presses.  
- If contacts become dirty, bouncing time may increase (called chattering).  
- Less expensive compared to other switch types.  

---

# 🔘 Membrane Switch

## 📌 Definition
A membrane switch is a special type of mechanical switch.

It uses two plastic or rubber sheets:
- Row sheet  
- Column sheet  

Another sheet with holes is placed between them at key positions.

---

## 🧱 Structure
- The top layer is the row layer.  
  It has conductive lines under each row of keys.  

- The bottom layer is the column layer.  
  It has conductive lines under each column of keys.  

---

## ⚙️ Working Principle
- When a key is pressed, the row line touches the column line through the hole.  
- This contact is detected by interfacing circuits.  
- Then the key signal is sent to the computer system.  

---

# ⌨️ Keyboard Encoders

## 📌 Working of Keyboard Encoder
When a key is pressed, the hardware:
- Detects the key press  
- Removes key bouncing  
- Finds the row and column number of the key  
- Converts the information into a standard code  
- Sends the information to the computer system  

An 8048 microcontroller-based keyboard encoder performs these tasks.

---

## 🧠 Keyboard Debouncing
Key bouncing should not be treated as multiple key presses and releases.  
Different hardware and software debouncing methods are used.

### Simple Debouncing Method
A software delay of about 20 ms is added whenever a key is pressed or released.

---

## 🔍 Keyboard Scanning
Keyboard switches are arranged in rows and columns.  
Every key has a unique row and column number.

Finding the row and column of a pressed key is called keyboard scanning.

---

## 📌 Example
For 16 keys (0 to F), a 4×4 matrix is used.

---

# ⌨️ Keyboard Scanning Process

---

## 🔍 Step 1: Check if Any Key is Pressed
First, 0000 is written to the output port.  
Then the input port is read.

### 📌 Result
- If all keys are open → input port reads 1111  
- If a key is pressed → one bit becomes 0  

This helps find the column number of the pressed key.

---

## ⏳ Step 2: Debouncing
A delay of about 20 ms is given.  
The input port is read again to confirm the key press.

---

## 📍 Step 3: Find the Row Number
The output port bits are changed one by one.

### 📌 Example
- First output = 1110  
  Input port is read:  
  - If all bits are 1, the key is not in that row.  

- Next output = 1101  
  Input is read again.  

This process continues until one input bit becomes 0.

---

## 🎯 Final Result
- The output port value gives the row number.  
- The input port value gives the column number.  

Using row and column values, the system identifies the pressed key.

---