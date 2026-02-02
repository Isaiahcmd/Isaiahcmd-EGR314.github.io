---
title: Tempurature/Humidity Module Requirements
---

## Module Requirements
The following sections document the requirements that the this module need to fulfill to accurately sense and trasmit soil tempurature and ambient humidity to the user.

| **Requirement Description** | **Measure of<br> Threshold** | **Target<br>Measure** |**Stretch<br>Requirement<br>(Y-N)**|
|-----------------------------| ----------------- | ----------------- | :-----: |
| Surface mounted, 3.3V switching power regulatore | 3.2 Volts | 3.3 Volts | No |
| Surface mounted microcontroller | 1 PIC or ESP | 8-bit PIC | No |
| Wireless Communication | Able to send or receive a Wi-Fi data | Send and receive Wi-Fi Data to MQTT | Yes |
| Soil Temperature sensor (Analog) |  ±5°C accuracy<br> 0–50°C range<br> 1°C resolution |  ±1°C accuracy<br> −30–60°C range<br> 0.5°C resolution | No       |
| Ambient Humidity sensor (Serial)         |  ±5% accuracy<br> 10–90% humidity range<br> 5% resolution |  ±1% accuracy<br> 0–100% humidity range<br> 0.5% resolution | No      |

