---
title: Microcontroller Selection
---

## Microcontroller 
The selected microcontroller for the sensing module is the ESP32-S3-WROOM-1-N4. The device provides flexible peripheral routing through the ESP32-S3 GPIO matrix and supports multiple serial communication interfaces, including I²C, UART, SPI, and ADC channels.
The I²C interface allows connection to the HDC2080 humidity sensor through the PCA9511A buffer. 
The integrated 12-bit ADC provides sufficient analog inputs for reading the PT1000 temperature probe signal conditioned by the MCP6001 amplifier and referenced by the REF3325 voltage reference. 
The microcontroller also provides multiple UART interfaces for inter-board communication through the 8-pin system connector. 
With over 30 available GPIO pins on the module, the ESP32-S3 exceeds the pin requirements for the sensing subsystem and allows future expansion.

The Temperature/Humidity subsystem is responsible for measuring soil temperature and ambient relative humidity and providing this environmental data to the rest of the CropScout system. 
Temperature measurements are obtained using the PT1000 soil probe, while ambient humidity is measured using the HDC2080 digital humidity sensor via the I²C communication interface. 
The processed sensor data is transmitted to the communication subsystem through the system interface connector, where it is forwarded to the display subsystem for user visualization. 
In addition to sending measurement data, the Temperature/Humidity subsystem receives configuration inputs originating from the display subsystem, allowing the user to select temperature units (°C or °F) and configure threshold-based alert settings.

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

The ESP32-S3 provides all of the required peripherals needed for the subsystem. The built-in 12-bit ADC can read the analog signal from the PT1000 temperature probe after it is conditioned by the MCP6001 amplifier. The microcontroller also supports I²C communication, which allows it to interface directly with the HDC2080 humidity sensor. In addition, the ESP32-S3 includes multiple UART interfaces, which can be used for communication with the rest of the CropScout system through the system connector.

Another advantage of the ESP32-S3 is that it provides more than enough GPIO pins for the subsystem. This allows the design to include status signals, sensor connections, and other control lines without running out of pins, while still leaving room for possible future additions.

The ESP32-S3 is also widely supported and relatively easy to program using common development environments such as Arduino or ESP-IDF. This makes firmware development simpler compared to some other microcontrollers that require more specialized tools.

Overall, the ESP32-S3-WROOM-1-N4 satisfies all peripheral, processing, and communication requirements for the sensing subsystem while remaining straightforward to program and expand, making it a practical choice for the CropScout system.
