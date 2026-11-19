# Electrical Bill of Materials — Design-Stage Summary

I led the electrical BOM work in the 2026 group design project. The report includes a full detailed electrical component list (E-01 to E-54), with preliminary prices and source notes.

**Important:** The table below is a selected *overview*, not the complete procurement BOM. Pricing is intentionally excluded because the 2026 estimates were not re-verified. All parts and quantities require review before purchasing.

| Report reference | Selected item / family | Design role |
| --- | --- | --- |
| E-01 | ESP32-WROOM-32E-H4 | Main controller |
| E-02 | Nextion NX8048P070-011C, 7-inch | Touchscreen HMI |
| E-03 | PT100 Class A probe | Frying temperature |
| E-04 | MAX31865 interface | PT100 signal conditioning |
| E-06 | Mean Well LRS-150-24 | 24 V DC supply |
| E-07 | LM2596 buck module | 24 V-to-5 V conversion |
| E-08 | 3.3 V regulator | ESP32 logic supply |
| E-09 | HOTSET 230 V / 400 W cartridges (4 in detailed BOM) | Frying heat source |
| E-10 | SSR-25DA | Heating switching |
| E-16–E-17 | NEMA 17 stepper motors | Egg feeding and pan rotation |
| E-18 | DRV8825 modules | Stepper motor control |
| E-19–E-22 | MG996R servos | Cracking and serving motions |
| E-23 | 24 V DC solenoid | Cracking mechanism |
| E-24 | 24 V peristaltic oil pump | Oil dispensing |
| E-26–E-27 | MOSFETs and flyback diodes | DC-load switching/protection |
| E-28–E-30 | IR sensors | Position detection and counting |
| E-31 | XKC-Y25-V capacitive sensor | Oil-level indication |
| E-53–E-54 | Proposed custom controller PCB and assembly | Design/manufacturing items; not completed |

The detailed BOM also lists electrical protection, wiring, connectors, passives, electronics enclosure and assembly-related items.

## BOM Review Needed

The detailed BOM and the separate requirements manual in the report describe **different configurations** in places (for example, the quantity of motors and the heating-element arrangement). These should be treated as alternative design-stage entries rather than a finalized build specification. See [Design Review Notes](../docs/Design-Review-Notes.md).

To publish the complete original BOM, extract it from the report, review each line for consistency and remove private information and unverified commercial details as necessary.

