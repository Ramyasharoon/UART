# UART Transmitter using Verilog HDL

## Project Overview

This project implements a UART (Universal Asynchronous Receiver Transmitter) Transmitter using Verilog HDL. UART is a serial communication protocol widely used for communication between microcontrollers, computers, sensors, and embedded systems.

The transmitter sends one byte of parallel data serially by adding:
- 1 Start Bit (Logic 0)
- 8 Data Bits (LSB First)
- 1 Stop Bit (Logic 1)

---

## Features

- UART Transmitter (TX)
- 8-bit Data Transmission
- Start and Stop Bit Generation
- Parameterized Clock Divider
- Verilog HDL Implementation
- Testbench Included

---

## Inputs

| Signal | Description |
|---------|-------------|
| clk | System Clock |
| rst | Active High Reset |
| tx_start | Starts Transmission |
| tx_data[7:0] | Data to Transmit |

## Outputs

| Signal | Description |
|---------|-------------|
| tx | UART Serial Output |
| busy | Transmission Busy Flag |

---

## UART Frame Format

Start | D0 | D1 | D2 | D3 | D4 | D5 | D6 | D7 | Stop

0      LSB -------------------------> MSB      1

---

## Project Files

- uart_tx.v
- uart_tx_tb.v
- simulation_output.txt
- simulation_waveform.png

---

## Software

- Vivado
- ModelSim
- Icarus Verilog
- GTKWave

---

## Compile

```bash
iverilog uart_tx.v uart_tx_tb.v
```

Run

```bash
vvp a.out
```

View Waveform

```bash
gtkwave uart_tx.vcd
```

---

## Applications

- Serial Communication
- Embedded Systems
- FPGA Designs
- Microcontroller Interfaces
- IoT Devices

---

## Author

Your Name