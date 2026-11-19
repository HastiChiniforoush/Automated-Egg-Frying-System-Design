# Proposed Electrical Verification Plan

**Status:** Planning document. These are *intended future tests* based on the team's design; **they were not executed on a completed machine**.

The electrical hardware-validation work package was part of my assigned responsibilities.

| ID | Proposed check | What should be verified |
| --- | --- | --- |
| V-01 | Supply-rail check | 24 V, 5 V and 3.3 V rails under the specified load conditions |
| V-02 | PT100 interface | Sensor wiring, plausible readings and comparison with a trusted reference |
| V-03 | Temperature fault handling | Broken or implausible sensor readings inhibit unsafe heater commands |
| V-04 | Heating switching | SSR control logic and correct default-off behavior; assessed with a qualified safety setup |
| V-05 | Temperature regulation | Response to a setpoint, overshoot and repeatability on instrumented equipment |
| V-06 | IR sensor inputs | Detection of single eggs and fault response to missed or repeated triggers |
| V-07 | Oil-level sensing | Correct indication of low and sufficient oil levels |
| V-08 | Stepper motor interface | Direction, step signals, load current and repeatable positioning |
| V-09 | Servo / solenoid outputs | Command behavior and protection of switching circuits |
| V-10 | Emergency stop / thermal safety | Protective shutdown design and independent safeguards |
| V-11 | Noise and wiring | Measurement stability with motors and heating circuits active |
| V-12 | System-level sequence | Requested egg count, sensor feedback and actuator coordination |

## Before Testing

- Consolidate the open design selections and component counts.
- Carry out electrical, mechanical, thermal and food-safety assessments with suitable supervision.
- Establish measurable acceptance criteria, test instruments and data-logging methods.
- Document results only after a test has genuinely been performed.

This document is **not** a certification, commissioning record or safety approval. In particular, high-voltage heating hardware should not be assembled or tested on the basis of this summary alone.

