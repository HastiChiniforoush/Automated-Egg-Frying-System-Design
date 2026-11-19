# Sensors and Measurement Chain

My electrical work included sensor selection, measurement-chain design, signal conditioning, and interface planning. The following components are **proposed**, not installed or experimentally characterized.

| Measured quantity / event | Proposed sensor or interface | Role |
| --- | --- | --- |
| Frying-surface temperature | Three-wire Class A PT100 RTD | Temperature feedback for controlled heating |
| PT100 signal conditioning | MAX31865 RTD-to-digital interface (SPI) | Converts RTD resistance measurement to digital data for ESP32 |
| Egg position before cracking | IR break-beam sensor | Detects egg presence at a process station |
| Egg counting | IR counting / break-beam sensor | Supports order quantity and available egg count |
| Oil level | XKC-Y25-V capacitive sensor (detailed BOM) | Signals low oil level without a probe inside the reservoir |

## Proposed Measurement Path

1. **Temperature:** PT100 probe → MAX31865 signal-conditioning interface → SPI → ESP32 → heating-control decision.
2. **Egg presence:** IR break-beam digital output → microcontroller input → sequence logic / HMI indication.
3. **Oil level:** Capacitive sensor output → microcontroller input → warning or inhibit condition.

## Design Considerations

- RTD wiring, measurement resolution and noise reduction
- Digital-input compatibility with the 3.3 V ESP32 logic (level adaptation may be required)
- Cable routing, connector reliability and safe separation from heater wiring
- Sensor failure detection and operator notification
- Environmental suitability near heat, moisture, cleaning agents and food areas

## Documentation Status

The team report describes these component choices and interfaces. No calibration logs, measured uncertainty, temperature-response plots, or physical sensor verification results were produced for a built machine. See the proposed checks in [Verification Plan](../verification/README.md).

