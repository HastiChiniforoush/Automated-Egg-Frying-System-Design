# Proposed hardware verification plan (not executed)

**Status:** DESIGN-ONLY. This is a planning matrix derived from the project report, not evidence of a completed prototype or passed tests.

The companion CSV, [`Proposed-Verification-Matrix.csv`](Proposed-Verification-Matrix.csv), organizes ten proposed checks across temperature measurement, heating control, electrical power, optical and oil-level sensing, motor interfaces, emergency stop and integration.

## Verification approach

1. **Design review:** reconcile the two electrical BOMs, select one heating approach, and resolve power and thermal protection requirements.
2. **Component/interface checks:** confirm ESP32 voltage compatibility, PT100/MAX31865 interface, driver load ratings and mechanical sensor mounting.
3. **Bench plan:** define safe, supervised test procedures for low-voltage electronics first, then separately review mains and heating circuits with appropriately qualified personnel.
4. **Integration plan:** define operating sequences, alarm states and hardware shutdown logic.
5. **Documentation:** log intended test procedures, acceptance criteria, measured results and deviations **only after tests are actually carried out**.

The report does not include real prototype testing or measured performance. No pass/fail status is assigned.

**Source:** Group report pp. 30-31, 45-52, 65-77 and 82-87.
