# Electrical Design and System Architecture

This folder documents the **proposed electrical architecture** for the Automated Four-Egg Frying Machine (academic design project, 2026). It does not contain a manufactured or validated circuit.

## Functional Signal Flow

```text
PT100 temperature probe -- MAX31865 (SPI) --+
IR egg sensors (digital inputs) --------------+--> ESP32 controller
Capacitive oil-level sensor (input) ----------+         |
                                                      +--> Touchscreen HMI
                                                      +--> DRV8825 stepper drivers
                                                      +--> Servo control signals
                                                      +--> MOSFET-switched DC loads
                                                      +--> SSR heating control
```

## Power Distribution — Design Concept

```text
230 V AC input
  |-- AC heating branch --> SSR --> heating cartridges
  |-- AC/DC supply --> 24 V DC --> motors / DC actuators
                           |--> buck converter --> 5 V
                                                      |--> 3.3 V regulator --> ESP32
```

These are *functional-level* diagrams. They are not wiring instructions or verified power-distribution schematics. Mains wiring, overcurrent protection, thermal cut-offs, isolation, protective earth and emergency stop would require a detailed safety review before construction.

## Components Selected in the Detailed BOM

- **Controller:** ESP32-WROOM-32E-H4, 3.3 V logic
- **RTD interface:** MAX31865 for the PT100, connected via SPI
- **HMI:** Nextion 7-inch display, described as UART in the detailed component list
- **Motor drivers:** DRV8825 for NEMA 17 stepper motors; PWM for MG996R servos
- **Power:** Mean Well LRS-150-24, LM2596 adjustable buck converter and 3.3 V regulator
- **Heating:** 230 V cartridge heaters, SSR and protective components (design proposal)

## Deliverables

The original group report documents component selection, architecture and a proposed custom controller PCB. **Do not claim that the PCB was fabricated, assembled or tested.** Add any original circuit drawings you personally own and are permitted to publish here, such as `Controller-Schematic.pdf` or `Electrical-Block-Diagram.png`, once available.

## Design Review

See [Design-Review-Notes.md](../docs/Design-Review-Notes.md) for alternative component/quantity choices in different sections of the report.

