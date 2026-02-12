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

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](image)<br>**ADR4525 precision reference**<br>$3.50/each<br>[link to product](link) | • Very low temperature drift for stable ADC measurements<br>• High initial accuracy supports consistent calibration<br>• Low noise improves precision readings | • Higher cost than basic references<br>• Requires careful PCB layout and decoupling<br>• Fixed output voltage |
| ![](image)<br>**TL431A adjustable reference**<br>$0.20/each<br>[link to product](link) | • Very inexpensive and widely available<br>• Adjustable output using external resistors<br>• Useful as reference or regulator | • Higher noise and drift<br>• Requires bias current to operate<br>• Accuracy depends on external components |
| ![](image)<br>**REF3325 precision reference**<br>$1.60/each<br>[link to product](link) | • Low quiescent current ideal for battery systems<br>• Good accuracy and low drift<br>• Compatible with many ADC ranges | • Not as low-drift as premium references<br>• Limited output current capability<br>• Requires clean layout for best performance |

**Rationale:** A clock oscillator is easier ....

**Hot-Swap I<sup>2</sup>C Buffer**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](image)<br>**TCA4311A I²C buffer**<br>$1.40/each<br>[link to product](link) | • Enables live insertion/removal of I²C devices<br>• Built-in rise-time accelerator improves signal integrity<br>• Minimal external components required | • Adds small propagation delay<br>• Must be placed near connector boundary<br>• Signal-level protection only |
| ![](image)<br>**PCA9511A I²C buffer**<br>$1.20/each<br>[link to product](link) | • Industry-standard hot-swap solution<br>• Protects bus during hot-plug events<br>• Supports standard and fast I²C modes | • Increases bus capacitance slightly<br>• Limited diagnostics<br>• Requires proper pull-up sizing |
| ![](image)<br>**LTC4300A I²C buffer**<br>$2.00/each<br>[link to product](link) | • Bus pre-charge minimizes insertion glitches<br>• Good for industrial environments<br>• Helps isolate faulty downstream devices | • Slightly higher cost<br>• Requires careful layout<br>• Additional design considerations for segmentation |

**Rationale:** A clock oscillator is easier ....

**Power Regulator**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](image)<br>**XL1509-3.3 buck regulator**<br>$1/each<br>[link to product](link) | • Simple fixed 3.3 V design<br>• Handles high input voltages<br>• Low cost | • Lower switching frequency requires larger passives<br>• Higher ripple/EMI<br>• Lower efficiency at light loads |
| ![](image)<br>**TPS62172 synchronous buck**<br>$3/each<br>[link to product](link) | • High efficiency across load range<br>• Smaller external components<br>• Cleaner output rail | • Higher cost<br>• Requires careful layout<br>• Narrower input range |
| ![](image)<br>**MP1584EN buck regulator**<br>$1.50/each<br>[link to product](link) | • Good performance for cost<br>• Smaller magnetics than older regulators<br>• Widely used design option | • EMI depends heavily on layout<br>• Variant documentation differences<br>• Not ultra-low-noise |


**Rationale:** A clock oscillator is easier ....

**MOSFET Options**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](image)<br>**AO3407A P-MOSFET**<br>$0.30/each<br>[link to product](link) | • Low Rds(on) for efficient switching<br>• Compact SOT-23 package<br>• Common high-side switching device | • Limited current handling<br>• Thermal limits of small package<br>• Gate-drive margin must be verified |
| ![](image)<br>**SI2301CDS P-MOSFET**<br>$0.40/each<br>[link to product](link) | • Good balance of cost and performance<br>• Widely available<br>• Suitable for 3.3 V and 5 V switching | • Slightly higher Rds(on)<br>• Limited dissipation capability<br>• Requires gate resistor design |
| ![](image)<br>**DMG2305UX P-MOSFET**<br>$0.50/each<br>[link to product](link) | • Very low on-resistance<br>• Compact package<br>• Good for moderate current switching | • Thermal limitations<br>• Gate-threshold must be checked<br>• Slightly higher cost |

**Rationale:** A clock oscillator is easier ....








