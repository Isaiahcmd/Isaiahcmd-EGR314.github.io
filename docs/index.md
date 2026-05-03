---
title: Welcome
tags:
- tag1
- tag2
---
<center>
<font size= "6">Isaiah Johnston Datasheet</font><br>
as part of<br>
<font size= "8"> Temperature / Humidity Module</font><br>
for<br>
<font size= "5"> Team 202 </font><br>
<font size= "5"> S.C.O.U.T.S </font><br>
<font size= "5"> *Super Cool Original and Unique Technology Systems*</font>font><br>

**Submission: January, 13, 2026**
</center>

## Introduction

This data sheet exists to describe the design and function of the temperature / humidity module subsystem.

### Project Summary

This subsystem existes to allow users to remotely observe soil temperature and relative humidity levels as part of the CropScout exploritory drone.
A link to the full product report can be found [here.](https://EGR314-S-2026-202.github.io)
The Cropscout prototype, as it stands now, has a fully functioning robotic 3 degree of freedom arm with a tempurature probe end effector.
The body of the rover houses an ambient humidity sensor, and the PCB's and the motors. 
All data is sent via wifi to an MQTT server where it is recivied by the human machine interface (HMI). 
Commands can be given by the HMI and recieved by the sensors and motor control units in the same manner.
The motors have partial functionality and the broadcast message gets stuck in the motor PCB at this point in time. 
The issue is suspected to be in the software of the motor PCB. 
More work will have to be done to achive full functionality.
The metal detecting subsystem is currently fully non functional but showed base line funtionality in early testing. A complete redesign of the subsystem is needed.
The pressure sensing subsystem was never created, a complete redesign and testing will be needed to integrate it.
Noise was an issue for the sensors, occasionally a corrupted character will make it into the string recieved by the HMI.
The soil tempurature probe needs a more thorough calibration.
It is recomended the probe be submerged in ice water for 10 minutes and the temperature be set at 0°C then submerged in boiling water and the temperature be set at 100°C.
The temurature subsystem has noise in the line and requires some smoothing by hardware changes, software smothing or a combination. 

### My Contribution

This subsystem is responsible for providing the user with soil temperature and ambient reletive humidity data.

*To veiw the block diagram of this subsystem for information on the general layout of this subsystem click ["here".](https://isaiahcmd.github.io/Isaiahcmd-EGR314.github.io/02-Block-Diagram/Block-Diagram/)

*To view the component selection process of this subsystem click ["here".](https://isaiahcmd.github.io/Isaiahcmd-EGR314.github.io/03-Component-Selection/Component-Selection/)

*To view the microcontroller selection process of this subsystem click ["here".](https://isaiahcmd.github.io/Isaiahcmd-EGR314.github.io/04-Microcontroller-Selection/Microcontroller-Selection/)

*To view the power budget of this subsystem click ["here".](https://isaiahcmd.github.io/Isaiahcmd-EGR314.github.io/05-Power-Budget/Power-Budget/)

*To veiw the bill of materials of this subsystem for information on materials and parts click ["here".](https://isaiahcmd.github.io/Isaiahcmd-EGR314.github.io/06-BOM/BOM/)

*To view schematic of this subsystem click [here](https://isaiahcmd.github.io/Isaiahcmd-EGR314.github.io/07-Schematic/schematic/)

*To view the ECAD PCB for this subsystem click ["here".]([https://isaiahcmd.github.io/Isaiahcmd-EGR314.github.io/02-Block-Diagram/Block-Diagram/])

*To look at personal reflections on this subsystem and the processes that went into its creation click ["here".]([https://isaiahcmd.github.io/Isaiahcmd-EGR314.github.io/02-Block-Diagram/Block-Diagram/])

*To vie the API for this subsystem click ["here".](https://isaiahcmd.github.io/Isaiahcmd-EGR314.github.io/10-API/API/)


