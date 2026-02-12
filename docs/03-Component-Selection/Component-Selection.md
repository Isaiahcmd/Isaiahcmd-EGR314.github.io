---
title: Module's Selected Major Components
---

## Module's Selected Major Components

The following sections are the selected major components necessary for  .....

>**For each of the following sections, use <ins>one of the two styles</ins> given near the end. *REMOVE THIS NOTE***

### Power Management

(**remove this note/placeholder**: this is where your 3.3 volt switching regulator, any other needed power regulator, and power source {if applicable} **THAT WERE SELECTED**)

For more details, review the ["Appendix - Component Selection Process - Power Mangement"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#power-management) selection.

### Sensor

(**remove this note/placeholder**: if applicable, this is where your  **SELECTED** sensor is shown. Otherwise, remove this section.)

For more details, review the ["Appendix - Component Selection Process - Sensor"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#sensor) selection.

### Actuator

(**remove this note/placeholder**: if applicable, this is where your **Selected** the actuator items go, which includes both the driver and motor. Otherwise, remove this section.)

For more details, review the ["Appendix - Component Selection Process - Actuator"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#actuator) selection.

-----------
> Remove the following before submitting! Use them to present the selected components

### Style 1

> This is the example found in the assignment, uses more html

*Table 1: Example component selection*

**Moisture Sensor**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](image)<br>**SHT45-AD1B-R2A0/A1 humidity sensor**<br>$3–4/each<br>[link to product](link) | • High RH accuracy and long-term stability<br>• Digital I²C output simplifies PCB design (no analog conditioning)<br>• Low power operation suitable for embedded environmental nodes | • Higher cost than lower-accuracy RH sensors<br>• Requires careful placement away from heat sources for accurate readings<br>• Needs environmental protection (filter or coating) to avoid contamination drift |
| ![](image)<br>**SHT41-AD1B humidity sensor**<br>$2–3/each<br>[link to product](link) | • Good accuracy-to-cost ratio<br>• I²C interface enables simple firmware integration<br>• Compact surface-mount package | • Slightly lower performance compared to SHT45<br>• Sensitive to condensation/contamination without protection<br>• Placement airflow affects measurement accuracy |
| ![](image)<br>**HDC3022 humidity sensor**<br>$2–3.5/each<br>[link to product](link) | • High accuracy alternative supply chain to Sensirion parts<br>• I²C interface with simple integration<br>• Stable performance across wide environmental conditions | • Requires careful layout and decoupling for best accuracy<br>• Placement must minimize self-heating effects<br>• Availability may vary depending on package/SKU |


**Rationale:** A clock oscillator is easier ....

**Op-Amp**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](image)<br>**OPA333 precision op-amp**<br>$1.50/each<br>[link to product](link) | • Very low input offset voltage ideal for precision RTD current sources<br>• Zero-drift architecture provides excellent long-term stability<br>• Rail-to-rail input/output operation suitable for low-voltage systems | • Higher cost than general-purpose op-amps<br>• Limited bandwidth compared to high-speed amplifiers<br>• Slightly higher quiescent current than ultra-low-power options |
| ![](image)<br>**MCP6001 general-purpose op-amp**<br>$0.40/each<br>[link to product](link) | • Very low cost and widely available<br>• Rail-to-rail operation works well in 3.3 V systems<br>• Low power consumption suitable for battery-powered nodes | • Higher offset voltage reduces precision for RTD circuits<br>• Lower accuracy over temperature compared to precision op-amps<br>• Moderate noise performance for sensitive measurement circuits |
| ![](image)<br>**LT6015 precision op-amp**<br>$2.50/each<br>[link to product](link) | • Very low offset voltage and drift suitable for precision current generation<br>• Excellent noise performance for accurate sensor measurements<br>• Good temperature stability across wide ranges | • Higher cost than low-power devices<br>• Slightly higher power consumption<br>• May be unnecessary for moderate-accuracy environmental sensing |

**Rationale:** A clock oscillator is easier ....

**Voltage Reference IC**











**Hot-Swap I**










**Op-Amp**









**Op-Amp**








**Op-Amp**
