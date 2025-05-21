
# 📲 RPi4 Control — TorHando

This module contains Python scripts for operating the robot end-effector using a **Telegram bot** on Raspberry Pi 4.

---

## 🤖 Functionality

- Remote bot control via Telegram chat commands
- Servo actuation for dropping a ball
- Uses `telepot` library for messaging

---

## 📜 Features

| Command | Action |
|---------|--------|
| `/hi`   | Greets user |
| `/time` | Sends current time |
| `/date` | Sends current date |
| `/drop` | Executes servo-based drop mechanism |

---

## 🛠 Requirements

- Raspberry Pi 4 (Raspbian)
- Servo motor
- Telegram Bot Token (via BotFather)
- Python libraries: `telepot`, `RPi.GPIO`, `datetime`

---

## 🚀 Run Script

```bash
sudo pip install telepot
python3 test_with_servo_telegram_bot.py
```