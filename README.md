#  Verilog Digital Clock

This project implements a real-time digital clock in Verilog that displays time in **HH:MM:SS** format on an **8-digit 7-segment display**. It is designed for FPGA boards such as the **Basys 3** with a **50 MHz input clock**.

---

## Features

- Displays time in `HH:MM:SS` using multiplexed 7-segment output
- Clock division to generate 1 Hz from a 50 MHz clock
- BCD-based counters for time tracking
- Colon display (`:`) between hours, minutes, and seconds
- Works with active-low digit selection and active-high segments

---

## Working

- `count`: Divides 50 MHz clock to create a 1 Hz `sec_clk`
- `time_r`: 24-bit BCD counter (6 digits: HH MM SS)
- `seg_r`: Holds current digit to be displayed (based on multiplexer)
- `dig` & `seg`: Output to drive 7-segment display


##  License

This project is open-source and free to use under the [MIT License](LICENSE).

