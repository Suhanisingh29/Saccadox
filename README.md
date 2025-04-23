# SACCADOX
Saccadox-An Arduino-based interactive system with 33 illuminated push buttons arranged in concentric circles, featuring LED sequencing, user input detection, and a 7-segment display counter using Master-Slave I2C communication.


This project is a reaction-based training and testing system developed using two Arduino Mega boards. It features 33 illuminated push buttons arranged in a circular manner. The system lights up a random LED, and the user has to press the corresponding button. When the correct button is pressed, the 7-segment display updates the score count.

---

## 🚀 Features

- 🟢 **Random LED Illumination**: One of the 33 LED push buttons lights up at random.
- 👆 **User Interaction**: The user must press the button that corresponds to the glowing LED.
- ✅ **Correct Press Detection**: Upon pressing the correct button, the LED turns off, and the score is incremented.
- 🔢 **Live Score Display**: A 2-digit 7-segment display shows the current score in real-time.
- 🔄 **Dual Arduino Communication**: One Arduino Mega serves as the **Master** (controls 13 LEDs), while the other is the **Slave** (controls 20 LEDs) via I²C.

---

## ⚙️ Hardware Setup

- **Arduino Mega x2** (Master and Slave)
- **33 LED push buttons** (10 + 3 on Master, 20 on Slave)
- **7-Segment Display with 74HC595 shift register**
- **Circular layout**: LEDs arranged concentrically
- **SPI communication** for 7-segment display
- **I²C communication** between Master and Slave

---

## 🔧 How It Works

1. The system starts by randomly lighting up an LED push button.
2. The user finds and presses the illuminated button.
3. If the button pressed is correct:
    - The LED turns off.
    - The score is incremented.
    - The next random LED lights up.
4. This process continues, and the live score is updated on the display.

---

## 📁 Files

- `Master.ino` – Controls main logic, random LED selection, scoring, and 7-segment display.
- `Slave.ino` – Handles the slave side button-LED logic and communicates with the master.

---
