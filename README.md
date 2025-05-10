# SACCADOX
Saccadox-An Arduino-based interactive system with 33 illuminated push buttons arranged in concentric circles, featuring LED sequencing, user input detection, and a 7-segment display counter using Master-Slave I2C communication.


This project is a reaction-based training and testing system developed using two Arduino Mega boards. It features 33 illuminated push buttons arranged in a circular manner. The system lights up a random LED, and the user has to press the corresponding button. When the correct button is pressed, the 7-segment display updates the score count.

---

## 🚀 Features

This system supports four different modes, each with a unique pattern of LED illumination and timing behavior:

---

### 1️⃣ Random Button Glowing (Without Delay)

- A **random LED** lights up.
- The **user must press the correct button**.
- Only **after correct press**, the next random LED lights up.
- Each correct press **increments the score**.
- **No automatic switching** unless the correct button is pressed.

**🔧 Code Files:**
- Master: `Random_Without_Delay_Master.ino`
- Slave: `Random_Without_Delay_Slave.ino`

---

### 2️⃣ Random Button Glowing (With Delay)

- A **random LED** lights up.
- The system **waits 1500 ms**, then switches to a new random LED.
- **Only button presses during LED ON time are counted**.
- Adds a timed challenge to the reflex.

**🔧 Code Files:**
- Master: `Random_With_Delay_Master.ino`
- Slave: `Random_With_Delay_Slave.ino`

---

### 3️⃣ Circular Button Glowing (Without Delay)

- LEDs **glow in a circular clockwise sequence**, starting from the inner circle outward.
- The next LED **glows only after a correct button press**.
- Emulates an **order-based saccadic pattern**.
- Score updates only on valid button presses.

**🔧 Code Files:**
- Master: `Circular_Without_Delay_Master.ino`
- Slave: `Circular_Without_Delay_Slave.ino`

---

### 4️⃣ Circular Button Glowing (With Delay)

- LEDs **glow sequentially in a clockwise circular pattern**.
- Each LED is ON for **1.5 seconds**.
- If the user does not press the button in time, the system **moves to the next one**.
- Only correct presses during the ON time are counted.

**🔧 Code Files:**
- Master: `Circular_With_Delay_Master.ino`
- Slave: `Circular_With_Delay_Slave.ino`

---

## 📟 Hardware Overview

- **Arduino Mega x2** (Master & Slave)
- **33 LED push buttons**
  - 13 connected to Master
  - 20 connected to Slave
- **7-Segment Display** (2-digit with 74HC595)
- **SPI Communication** for display
- **I²C Communication** between Master and Slave
- **Circular layout** with:
  - 1 button at center
  - 8 buttons in first circle
  - 8 buttons in second circle
  - 16 buttons in third circle
- **Spacing:** 10 cm between each concentric circle

## 📁 File Structure

```plaintext
├── Random_Without_Delay_Master.ino
├── Random_Without_Delay_Slave.ino
├── Random_With_Delay_Master.ino
├── Random_With_Delay_Slave.ino
├── Circular_Without_Delay_Master.ino
├── Circular_Without_Delay_Slave.ino
├── Circular_With_Delay_Master.ino
├── Circular_With_Delay_Slave.ino
└── README.md

