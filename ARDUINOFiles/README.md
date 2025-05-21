# 🔌 Arduino Integration — TorHando

This module handles low-level hardware interfacing using Arduino microcontrollers. It primarily focuses on serial communication and actuation logic for components like motors and sensors.

---

## 📋 Overview

Arduino is used in this project for:
- Controlling actuators like servos or motors
- Collecting sensor data (e.g., ultrasonic sensors, IR)
- Communicating with higher-level processors (e.g., Raspberry Pi) via serial interface
- Real-time feedback and control loops

---

## 🧰 Folder Contents

| File/Folder        | Description |
|--------------------|-------------|
| `main_code.ino` *(example)* | Main control script for Arduino (e.g., motor or servo control) |
| `serial_test.ino` | Test script to verify communication with external controllers |
| `README.md`        | This documentation |

> *(Note: Add your actual Arduino files or rename the examples accordingly)*

---

## 🔌 Hardware Setup

- Arduino UNO / Nano / Mega
- USB cable for serial connection
- Servo motor (SG90/MG996R) or DC motor + driver (e.g., L298N)
- Optional: IR or ultrasonic sensors

---

## ⚙️ Serial Communication

Arduino can act as a slave device listening to commands via:
```cpp
void loop() {
  if (Serial.available()) {
    char command = Serial.read();
    // Parse and execute command
  }
}
```

This allows integration with ROS or Python-based teleop modules (e.g., RPi4).

## 🚀 Upload Instructions
Open any .ino file in Arduino IDE.

Select the correct board and COM port.

Click Upload.

## 🧪 Testing & Debugging
Use Arduino Serial Monitor or a Python serial interface (pyserial) to send commands and observe behavior.

## 💡 Tip
Use PWM pins (like 3, 5, 6, 9, 10, 11) for motor speed control via analogWrite(pin, value).

## 📎 Related Modules
See **RPi4** to integrate this logic into a Telegram bot-based remote control system.