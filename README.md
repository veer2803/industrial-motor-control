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

Control Circuit

The control circuit contains:

Emergency stop
Stop pushbutton
Start pushbutton
Magnetic contactor
Thermal overload relay
Contactor auxiliary holding contact
Run indication
Overload indication
Control power indication
Phase indication

3. Panel General Arrangement

The panel layout translates the electrical schematic into a physical
arrangement of components inside the enclosure.

Panel Interior

The internal panel contains:

QF1 — Main protection
QF2 — Control circuit MCB
QF3 — Motor feeder protection
KM1 — Magnetic contactor
FR1 — Thermal overload relay
DIN Rail 1
DIN Rail 2
X1-X4 — Terminal blocks
Wiring duct
PE bar
Panel Door

The panel door contains:

Phase Indication
H4 — R Phase
H5 — Y Phase
H6 — B Phase
Status Indication
H1 — RUN
H2 — OVERLOAD
H3 — CONTROL POWER
Operator Controls
S2 — START
S1 — STOP
S0 — EMERGENCY STOP


