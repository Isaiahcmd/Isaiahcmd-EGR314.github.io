---
title: Tempurature/Humidity API
---

## Overview
This page exists to describe the aplication programing interface of the temperature/humididty subsystem. 
Described will be which messages will be read and sent by the subsystem, and how messages not meant for this subsystem will be handeled.

## Recieved Messages

### Message: Broadcast (X) Start TYPE 1

Used by HMI to initialize all systems and ensure board to board communication.

| Field           | Bytes | Variable Name   | Type (Protocol / Code) | Min Recognized | Max Recognized | Example |
|----------------|------:|-----------------|------------------------|----------------|----------------|---------|
| Variable Token | 1     | X               | char                   | X              | X              | X       |
| Separator      | 1     | :               | char                   | :              | :              | :       |
| Type Identifier| 2     | unit_type       | char (`ST`)            | ST             | ST             | ST      |
| Separator      | 1     | :               | char                   | :              | :              | :       |
| Value          | 4     | Start           | char                   | Start          | Start          | Start   |
| Terminator     | 1     | ;               | char                   | ;              | ;              | ;       |

**Total Message Data Bytes:** 10

**Valid Example Packet:**  
`AZhX:ST:Start;YB`

**Meaning:**  
-`X` = Broadcast to everyone
-`ST` = Start: blink LED

### Message: Change Temperature Unit (CU) TYPE 6

Used to change the temperature unit used by the Temp/Humidity subsystem.

| Field           | Bytes | Variable Name   | Type (Protocol / Code) | Min Recognized | Max Recognized | Example |
|----------------|------:|-----------------|------------------------|----------------|----------------|---------|
| Variable Token | 2     | CU              | char[2]                | CU             | CU             | CU      |
| Separator      | 1     | :               | char                   | :              | :              | :       |
| Type Identifier| 1     | unit_type       | char (`S`)             | S              | S              | S       |
| Separator      | 1     | :               | char                   | :              | :              | :       |
| Value          | 1     | requested_unit  | char                   | C              | F              | F       |
| Terminator     | 1     | ;               | char                   | ;              | ;              | ;       |

**Total Message Data Bytes:** 7

**Valid Example Packet:**  
`AZhtCU:S:F;YB`

**Meaning:**  
- `h` = HMI  
- `t` = Temp/Humidity subsystem  
- `CU` = change unit  
- `S` = string type  
- `F` = Fahrenheit

### Message: Request Temperature (RT) TYPE 6

Used by the HMI to request the current processed temperature reading.

| Field           | Bytes | Variable Name   | Type (Protocol / Code) | Min Recognized | Max Recognized | Example |
|----------------|------:|-----------------|------------------------|----------------|----------------|---------|
| Variable Token | 2     | TR              | char[2]                | TR             | TR             | TR      |
| Separator      | 1     | :               | char                   | :              | :              | :       |
| Type Identifier| 1     | request_type    | char (`S`)             | S              | S              | S       |
| Separator      | 1     | :               | char                   | :              | :              | :       |
| Value          | 1     | request_value   | char                   | T              | T              | T       |
| Terminator     | 1     | ;               | char                   | ;              | ;              | ;       |

**Total Message Data Bytes:** 7

**Valid Example Packet:**  
`AZhtTR:S:T;YB`

**Meaning:**  
- `TR` = request temperature  
- `T` = temperature requested

### Message: Request Humidity (RH) TYPE 6

Used by the HMI to request the current processed humidity reading.

| Field           | Bytes | Variable Name   | Type (Protocol / Code) | Min Recognized | Max Recognized | Example |
|----------------|------:|-----------------|------------------------|----------------|----------------|---------|
| Variable Token | 2     | RH              | char[2]                | RH             | RH             | RH      |
| Separator      | 1     | :               | char                   | :              | :              | :       |
| Type Identifier| 1     | request_type    | char (`S`)             | S              | S              | S       |
| Separator      | 1     | :               | char                   | :              | :              | :       |
| Value          | 1     | request_value   | char                   | H              | H              | H       |
| Terminator     | 1     | ;               | char                   | ;              | ;              | ;       |

**Total Message Data Bytes:** 7

**Valid Example Packet:**  
`AZhtRH:S:H;YB`

**Meaning:**  
- `RH` = request humidity  
- `H` = humidity requested

## Sent Messages

### Message: Temperature Reading (TR + TT) TYPE 6

Used to send the current processed PT1000 temperature and the current temperature unit.

| Field           | Bytes | Variable Name      | Type (Protocol / Code) | Min Recognized | Max Recognized | Example |
|----------------|------:|--------------------|------------------------|----------------|----------------|---------|
| Variable Token | 2     | TR                 | char[2]                | TR             | TR             | TR      |
| Separator      | 1     | :                  | char                   | :              | :              | :       |
| Type Identifier| 1     | temperature_type   | char (`F`)             | F              | F              | F       |
| Separator      | 1     | :                  | char                   | :              | :              | :       |
| Value          | 1-7   | temperature_value  | ASCII float / `float`  | -50.0          | 200.0          | 75.256  |
| Terminator     | 1     | ;                  | char                   | ;              | ;              | ;       |
| Variable Token | 2     | TT                 | char[2]                | TT             | TT             | TT      |
| Separator      | 1     | :                  | char                   | :              | :              | :       |
| Type Identifier| 1     | unit_type          | char (`S`)             | S              | S              | S       |
| Separator      | 1     | :                  | char                   | :              | :              | :       |
| Value          | 1     | temperature_unit   | char                   | C              | F              | F       |
| Terminator     | 1     | ;                  | char                   | ;              | ;              | ;       |

**Total Message Data Bytes (example shown):** 19

**Valid Example Packet:**  
`AZthTR:F:75.256;TT:S:F;YB`

**Meaning:**  
- `t` = Temp/Humidity subsystem  
- `h` = HMI  
- `TR` = temperature reading  
- `F` = float type  
- `75.256` = current temperature value  
- `TT` = temperature type/unit  
- `S` = string type  
- `F` = Fahrenheit

### Message: Humidity Reading (HR) TYPE 6

Used to send the current processed humidity reading.

| Field           | Bytes | Variable Name    | Type (Protocol / Code) | Min Recognized | Max Recognized | Example |
|----------------|------:|------------------|------------------------|----------------|----------------|---------|
| Variable Token | 2     | HR               | char[2]                | HR             | HR             | HR      |
| Separator      | 1     | :                | char                   | :              | :              | :       |
| Type Identifier| 1     | humidity_type    | char (`F`)             | F              | F              | F       |
| Separator      | 1     | :                | char                   | :              | :              | :       |
| Value          | 1-6   | humidity_value   | ASCII float / `float`  | 0.0            | 100.0          | 43.5    |
| Terminator     | 1     | ;                | char                   | ;              | ;              | ;       |

**Total Message Data Bytes (example shown):** 10

**Valid Example Packet:**  
`AZthHR:F:43.5;YB`

**Meaning:**  
- `HR` = humidity reading  
- `43.5` = current humidity value
