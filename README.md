# LV DOL Motor Control Panel Design

![Tool](https://img.shields.io/badge/Tool-QElectroTech-blue)
![Application](https://img.shields.io/badge/Application-LV%20Motor%20Control-orange)
![System](https://img.shields.io/badge/System-DOL%20Motor%20Starter-green)
![Power](https://img.shields.io/badge/Power-415V%203--Phase-lightgrey)

A low-voltage **Direct-On-Line (DOL) motor control panel** designed using
**QElectroTech**.

The project demonstrates the complete basic electrical design workflow from
power and control schematic development to physical panel layout,
component identification, and Bill of Materials preparation.

---

# 1. Overview

This project represents a **415 V, 3-phase, 50 Hz motor control panel**
used to operate a **7.5 kW three-phase induction motor** using a
Direct-On-Line starting method.

The project consists of:

- Electrical power schematic
- Electrical control schematic
- Panel General Arrangement
- Component identification
- Bill of Materials
- Protection and control logic

The objective was to develop practical understanding of **LV electrical
panel design, motor protection, control circuits, electrical CAD and panel
component arrangement**.

---

# 2. Electrical Schematic

The electrical schematic represents the power and control circuitry of
the DOL motor starter.

## Power Circuit

The main power path is:

```text
415 V 3-Phase Supply
        |
        v
       QF1
Main Protection
        |
        v
       QF3
Motor Protection
        |
        v
       KM1
Magnetic Contactor
        |
        v
       FR1
Thermal Overload
        |
        v
       M1
7.5 kW Induction Motor
