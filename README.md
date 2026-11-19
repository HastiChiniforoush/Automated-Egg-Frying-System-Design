# Automated Four-Egg Frying Machine — Electrical & Control System Design

**Rhine-Waal University of Applied Sciences | Group Project | Summer Semester 2026**  
**Project status:** Academic engineering design/concept — **not a built or experimentally validated machine**

## Overview

This interdisciplinary group project developed a design concept for an automated machine that stores, feeds, cracks, fries and serves eggs. The concept supports orders of **one to four eggs** and includes a heated frying unit, mechanical handling, sensors, actuators and a user interface. A throughput of **120 eggs per hour** was a design target, not a measured result.

This repository focuses on the **electrical engineering and sensor-integration work** undertaken within the larger project.

## My Contributions — Hasti Chiniforoush

Within the four-person team, I led the electrical-engineering work on:

- Measurement-chain design and signal conditioning
- Circuit schematics and electrical subsystem interfaces
- Selection and integration planning for sensors and electronic components
- Electrical bill of materials (BOM) and technical purchasing specifications
- Planning of electrical hardware verification and validation
- Supporting the design failure mode and effects analysis (DFMEA)

Mechanical CAD, HMI design, system-level functional diagrams and several other work packages were led by other teammates.

## Planned Technical Architecture

| Subsystem | Selected / proposed design approach |
| --- | --- |
| Main control | ESP32-WROOM-32E microcontroller-based controller |
| Temperature measurement | Three-wire PT100 RTD with MAX31865 interface (SPI) |
| Heating | 230 V AC heating elements controlled through a solid-state relay (SSR) |
| Position / counting | IR break-beam sensors for egg detection and counting |
| Oil reservoir | Non-contact capacitive oil-level sensor |
| Motion | NEMA 17 steppers with DRV8825 modules; MG996R servos; solenoid |
| User interface | Touchscreen HMI |
| Low-voltage power | AC/DC 24 V supply, 5 V buck conversion and 3.3 V regulation |

These are **design-stage selections** documented in the group report. Some specifications and quantities differ between the report's conceptual and detailed BOM sections; see [design-review notes](docs/Design-Review-Notes.md). The prototype was not constructed, so there are no experimental performance results.

## Project Documentation

- [Electrical architecture and interfaces](electrical-design/README.md)
- [Sensors and measurement chain](sensors/README.md)
- [Electrical BOM overview](bom/README.md)
- [Proposed verification plan](verification/README.md)
- [Images and diagrams](images/README.md)
- [Technical documentation and design-review notes](docs/README.md)

## Engineering Considerations

The design work considered controller/sensor interfaces, actuator drivers, temperature feedback, electrical protection, thermal safety and component manufacturability. The project report also contains a DFMEA. These were **engineering proposals**, not evidence of electrical safety certification or completed verification tests.

## Source and Attribution

Prepared from the team's *Egg Frying Machine* report, submitted **12 May 2026** as part of Group Project 04. This repository describes the contributor's work and summaries of the group concept. Original shared documents or diagrams should be uploaded only where all necessary publication permissions exist, and personal/student details should be removed.
