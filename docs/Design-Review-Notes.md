# Design Review Notes — Open Items

**Status:** Unresolved design-stage observations, not fixes or conclusions. These are based on differences between sections of the team's May 2026 report and require a new review before implementation.

## 1. Heating Arrangement

The detailed electrical parts list (report section 9, p. 74) specifies **four 230 V, 400 W heating cartridges**. The separate requirement manual (p. 85) describes a **230 V heating plate in the 800–1000 W range**. These should not be presented as the same finalized heating solution. The concept description also uses alternative heating terminology. A final thermal design and corresponding protection design are still required.

## 2. Motor / Actuator Counts

The detailed BOM and electrical drive summary describe **two NEMA 17 steppers** (feeding and pan rotation), along with servos and a cracking solenoid. Other requirement-manual tables describe **three steppers / drivers** with a different allocation. A unified electrical architecture and BOM revision would be needed.

## 3. HMI Communication

The detailed selected Nextion touchscreen (section 9, p. 73) specifies **UART TTL**, whereas a more generic interface requirement elsewhere allows SPI/parallel. The final display communication interface must match the selected hardware and MCU pin plan.

## 4. Safety and Verification

The report proposes protective-earth wiring, fusing, emergency stop, thermal protection, SSR control and hygienic design. Their inclusion in a conceptual BOM **does not establish electrical or food-safety compliance**. Component suitability, the intended safety architecture, power budgets and physical tests remain open.

## 5. Project Status

No production hardware, assembled controller PCB, successful cooking tests or measured 120-eggs/hour throughput are documented. The work is presented as a **design concept** and **verification plan** only.
