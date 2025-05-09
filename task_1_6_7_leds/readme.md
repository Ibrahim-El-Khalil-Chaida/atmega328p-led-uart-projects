# Task 1.7 – UART-Controlled LED Speed (ATMega328P + Gertboard)

This project allows the user to control the speed of an LED animation using **UART serial communication**.

- The microcontroller (ATMega328P) receives commands over UART from a terminal (e.g., `minicom`)
- The LED pattern runs across 12 LEDs (D1 to D12) connected to **PORTB** and **PORTD**
- The user sends `1`, `2`, or `3` to change the animation speed in real-time
- Feedback is printed back to the terminal

---

## 🧠 Features

- **9600 baud UART communication**
- **UART RX (PD0)** and **TX (PD1)** used for serial link with Raspberry Pi
- Speed options:
  - `1` → 200 ms delay
  - `2` → 1000 ms delay
  - `3` → 2000 ms delay
- Real-time UART response:
  - Example: `Speed set to 1 second`

---

## 🔧 Hardware Setup

- **Microcontroller:** ATMega328P on Gertboard
- **Clock:** 12 MHz (3.3V safe)
- **LEDs:**
  - `PORTB (PB0–PB5)` → LEDs D1–D6
  - `PORTD (PD2–PD7)` → LEDs D7–D12
- **UART:** Connected to Raspberry Pi via GPIO 14 (TX) and GPIO 15 (RX)

---

## 💻 How to Use

1. **Connect Raspberry Pi to Gertboard**
2. Flash the program:

   ```bash
   make
   make flash
minicom ama0
1 for fast

2 for medium

3 for slow
