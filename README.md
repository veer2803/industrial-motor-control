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

## Schematic

The schematic shows the complete electrical and control circuit for the LV motor control panel, including incoming protection, motor protection, contactor control, overload protection, indication lamps, start/stop controls and emergency stop.

![LV Motor Control Schematic](schematic.png)

---

## Panel Layout

The panel layout shows the physical arrangement of the main components inside the enclosure, including DIN rails, protective devices, contactor, overload relay, terminal blocks, wiring duct, PE bar and door-mounted controls and indicators.

![LV Motor Control Panel Layout](panel_layout.png)

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


```
The three-phase supply is switched by the magnetic contactor KM1.

QF1 provides incoming protection and isolation, while QF3 provides protection for the motor feeder.

FR1 provides thermal overload protection for the motor.

Control Circuit

The control circuit contains:
```
Control Supply
      |
      v
Emergency Stop (S0 - NC)
      |
      v
Stop Pushbutton (S1 - NC)
      |
      v
Overload Contact (FR1 - NC)
      |
      v
Start Pushbutton (S2 - NO)
      |
      v
KM1 Contactor Coil
      |
      v
Control Return


```
An auxiliary contact of KM1 is used as a self-holding/seal-in contact.

The basic control logic is:
```
START pressed
      |
      v
KM1 coil energizes
      |
      v
KM1 main contacts close
      |
      v
Motor receives 3-phase supply
      |
      v
KM1 auxiliary contact maintains coil energization
      |
      v
Motor continues running

```
The motor stops when:
```
STOP pressed
       OR
EMERGENCY STOP pressed
       OR
THERMAL OVERLOAD TRIPS
       |
       v
KM1 coil de-energizes
       |
       v
Main contacts open
       |
       v
Motor disconnected
```

3. Panel General Arrangement

The panel layout translates the electrical schematic into a physical
arrangement of components inside the enclosure.

Panel Interior

The internal panel contains:
```
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

```
Panel Door
The panel door contains the operator controls and indication devices.

The panel door contains:
```
Phase Indication
H4 — R Phase
H5 — Y Phase
H6 — B Phase
```

Status Indication
```
H1 — RUN
H2 — OVERLOAD
H3 — CONTROL POWER
```
Operator Controls
```
S2 — START
S1 — STOP
S0 — EMERGENCY STOP
```

Bill of Materials

The following project-level Bill of Materials identifies the major components represented in the schematic and panel layout.
```
No.	Tag	Component	                      Qty.
1	QF1	Main Protective Device	               1
2	QF2	Control Circuit MCB	               1
3	QF3	Motor Circuit MCB	               1
4	KM1	Magnetic Contactor	               1
5	FR1	Thermal Overload Relay                 1
6	M1	7.5 kW Three-Phase Induction Motor     1
7	S0	Emergency Stop Pushbutton	       1
8	S1	Stop Pushbutton	                       1
9	S2	Start Pushbutton	               1
10	H1	RUN Indicator	                       1
11	H2	OVERLOAD Indicator	               1
12	H3	CONTROL POWER Indicator        	       1
13	H4	R Phase Indicator	               1
14	H5	Y Phase Indicator	               1
15	H6	B Phase Indicator	               1
16	X1-X4	Terminal Blocks	                       4
17	-	DIN Rails	                       2
18	-	Wiring Duct	                     1 Set
19	-	PE Bar                           	1
20	-	Panel Enclosure	                        1

```
