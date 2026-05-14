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