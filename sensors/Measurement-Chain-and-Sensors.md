# Measurement chain and sensor selection (design-stage extract)

**Project:** Automated Egg Frying Machine - Group Project, Summer Semester 2026  
**Status:** Academic design only; no sensor integration or hardware validation was completed.  
**Source:** Original group report, pp. 21, 24, 34-38, 45, 73-76 and 83-87.

## Planned temperature measurement chain

`Frying surface -> 3-wire PT100 Class A RTD -> MAX31865 signal-conditioning / RTD interface -> SPI -> ESP32-WROOM-32E -> heater control logic`

- **PT100 sensor:** The selected sensor type monitors frying-surface temperature. The requirements section specifies a Class A, 3-wire probe for a 0-200 C range and cites 150-180 C as a target process range (p. 83).
- **MAX31865:** Converts PT100 resistance information into digital temperature data over SPI; an interface module and 430 ohm reference resistor appear in the sourcing list (p. 73).
- **Controller:** ESP32-WROOM-32E selected as the planned controller; sensor feedback informs the heating-control subsystem (pp. 35-37, 73).
- **Heater switching:** A solid-state relay is selected in the design documents for switching the heating circuit (pp. 37, 74, 83). This is **not** a validated mains wiring design.

## Other sensing and feedback concepts

| Function | Proposed sensor or feedback | Planned controller interface | Report references |
|---|---|---|---|
| Egg presence / feeding position | IR break-beam sensor | Digital signal | pp. 33, 75-76, 86 |
| Cracking position | IR break-beam sensor | Digital signal | pp. 75, 86 |
| Remaining egg count | IR counting / break-beam arrangement | Digital signal | pp. 45, 75, 86 |
| Oil level | Capacitive sensor, XKC-Y25-V in the sourcing list | Digital signal, with voltage matching to be checked | pp. 24, 75, 86 |
| Actuator home / end positions | Mechanical limit switches | Digital signal | pp. 31, 87 |

## Engineering considerations from the design phase

1. Confirm the selected PT100 probe and the MAX31865 interface match the intended accuracy and wiring arrangement.
2. Confirm input electrical levels are compatible with 3.3 V ESP32 logic; interface circuitry is not fully proven in the report.
3. Plan signal checks for missing, implausible, and disconnected sensor outputs.
4. Keep heating safety shutoff independent of normal firmware operation; the design's thermal protection setpoints must be reconciled with the intended cooking range.

**No experimental measurement traces, calibrated readings, or validated wiring pin assignments were supplied in the original report.** Do not claim these tests were completed.
