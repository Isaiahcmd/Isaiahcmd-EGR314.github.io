---
title: Microcontroller Selection
---

## Microcontroller 
The selected microcontroller for the sensing module is the PIC18F47Q10. 
The device provides multiple MSSP modules supporting I²C communication, allowing connection to the HDC2080 humidity sensor through the PCA9511A buffer. 
The integrated 12-bit ADC provides sufficient analog inputs for reading the PT1000 temperature probe signal conditioned by the MCP6001 amplifier and referenced by the REF3325 voltage reference. 
The microcontroller also provides multiple UART modules for inter-board communication through the 8-pin system connector. 
With over 30 GPIO pins available, the device exceeds the pin requirements for the sensing subsystem and allows future expansion.

The Temperature/Humidity subsystem is responsible for measuring soil temperature and ambient relative humidity and providing this environmental data to the rest of the CropScout system. 
Temperature measurements are obtained using the PT1000 soil probe, while ambient humidity is measured using the HDC2080 digital humidity sensor. 
The processed sensor data is transmitted to the communication subsystem through the system interface connector, where it is forwarded to the display subsystem for user visualization. 
In addition to sending measurement data, the Temperature/Humidity subsystem receives configuration inputs originating from the display subsystem, allowing the user to select temperature units (&deg;C or &deg;F) and configure threshold-based alert settings.

**Microcontroller Requirements**

## Required Microcontroller Peripherals

| Peripheral | Quantity Required | Component Using It |
|---|---|---|
| ADC | 1 channel | PT1000 temperature probe (via MCP6001) |
| I²C | 1 bus | HDC2080 humidity sensor, PCA9511A I²C buffer |
| UART (system communication) | 1 | CropScout system connector |
| GPIO | 3–6 pins | Control / interface signals |
| Interrupt (optional) | 1 | HDC2080 alert pin (optional) |
| Power / Ground pins | 8 pins (4 VDD, 4 VSS) | Microcontroller power connections |

**PIC18F47Q10**

## PIC18F47Q10-I/PT Peripheral Capability Comparison

| Peripheral | Required | Available on PIC18F47Q10 | Meets Requirement |
|---|---|---|---|
| ADC channels | 1 | 35 channels | Exceeds |
| I²C interfaces | 1 | 2 MSSP modules | Exceeds |
| UART interfaces | 1 | 2 UART modules | Exceeds |
| GPIO pins | 3–6 | 36 GPIO pins | Exceeds |
| Interrupt inputs | 1 (optional) | Multiple external interrupts | Meets |
| Power / Ground pins | 8 pins (4 VDD, 4 VSS) | 8 pins (4 VDD, 4 VSS) | Meets |

**Compatability**

Compatibility between the sensing components and the selected PIC18F47Q10 microcontroller was verified through review of the PIC18F47Q10 device datasheet, which confirms support for ADC and I²C peripherals, and through manufacturer-provided HDC2080 sensor documentation and example I²C driver implementations demonstrating standard microcontroller interfacing.

**MPLAB Configuration**
