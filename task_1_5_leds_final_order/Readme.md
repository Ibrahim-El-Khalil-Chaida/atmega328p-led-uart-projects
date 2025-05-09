# Task 1.5 – LED Animation Sequence

This program lights up 12 LEDs one by one (D7–D12, then D1–D6), and then turns them off in reverse order.

## 🔧 How It Works
- Uses PORTD (PD2–PD7) for LEDs D7–D12
- Uses PORTB (PB0–PB5) for LEDs D1–D6
- Uses `_delay_ms()` to control animation timing

## ⏱ Clock: 12 MHz
## 🔋 Power: 3.3V (Gertboard)

## 💻 To Compile and Flash:
```bash
make
make flash
