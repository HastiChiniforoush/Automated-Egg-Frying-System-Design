# Differences between the two electrical BOMs - design review needed

The original report contains **two distinct electrical BOM sections** with different reference-number assignments. They have been extracted into **two separate CSV files** rather than silently merged.

- `Concept-Electrical-BOM-Report-Extract.csv`: Section 4.5, report pp. 30-31; references E-01 through E-31.
- `Sourcing-Electrical-BOM-Report-Extract.csv`: Section 9, report pp. 73-77; references E-01 through E-54.

**Never assume that E-06 (or any other reference) represents the same component in both CSVs.** For example, concept E-06 means *SSR heat sink*, but sourcing E-06 means *Mean Well AC/DC power supply*.

## Specific unresolved differences

| Issue | Earlier concept / other part of report | Later sourcing section | Source pages |
|---|---|---|---|
| Heating technology / quantity | Descriptive section mentions induction; concept BOM has one 800-1000 W heating plate | Four 400 W, 230 V heating cartridges | 28, 30, 74 |
| Main DC power | 230 VAC to 24 VDC, 120 W | Mean Well LRS-150-24, 156 W | 30, 74 |
| Stepper motors and drivers | Three NEMA17 motors / three motor drivers | Two NEMA17 motors / two DRV8825 driver modules | 30, 72, 74 |
| Touchscreen | Five-inch screen in rough sketch, seven-inch in concept BOM | Nextion seven-inch UART display | 27, 30, 73 |
| Safety thermal cutoff | Process design target is 150-180 C | The later requirements list suggests a 150 C cutoff in one place | 83-85 |
| Electrical BOM numbering | Concept E-01 through E-31 | Sourcing E-01 through E-54 with different mapping | 30-31, 73-77 |

No correction or engineering reconciliation has been performed here. **These are source-report discrepancies**, not defects proven by testing.

## Before fabrication

Confirm a single heating method, thermal operating range and independent protection setpoint; calculate all load and supply currents; reconcile actuator count and motor driver ratings; validate mains wiring and protection with a qualified engineer; check controller 3.3 V input compatibility; finalize one unified BOM and schematic.

This file is a documentation aid only and does not establish compliance with any regulation or safety standard.
