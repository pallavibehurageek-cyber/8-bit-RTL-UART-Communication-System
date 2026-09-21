
# 8-bit UART Serial Communication System

## Overview

This project implements an 8-bit UART (Universal Asynchronous Receiver/Transmitter) communication system using Verilog HDL.

The system demonstrates serial data transmission and reception using a UART transmitter and receiver. A loopback connection is used to send the transmitted data directly to the receiver for verification.

## Features

- 8-bit UART communication
- UART transmitter and receiver
- Start and stop bit handling
- LSB-first data transmission
- Configurable clock cycles per bit
- TX-to-RX loopback verification
- Verilog-based RTL design
- Simulation and waveform analysis

## System Architecture

```text
        8-bit Input Data
               |
               v
      +------------------+
      | UART Transmitter |
      +------------------+
               |
               | Serial Data
               v
      +------------------+
      |   UART Receiver  |
      +------------------+
               |
               v
       8-bit Output Data

UART Frame Format

A UART frame consists of a start bit, 8 data bits, and a stop bit.

Idle | Start | D0 D1 D2 D3 D4 D5 D6 D7 | Stop | Idle

The data is transmitted serially, starting from the least significant bit (LSB).

UART Transmitter

The transmitter converts 8-bit parallel data into a serial data stream.

8-bit Parallel Data
        |
        v
 UART Transmitter
        |
        v
   Serial Data

UART Receiver

The receiver accepts the serial data stream and converts it back into 8-bit parallel data.

Serial Data
        |
        v
   UART Receiver
        |
        v
8-bit Parallel Data

Loopback Testing

For verification, the transmitter output is directly connected to the receiver input.

UART TX
   |
   | Serial Data
   v
UART RX
   |
   v
Received Data

This allows the transmitted and received data to be compared during simulation.

Verification

The testbench performs the following steps:

1. Provides an 8-bit data value to the transmitter.


2. Converts the data into serial form.


3. Sends the serial data to the receiver.


4. Reconstructs the received data.


5. Compares the transmitted and received values.


6. Observes the signals using simulation waveforms.



Tools Used

Verilog HDL

Icarus Verilog

GTKWave

Visual Studio Code

Learning Outcomes

This project provides practical understanding of:

UART serial communication

Parallel-to-serial conversion

Serial-to-parallel conversion

Verilog HDL

RTL design

Testbench development

Digital communication

Simulation and waveform analysis


Applications

UART is commonly used in:

Embedded systems

Microcontroller communication

FPGA systems

Serial communication interfaces

Debugging interfaces

Peripheral communication


Future Improvements

Baud-rate configuration

Parity-bit support

FIFO buffering

Error detection

Overrun detection

FPGA implementation

Support for additional UART configurations


Conclusion

This project demonstrates an 8-bit UART serial communication system using Verilog HDL. The transmitter and receiver are connected through a loopback arrangement, allowing the complete communication process to be verified through simulation and waveform analysis.

