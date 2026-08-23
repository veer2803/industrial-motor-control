# Industrial Motor Control System

![Tool](https://img.shields.io/badge/Tool-AutoCAD_Electrical-0696D7?logo=autodesk&logoColor=white)
![Motors](https://img.shields.io/badge/Motors-14-informational)
![Phases](https://img.shields.io/badge/Power-Three--Phase-FF6600)
![License](https://img.shields.io/badge/License-MIT-green)

A multi-motor industrial control system designed in **AutoCAD Electrical**, modeled after a water treatment plant. The project covers the full design workflow: ladder schematic, control panel layout, and an auto-generated Bill of Materials.

---

## Table of Contents

- [Overview](#overview)
- [Schematic](#schematic)
- [Panel Layout](#panel-layout)
- [Bill of Materials](#bill-of-materials)
- [Design Details](#design-details)
- [File Structure](#file-structure)
- [License](#license)

---

## Overview

The system controls 14 three-phase motors, each representing a distinct process function in a water treatment plant–style facility. The design was built entirely within AutoCAD Electrical, taking advantage of its intelligent schematic tools: ladder references, multi-phase power buses, net labeling, component tagging with Xdata, balloon annotations, and automated BOM generation directly from the panel layout.

The project is organized into three deliverables that mirror a real engineering workflow:

1. **Schematic** — the control logic and wiring for all motors
2. **Panel layout** — the physical arrangement of hardware inside the enclosure
3. **BOM report** — a complete component list generated from the layout

---

## Schematic

The schematic is drawn as a multi-sheet ladder diagram structured around multi-phase power buses. Each motor branch includes a 3-pole thermal circuit breaker, contactor, overload relay, and terminal connections. Net labels and ladder references are used throughout to keep the sheets readable and cross-referenceable.

<img width="2770" height="1873" alt="schematic" src="https://github.com/user-attachments/assets/53e0d291-b614-4551-b673-4f957ea6733d" />


Key elements documented in the schematic:

- **14 three-phase motors**, each on a dedicated branch
- **3-pole thermal circuit breakers** for overcurrent protection on each branch
- **Contactors and overload relays** for motor switching and thermal protection
- **Multi-phase power buses** running across sheets
- **Terminal blocks** for field wiring connections
- **Ladder references** linking control and power sections across sheets

---

## Panel Layout

The panel layout defines the physical placement of all hardware inside the control enclosure. Components are arranged on DIN rails with defined spacing, and balloon annotations tie each physical component back to its reference in the schematic. Xdata visibility is enabled so that component tags are embedded in the drawing and available for automated reporting.

<img width="2696" height="1821" alt="panel" src="https://github.com/user-attachments/assets/bbfe786c-16cd-47f0-8fdd-8a51ba15091a" />


Hardware placed in the panel:

- DIN rails (35 mm × 7.5 mm)
- Terminal blocks
- Contactors / relays (4-pole DC coil)
- PLC — ControlLogix 5580 processor
- PLC I/O modules — digital input (24 VDC) and digital output (12/24 VDC)
- PLC communication module — Ethernet
- PLC power supply modules
- Wire ducts (slotted, PVC)

---

## Bill of Materials

The BOM was generated directly from the panel layout using AutoCAD Electrical's reporting tools. It documents each component's catalog number, manufacturer, quantity, and description.

<img width="1528" height="1461" alt="panel_bom" src="https://github.com/user-attachments/assets/163c16f6-a396-4fe2-b912-e38113706b13" />

---

## Design Details

### Workflow

This project was built using the standard AutoCAD Electrical design workflow:

1. **Project setup** — created a `.wdp` project file and configured ladder reference style and sheet numbering
2. **Power bus layout** — drew multi-phase power buses to serve as the backbone of the schematic
3. **Motor branches** — inserted and wired all motor branch components (breaker → contactor → overload → motor) with proper net labels
4. **Component tagging** — assigned catalog data and enabled Xdata so every component carries its manufacturer and part number
5. **Panel layout** — placed components onto DIN rails, applied balloon annotations, and verified that all tags matched the schematic
6. **BOM generation** — ran the panel report tool to produce the component list directly from the layout data

### AutoCAD Electrical Features Used

| Feature | Purpose |
|---|---|
| Ladder references | Structured cross-sheet navigation between control and power sections |
| Multi-phase power buses | Clean three-phase distribution across all motor branches |
| Xdata / component tagging | Embedded catalog data for automated reporting |
| Balloon annotations | Linked physical panel components back to schematic references |
| Panel BOM report | Auto-generated component list from layout — no manual transcription |

---

## File Structure

```
├── autocad/
│   ├── MotorControlSystem.wdp          # AutoCAD Electrical project file
│   ├── schematic/
│   │   └── MotorControl_Schematic.dwg  # Ladder schematic drawing
│   └── panel/
│       ├── MotorControl_Panel.dwg      # Panel layout drawing
│       └── MotorControl_BOM.dwg        # BOM report drawing
├── assets/
│   ├── schematic.pdf                   # Schematic export
│   ├── panel_layout.pdf                # Panel layout export
│   └── bom_report.png                  # BOM report export
├── LICENSE
└── README.md
```

---

## License

This project is licensed under the [MIT License](LICENSE).
