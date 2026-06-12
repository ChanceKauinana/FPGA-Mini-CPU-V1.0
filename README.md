# Simple 4-Bit CPU on Basys 3

This project is a small 4-bit accumulator-based CPU written in Verilog for the Digilent Basys 3 FPGA board.

The CPU executes a short program stored in ROM, displays the accumulator value on the Basys 3 seven-segment display, and also shows the accumulator value on the board LEDs.

## Hardware

- Board: Digilent Basys 3
- FPGA: Artix-7 `xc7a35tcpg236-1`
- Clock: 100 MHz onboard clock
- Reset: Center button `btnC`
- Output: LEDs and 4-digit seven-segment display

## Current Features

- 4-bit accumulator
- 4-bit program counter
- 8-bit instructions
- ROM-based program memory
- Simple ALU
- Immediate-style instructions
- HALT instruction
- Debounced reset button
- Clock divider for visible CPU execution
- Seven-segment display output

## Project Structure

```text
Simple-CPU-Basys3/
├── README.md
├── .gitignore
├── rtl/
│   ├── top.v
│   ├── simple_cpu.v
│   ├── alu.v
│   ├── rom.v
│   ├── clk_divider.v
│   ├── debounce.v
│   └── seven_dig_display.v
└── Constraints/
    └── Basys3_Simple_CPU.xdc