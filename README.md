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

The board implements a regulated power architecture designed to support USB-powered
operation as well as external supply input. A buck regulator is used for efficient
voltage conversion, followed by local LDO regulation and ferrite bead isolation to
ensure clean power delivery to sensitive domains.

Key design considerations include:
- Separation of high-current switching paths from sensitive analog and RF circuitry
- Compact high-current loops in the switching regulator section
- Local decoupling capacitors placed close to IC power pins
- Ferrite beads used to isolate digital, analog, and RF supply domains

This architecture was selected to balance efficiency, noise performance, and layout
simplicity while maintaining robustness during hardware bring-up and validation.

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
