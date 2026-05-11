# ⚙️ Motor

## 📌 Definition
An electric motor is an electrical machine that converts **electrical energy into mechanical energy**.

---

## 🖼️ Image of Motor:
*(image)*

---

## 🔄 Types of Motor

- ✔ AC Motors  
- ✔ DC Motors  
- ✔ Brushless Motors  
- ✔ Brushed Motors  
- ✔ Servo Motors  
- ✔ Stepper Motors  
- ✔ Synchronous Motors  
- ✔ Asynchronous Motors  

---

# 🔌 DC Motors

## 📌 Definition
DC motors are simple motors with **2 wires (power and ground)** and they rotate continuously.

---

## ⚙️ Working Principle
- When we give power, the motor starts spinning.
- It keeps running until we turn off the power.

---

## 🚀 Characteristics
- Most DC motors spin very fast  
- High RPM (Rotations Per Minute = high speed)

---

## 📌 Examples
- Computer fan  
- RC car wheels  

---

# ⚙️ Servo Motor 

## 📌 Definition
A servo motor is a type of motor that rotates with high precision (very accurate position control).  
Servo uses an error-sensing feedback control system, which helps to check the output position and correct it if there is any error in the system performance.

---

## 🔧 Main Parts of Servo Motor
A servo motor is generally made of four main parts:

- DC motor  
- Gear system (gearing set)  
- Control circuit  
- Position sensor (usually a potentiometer)  

---

## ⭐ Key Features
- The position of a servo motor can be controlled more accurately than a standard DC motor  
- Usually, servo motors have three wires: power, ground, and control  
- Power is continuously supplied, but the control circuit manages how much power is used  
- Servo motors do not rotate freely like normal DC motors  

---

## 📌 Example Uses
- Controlling the rudder of a boat  
- Moving a robotic arm  
- Moving robot legs within a fixed range  

---

# ⚙️ Servo Motor Working Principle

- The DC motor runs using battery power.  
- It rotates at high speed but gives low torque.  
- Gear and shaft assembly reduce the speed and increase the torque.  
- A position sensor detects the shaft position and sends information to the control circuit.  
- The control circuit compares the actual position with the desired position and controls the motor direction accordingly.  
- Servo motors usually need a DC supply of 4.8V to 6V.

---

# 🎛️ Controlling a Servo Motor

- Servo motor control signal uses PWM (Pulse Width Modulation).  
- Unlike DC motors, here the length of the positive pulse decides the position of the motor shaft.  
- A neutral pulse (around 1.5 ms) keeps the servo in the middle position.  
- A longer pulse moves the servo clockwise.  
- A shorter pulse moves it anticlockwise.  
- The control signal is repeated every 20 milliseconds, even if the position stays the same.  

---

## 🖼️ Image Link:
*(Add your image link here)*

---

# ⚙️ Stepper Motors

- A stepper motor is a type of motor that moves in small steps instead of continuous rotation.  
- It is similar to a servo motor, but it works in a different way. Servo motors use a DC motor with a control circuit, while stepper motors use multiple electromagnets arranged around a central gear to control position.  
- Stepper motors are used where precise position control is needed, such as hard disk drives, robotics, antennas, telescopes, and some toys.  
- Stepper motors cannot run at very high speeds, but they have high holding torque (they can hold position strongly).  
- A stepper motor is operated by a DC voltage through a driver circuit.  

---