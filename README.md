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

The board is powered exclusively from the USB 5 V rail. Input protection is provided
by a resettable fuse and a ferrite bead to limit overcurrent conditions and attenuate
high-frequency noise coming from the USB source.

A low-dropout linear regulator (XC6206P332MR) is used to generate the 3.3 V rail required
by the STM32 microcontroller and RF transceiver. This device was selected due to its low
noise characteristics and simplicity, which are suitable for low-current applications
(≤200 mA).

Bulk and local decoupling capacitors are placed at the regulator input and output to
ensure stability and reduce supply ripple. Reverse polarity protection was intentionally
omitted, as USB is the only intended power source.

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
