# Electrical architecture - extracted design overview

**Project status:** Proposed conceptual architecture, not a built or commissioned electrical installation.  
**Source:** Group report pp. 30-39, 73-77, 82-87.

## Main functional blocks

- **Control:** ESP32-WROOM-32E controller on a proposed custom PCB (report p. 73).
- **Inputs:** PT100 temperature measurement through MAX31865; optical egg presence/count; capacitive oil-level feedback; planned limit switches (pp. 73, 75, 83-87).
- **Actuators:** Proposed NEMA 17 stepper motors with DRV8825 drivers, MG996R servos, a 24 V solenoid, a peristaltic oil pump, and cooling fan (pp. 72-75).
- **Heater:** Mains heating subsystem switched via solid-state relay (concept p. 30; sourced selection p. 74). The exact heater technology/power is *not consistent across the report*.
- **Power:** Design documents consider a 230 V AC to 24 V DC supply, a 24 V-to-5 V buck converter, and a 5 V-to-3.3 V regulator (pp. 30, 74).
- **Human interface:** Touchscreen with operator commands and status feedback (pp. 40-46, 73). Different concept stages give different display sizes.

## Report circuit diagram

![Original electrical circuit diagram, from the report](Electrical-Circuit-Diagram.png)

The image above is an embedded figure **extracted without circuit changes** from p. 73 (Section 9, Circuit Diagram). The original image is resolution-limited; no editable schematic or verified wiring netlist was available in the submitted report.

## Scope of individual work

The group report assigns measurement-chain design, circuit schematics, sensor component selection, signal conditioning, electrical BOM, and hardware validation planning to Hasti Chiniforoush (p. 5). Mechanical CAD, HMI, and functional-structure tasks were assigned to other group members.

## Design limitations

The drawings and BOMs are academic design artifacts. Electrical safety, mains isolation, protective device coordination, supply sizing, and component compatibility require an engineering review before any physical construction. See `../bom/BOM-Discrepancies.md` and `../docs/Source-Mapping-and-Limitations.md`.
