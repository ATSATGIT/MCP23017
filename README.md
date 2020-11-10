# MCP23017
Driver code reference for IC configuration, functions for write and read

Work in progress...

The driver is developed using the STM32H7 HAL Cube library.

Requirements:

1. Understanding the datasheet MCP23017

  - Registers required for configuring/read/write IO ports.
  - Byte mode vs Sequential mode and it's settings in IOCON register
  - IODIR settings for write and read
  - Mode of communication to IC - I2C interface
  - I2C Frame format for read and write
  
Byte mode :  S OP W ADDR DIN P

S         0 1 0 0 A2 A1 A0 0 ACK  * A7 A6 A5 A4 A3 A2 A1 A0 ACK *  DIN(D7 to D0) ACK    P
Start         Device Opcode              Register Address             Data              Stop

