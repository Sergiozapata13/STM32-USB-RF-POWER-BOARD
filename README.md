# STM32-USB-RF-POWER-BOARD

## Overview
STM32-based embedded board integrating USB, RF transceiver, and regulated power supply.
Designed in KiCad with focus on signal integrity, power distribution, EMI mitigation, and hardware validation.

## System Architecture
- STM32 microcontroller
- USB interface with ESD protection
- RF transceiver with matching network
- Buck and LDO-based power regulation
- SWD and UART debug interfaces
  
## Power Architecture

![Power architecture schematic](images/power_schematic.png)

The board is powered exclusively from the USB 5 V rail. Input protection is provided
by a resettable fuse (100 mA) and a ferrite bead (100 Ω @ 100 MHz) to limit overcurrent
conditions and attenuate high-frequency noise coming from the USB source.

A low-dropout linear regulator (XC6206P332MR) is used to generate the 3.3 V supply
required by the STM32 microcontroller and the RF transceiver. This regulator was
selected due to its low noise characteristics and simplicity, which are well suited
for low-current embedded applications (up to 200 mA).

Bulk capacitors are placed at both the regulator input and output to ensure stability
and reduce supply ripple. Reverse polarity protection was intentionally omitted, as the
USB connector is the only intended power source for the board.

## USB Design
(To be documented)

## RF Design
(To be documented)

## PCB Layout Strategy
(To be documented)

## Hardware Validation
(To be documented)

## Tools
- KiCad
- STM32CubeMX (pinout reference)

## Project Status
- PCB designed
- PCB manufactured and assembled
- Hardware bring-up and validation completed
