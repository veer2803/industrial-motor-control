# LV DOL Motor Control Panel Design

![Tool](https://img.shields.io/badge/Tool-QElectroTech-1F6FEB)
![Application](https://img.shields.io/badge/Application-LV%20Motor%20Control-informational)
![Supply](https://img.shields.io/badge/Supply-415V%203--Phase-FF6600)
![Motor](https://img.shields.io/badge/Motor-7.5%20kW%20Induction%20Motor-success)
![Design](https://img.shields.io/badge/Design-DOL%20Starter-blue)

A low-voltage **Direct-On-Line (DOL) motor control panel** designed using **QElectroTech**. The project covers the electrical power and control schematic along with a basic panel General Arrangement (GA) showing the physical placement of protection, switching, terminal, and operator-interface components.

The project was developed as an undergraduate electrical design project to understand the complete relationship between an electrical schematic and the physical arrangement of components inside an LV motor control panel.

---

## Table of Contents

- [Overview](#overview)
- [Electrical Schematic](#electrical-schematic)
- [Panel General Arrangement](#panel-general-arrangement)
- [Design Details](#design-details)
- [Component Functions](#component-functions)
- [Design Workflow](#design-workflow)
- [Project Files](#project-files)
- [Learning Outcomes](#learning-outcomes)

---

## Overview

The project is based on a **415 V, 3-phase, 50 Hz supply** feeding a **7.5 kW, 3-phase induction motor** through a Direct-On-Line starting arrangement.

The design consists of two main deliverables:

1. **Electrical schematic** — power circuit and control circuit for the DOL starter
2. **Panel General Arrangement** — physical arrangement of components inside the enclosure and controls mounted on the panel door

The design includes basic motor protection, contactor-based switching, thermal overload protection, emergency-stop functionality, operator controls, status indication, terminal blocks, DIN rails, wiring duct, and a protective-earth bar.

---

## Electrical Schematic

The electrical schematic represents both the **power circuit** and **control circuit** of the motor starter.

![Electrical Schematic](PASTE_YOUR_SCHEMATIC_IMAGE_LINK_HERE)

### Power Circuit

The motor power path is arranged as:

```text
415 V 3-Phase Supply
        ↓
      QF1
Main Protection
        ↓
      QF3
Motor Feeder Protection
        ↓
      KM1
Magnetic Contactor
        ↓
      FR1
Thermal Overload Relay
        ↓
       M1
7.5 kW Induction Motor
