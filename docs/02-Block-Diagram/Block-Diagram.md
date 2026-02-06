---
title: Temp / Humidity Module's Block Diagram
tags:
- tag1
- tag2
---

## Overview
The tempurature/moisture block diagram exists to show the basic construction of the module. The module is designed to measure temperature using a PT1000 resistance temperature detector and relative humidity using a digital I<sup>2</sup>C humidity sensor while operating as one node in a daisy-chained system. The system receives power either from a barrel jack adapter or from the team power distribution connection. These two power sources are combined using P-channel MOSFET ideal-diode OR-ing circuitry to prevent reverse current flow between supplies. The selected input voltage is then regulated by the 3.3-V switching regulator. The PT1000 temperature sensor is excited by a precision constant-current source formed using a voltage reference, precision resistor, and operational amplifier. The resulting voltage across the RTD is filtered by a low-pass RC network and routed to analog input RA0 of the PIC18F47Q10 microcontroller for analog-to-digital conversion. The humidity sensor communicates digitally with the microcontroller through the I<sup>2</sup>C interface using pins RC3 (SCL) and RC4 (SDA). Communication between nodes in the daisy-chain network is performed through upstream and downstream headers that carry power and I<sup>2</sup>C communication lines. A hot-swap I<sup>2</sup>C buffer is used between the external bus and the local microcontroller to protect the system and ensure reliable communication between multiple boards connected along the chain. The microcontroller processes the sensor data and transmits the measurements to the communication module through the shared I<sup>2</sup>C network. The ICSP interface provides in-circuit programming capability through the Microchip SNAP programmer for firmware development and system debugging.


## Block Diagram 

![Temperature / Humidity Module ](TempHumModual.drawio.png)
