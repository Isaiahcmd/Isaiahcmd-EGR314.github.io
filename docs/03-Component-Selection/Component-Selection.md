---
title: Module's Selected Major Components
---

## Module's Selected Major Components

The following sections are the selected major components necessary for  .....

>**For each of the following sections, use <ins>one of the two styles</ins> given near the end. *REMOVE THIS NOTE***

### Power Regulator

(**remove this note/placeholder**: this is where your 3.3 volt switching regulator, any other needed power regulator, and power source {if applicable} **THAT WERE SELECTED**)


### Tempurature Sensor



### Humidity Sensor

### Op-Amp

### Voltage Reference IC

### Hot-Swap I<sup>2</sup>C Buffer

### MOSFET

### Precision Resistor

### Barrel Jack

### 8-Pin Connector

-----------

**Humidity Sensor**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![image](SHT45.png)<br>**SHT45-AD1B-R2A0/A1 humidity sensor**<br>$5.54/each<br>[link](https://www.digikey.com/en/products/detail/sensirion-ag/SHT45-AD1B-R2/16360969?gclsrc=aw.ds&gad_source=4&gad_campaignid=20232005509&gbraid=0AAAAADrbLlhvjO3S2T4wJVM4nKnQCtGe4&gclid=CjwKCAiAkbbMBhB2EiwANbxtbR30zFlR6-ISnKVzKA9TfFOxo3CsswTxviwWlwFFxJSoi6N8-PF84hoCQ5cQAvD_BwE) | • High RH accuracy and long-term stability<br>• Digital I²C output simplifies PCB design (no analog conditioning)<br>• Low power operation suitable for embedded environmental nodes | • Higher cost than lower-accuracy RH sensors<br>• Requires careful placement away from heat sources for accurate readings<br>• Needs environmental protection (filter or coating) to avoid contamination drift |
| ![image](SHT.png)<br>**SHT41-AD1B humidity sensor**<br>$2.84/each<br>[link](https://www.digikey.com/en/products/detail/sensirion-ag/SHT41-AD1B-R3/15296599) | • Good accuracy-to-cost ratio<br>• I²C interface enables simple firmware integration<br>• Compact surface-mount package | • Slightly lower performance compared to SHT45<br>• Sensitive to condensation/contamination without protection<br>• Placement airflow affects measurement accuracy |
| ![image](HDC.png)<br>**HDC2080 humidity sensor**<br>$1.94/each<br>[link](https://www.digikey.com/en/products/detail/texas-instruments/HDC2080DMBR/9860135?gclsrc=aw.ds&gad_source=4&gad_campaignid=20232005509&gbraid=0AAAAADrbLlhvjO3S2T4wJVM4nKnQCtGe4&gclid=CjwKCAiAkbbMBhB2EiwANbxtbY5duiewVzGNgl5dhdKb6f7xtAyPZq1Vo0maRoVvSNwXd1f-4QeO-RoCcEMQAvD_BwE) | • High accuracy alternative supply chain to Sensirion parts<br>• I²C interface with simple integration<br>• Stable performance across wide environmental conditions | • Requires careful layout and decoupling for best accuracy<br>• Placement must minimize self-heating effects<br>• Availability may vary depending on package/SKU |


**Rationale:** A clock oscillator is easier ....

**Op-Amp**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![image](OPA333.png)<br>**OPA333 precision op-amp**<br>$2.82/each<br>[link](https://www.digikey.com/en/products/detail/texas-instruments/OPA333AIDBVT/1004627)) | • Very low input offset voltage ideal for precision RTD current sources<br>• Zero-drift architecture provides excellent long-term stability<br>• Rail-to-rail input/output operation suitable for low-voltage systems | • Higher cost than general-purpose op-amps<br>• Limited bandwidth compared to high-speed amplifiers<br>• Slightly higher quiescent current than ultra-low-power options |
| ![image](MCP6002.png)<br>**MCP6001 general-purpose op-amp**<br>$0.40/each<br>[link](https://www.digikey.com/en/products/detail/microchip-technology/MCP6001T-E-OT/1979833?gclsrc=aw.ds&gad_source=4&gad_campaignid=20228387720&gbraid=0AAAAADrbLlhNtrIkwPp0OiJmv8l7g3KB3&gclid=CjwKCAiAkbbMBhB2EiwANbxtbXV5fqL9M9kqF_H6gamELeyg9kteB0eufRAYaOHZXDlToHE7oz6ajRoCPDAQAvD_BwE)) | • Very low cost and widely available<br>• Rail-to-rail operation works well in 3.3 V systems<br>• Low power consumption suitable for battery-powered nodes | • Higher offset voltage reduces precision for RTD circuits<br>• Lower accuracy over temperature compared to precision op-amps<br>• Moderate noise performance for sensitive measurement circuits |
| ![image](LT6015.png)<br>**LT6015 precision op-amp**<br>$2.50/each<br>[link](https://www.digikey.com/en/products/detail/analog-devices-inc/LT6015HS5-TRPBF/8040793) | • Very low offset voltage and drift suitable for precision current generation<br>• Excellent noise performance for accurate sensor measurements<br>• Good temperature stability across wide ranges | • Higher cost than low-power devices<br>• Slightly higher power consumption<br>• May be unnecessary for moderate-accuracy environmental sensing |

**Rationale:** A clock oscillator is easier ....

**Voltage Reference IC**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![image](ADR.png)<br>**ADR4525 precision reference**<br>$10.55/each<br>[link](https://www.digikey.com/en/products/detail/analog-devices-inc/ADR4525BRZ-R7/4141690) | • Very low temperature drift for stable ADC measurements<br>• High initial accuracy supports consistent calibration<br>• Low noise improves precision readings | • Higher cost than basic references<br>• Requires careful PCB layout and decoupling<br>• Fixed output voltage |
| ![image](TL4.png)<br>**TL431A adjustable reference**<br>$0.10/each<br>[link](https://www.digikey.com/en/products/detail/evvo/TL431A/21406979) | • Very inexpensive and widely available<br>• Adjustable output using external resistors<br>• Useful as reference or regulator | • Higher noise and drift<br>• Requires bias current to operate<br>• Accuracy depends on external components |
| ![image](REF.png)<br>**REF3325 precision reference**<br>$2.18/each<br>[link](https://www.digikey.com/en/products/detail/texas-instruments/REF3325AIRSER/5034447) | • Low quiescent current ideal for battery systems<br>• Good accuracy and low drift<br>• Compatible with many ADC ranges | • Not as low-drift as premium references<br>• Limited output current capability<br>• Requires clean layout for best performance |

**Rationale:** A clock oscillator is easier ....

**Hot-Swap I<sup>2</sup>C Buffer**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![image](TCA4.png)<br>**TCA4311A I²C buffer**<br>$3.08/each<br>[link](https://www.digikey.com/en/products/detail/texas-instruments/TCA4311ADR/2816461) | • Enables live insertion/removal of I²C devices<br>• Built-in rise-time accelerator improves signal integrity<br>• Minimal external components required | • Adds small propagation delay<br>• Must be placed near connector boundary<br>• Signal-level protection only |
| ![image](PCA.png)<br>**PCA9511A I²C buffer**<br>$2.72/each<br>[link](https://www.digikey.com/en/products/detail/nxp-usa-inc/PCA9511AD,118/7649058) | • Industry-standard hot-swap solution<br>• Protects bus during hot-plug events<br>• Supports standard and fast I²C modes | • Increases bus capacitance slightly<br>• Limited diagnostics<br>• Requires proper pull-up sizing |
| ![image](LTC.png)<br>**LTC4300A I²C buffer**<br>$7.20/each<br>[link](https://www.digikey.com/en/products/detail/analog-devices-inc/LTC4300A-1IMS8-PBF/961339) | • Bus pre-charge minimizes insertion glitches<br>• Good for industrial environments<br>• Helps isolate faulty downstream devices | • Slightly higher cost<br>• Requires careful layout<br>• Additional design considerations for segmentation |

**Rationale:** A clock oscillator is easier ....

**Power Regulator**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![image](XL.png)<br>**XL1509-3.3 buck regulator**<br>$0.61/each<br>[link](https://www.digikey.com/en/products/detail/umw/XL1509-3.3/24889882?gclsrc=aw.ds&gad_source=4&gad_campaignid=21136823955&gbraid=0AAAAADrbLlghOQE-IwtSJAmaimMc3CB8-&gclid=CjwKCAiAkbbMBhB2EiwANbxtbUOFY1vp_WfZm_yfzUVH2KgDYfhga_t4X1uMC_d3urPPxXmPd3xWThoCNoUQAvD_BwE) | • Simple fixed 3.3 V design<br>• Handles high input voltages<br>• Low cost | • Lower switching frequency requires larger passives<br>• Higher ripple/EMI<br>• Lower efficiency at light loads |
| ![image](TPS.png)<br>**TPS62172 synchronous buck**<br>$1.67/each<br>[link](https://www.digikey.com/en/products/detail/texas-instruments/TPS62172DSGT/2781002) | • High efficiency across load range<br>• Smaller external components<br>• Cleaner output rail | • Higher cost<br>• Requires careful layout<br>• Narrower input range |
| ![image](MP1.png)<br>**MP1584EN buck regulator**<br>$2.75/each<br>[link](https://www.digikey.com/en/products/detail/monolithic-power-systems-inc/MP1584EN-LF-Z/9433299?gclsrc=aw.ds&gad_source=4&gad_campaignid=20228387720&gbraid=0AAAAADrbLlhNtrIkwPp0OiJmv8l7g3KB3&gclid=CjwKCAiAkbbMBhB2EiwANbxtbfMqG_6BKipHHG9ByxxlYfOU-f1pC9xHJrSH__PS0RDB2rjvrCsWCBoCJawQAvD_BwE) | • Good performance for cost<br>• Smaller magnetics than older regulators<br>• Widely used design option | • EMI depends heavily on layout<br>• Variant documentation differences<br>• Not ultra-low-noise |


**Rationale:** A clock oscillator is easier ....

**MOSFET**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![image](AO34.png)<br>**AO3407A P-MOSFET**<br>$0.46/each<br>[link](https://www.digikey.com/en/products/detail/alpha-omega-semiconductor-inc/AO3407A/1855778) | • Low Rds(on) for efficient switching<br>• Compact SOT-23 package<br>• Common high-side switching device | • Limited current handling<br>• Thermal limits of small package<br>• Gate-drive margin must be verified |
| ![image](SI2.png)<br>**SI2301CDS P-MOSFET**<br>$0.71/each<br>[link](https://www.digikey.com/en/products/detail/vishay-siliconix/SI2301CDS-T1-E3/2622018) | • Good balance of cost and performance<br>• Widely available<br>• Suitable for 3.3 V and 5 V switching | • Slightly higher Rds(on)<br>• Limited dissipation capability<br>• Requires gate resistor design |
| ![image](DMG.png)<br>**DMG2305UX P-MOSFET**<br>$0.30/each<br>[link](https://www.digikey.com/en/products/detail/diodes-incorporated/DMG2305UX-13/4251560?gclsrc=aw.ds&gad_source=1&gad_campaignid=120565755&gbraid=0AAAAADrbLljXIHCKJ57NJE_aqn3jKNSxh&gclid=CjwKCAiAkbbMBhB2EiwANbxtbXC-tmLpWw26TxszAiIrTx22b1P-vNTs2F-fxqSELN_cH8ikjKX3dxoCvEUQAvD_BwE) | • Very low on-resistance<br>• Compact package<br>• Good for moderate current switching | • Thermal limitations<br>• Gate-threshold must be checked<br>• Slightly higher cost |

**Rationale:** A clock oscillator is easier ....

**Temperature Sensor**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![image](PT1000.png)<br>**PT1000 Temperature Sensor Probe (1597-314010819-ND)**<br>$9.90/each<br>[link](https://www.digikey.com/en/products/detail/seeed-technology-co-ltd/314010819/22109375) | • Very high accuracy and long-term stability<br>• Excellent repeatability<br>• Wide temperature range (−200°C to 600°C)<br>• Easy calibration | • Requires precision current source<br>• More expensive than thermistors or digital sensors<br>• Wiring resistance must be compensated |
| ![image](DIGTHERMO.png)<br>**Digital Temperature Probe (SNS-TMP-DS18B20-MAXIM)**<br>$5.33/each<br>[link](https://www.digikey.com/en/products/detail/olimex-ltd/SNS-TMP-DS18B20-MAXIM/21662296?gclsrc=aw.ds&gad_source=1&gad_campaignid=20232005509&gbraid=0AAAAADrbLlhKGd9mOEygGzPFra-ui8Jij&gclid=CjwKCAiAkbbMBhB2EiwANbxtbbnKocjkgMGM6IwTZ5IB_zNq7v1d6wnbXuzygucdvPiQ-Pm-fBRvqBoCbOIQAvD_BwE) | • Simple PCB interface<br>• No precision analog circuitry required<br>• Factory calibrated | • Slower response time than exposed RTD<br>• Accuracy lower than PT1000<br>• Less stable long-term |
| ![image](NTC.png)<br>**THERM NTC 10KOHM 3988K Probe (B57800K0103A001)**<br>$5.22/each<br>[link](https://www.digikey.com/en/products/detail/epcos-tdk-electronics/B57800K0103A001/7099969) | • Least expensive<br>• High sensitivity<br>• Simple voltage divider readout | • Non-linear resistance, needs calibration<br>• Accuracy depends heavily on calibration<br>• Self-heating errors if measurement current is too high |

**Rationale**

**Precision Resistor**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![image](THINFILM.png)<br>**PATT0603E1002BGT1 thin-film resistor**<br>$0.82/each<br>[link](https://www.digikey.com/en/products/detail/vishay-dale-thin-film/PATT0603E1002BGT1/4307888) | • High precision tolerance (0.1%) suitable for sensor reference networks<br>• Good temperature stability (10–25 ppm/°C) for consistent measurements<br>• Compact 0603 SMD package ideal for small PCB layouts | • Lower power handling compared to larger package resistors<br>• More expensive than standard thick-film resistors<br>• Long-term drift is higher than ultra-precision metal-foil resistors |
| ![image](VPGFOIL.png)<br>**Y145310K0000T9L metal foil resistor**<br>$40.63/each<br>[link](https://www.digikey.com/en/products/detail/vpg-foil-resistors/Y145310K0000T9L/1888099) | • Extremely high precision (0.01% tolerance)<br>• Very low temperature coefficient (~2 ppm/°C) for highly stable measurements<br>• Excellent long-term stability and minimal drift | • Significantly more expensive than thin-film precision resistors<br>• Larger footprint compared to standard SMD thin-film resistors<br>• Performance benefits may exceed requirements for typical embedded sensor applications |
| ![image](RC0603.png)<br>**RC0603BR-0710KL thin-film resistor**<br>$0.10/each<br>[link](https://www.digikey.com/en/products/detail/yageo/RC0603FR-0710KL/726880) | • Low cost while maintaining 0.1% precision tolerance<br>• Good temperature stability (~25 ppm/°C) suitable for sensor reference networks<br>• Small SMD package ideal for compact PCB layouts | • Moderate long-term drift compared to metal-foil precision resistors<br>• Limited power dissipation due to small 0603 package<br>• Accuracy can be affected by PCB thermal gradients if placed near heat sources |

**Rationale**

**Barrel Jack**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![image](102A.png)<br>**PJ-102A barrel jack**<br>$0.59/each<br>[link](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices/PJ-102A/275425?gclsrc=aw.ds&gad_source=1&gad_campaignid=120565755&gbraid=0AAAAADrbLljXIHCKJ57NJE_aqn3jKNSxh&gclid=CjwKCAiAkbbMBhB2EiwANbxtbQ4bqXD_DcC_vtQ_a9KpprJgPE6ocemjFjgkedDVRx50j8IXPc3cxxoC0EYQAvD_BwE) | • Very common connector footprint<br>• Through-hole mounting provides strong mechanical stability<br>• Suitable for moderate current DC input | • Larger footprint than smaller connectors<br>• Not sealed against moisture or debris<br>• Limited retention strength compared to locking connectors |
| ![image](037A.png)<br>**PJ-037A barrel jack**<br>$0.60/each<br>[link](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices-/PJ-037A/1644545) | • Compact form factor<br>• Good mechanical anchoring for PCB mounting<br>• Widely available from multiple vendors | • Slightly lower current rating<br>• Reduced robustness under repeated insertion cycles<br>• Requires enclosure support |
| ![image](002A.png)<br>**CUI PJ-002A barrel jack**<br>$0.47/each<br>[link](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices-/PJ-002A/96962?gclsrc=aw.ds&gad_source=4&gad_campaignid=21016330783&gbraid=0AAAAADrbLlhJ4EBBDmQ1gvd8Snk-2l5yC&gclid=CjwKCAiAkbbMBhB2EiwANbxtbTGqU1Yb9pn2fjE5OupA7STVYf9jZ6BFDZZLidFZGeqfxTAWCCCqghoCmEcQAvD_BwE) | • Reliable manufacturer support and documentation<br>• Strong PCB retention due to through-hole mounting<br>• Compatible with standard 5.5 mm / 2.1 mm plugs | • Larger PCB area required<br>• No built-in locking mechanism<br>• Exposed contacts can collect dust/moisture |

**Rationale**

**8-Pin Connector**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![image](B8B.png)<br>**JST XH B8B-XH-A connector**<br>$0.25/each<br>[link](https://www.digikey.com/en/products/detail/jst-sales-america-inc/B8B-XH-A/1651049) | • Locking friction ramp improves retention<br>• Widely available and easy to assemble<br>• Good for low-cost sensor harnesses | • Larger PCB footprint<br>• Not sealed for outdoor environments<br>• Limited current rating per pin |
| ![image](613.png)<br>**61300811121 right-angle header**<br>$0.36/each<br>[link](https://www.digikey.com/en/products/detail/w%C3%BCrth-elektronik/61300811121/4846839) | • Simple, robust, easy to source<br>• Compatible with standard jumper wires<br>• Low vertical height in enclosures | • No locking mechanism<br>• Not suitable for vibration environments<br>• Exposed pins susceptible to corrosion |
| ![image](BM08B.png)<br>**JST GH BM08B-GHS-TBT connector**<br>$0.49/each<br>[link](https://www.digikey.com/en/products/detail/jst-sales-america-inc/BM08B-GHS-TBT/807852?gclsrc=aw.ds&gad_source=1&gad_campaignid=21016330783&gbraid=0AAAAADrbLlh9Msrnae-w7zvd5ktUciy2m&gclid=CjwKCAiAkbbMBhB2EiwANbxtbSY4wgHuoP6F8DNXTThv02R2RNWKHdS9iZEAluDFsUB5ZWFAyBkkgRoC06YQAvD_BwE) | • Compact footprint saves PCB space<br>• Positive latch improves vibration resistance<br>• Good for production harnesses | • Requires specialized crimp tools<br>• Harder to hand-solder due to fine pitch<br>• Not sealed without additional protection |








