# Book: Outline

## Scope note
This file defines the current ECU swap book deliverable inside the broader Jeep XJ technical knowledge system.
It does not define the identity or full scope of the repository.

Use this outline when working on the current ECU-swap-book deliverable.
For other writing tasks, start from `AGENTS.md` and the owning technical domain before deciding whether this outline is relevant.

## Title
*Ditch the Black Box: A DIY Guide to Open Source ECU Swaps for the Jeep Cherokee XJ*

## Structure

### Part 1 — Understanding the Problem
- Ch 1: Why XJ ECUs Fail — age, heat, capacitors, discontinued parts
- Ch 2: The Three Eras — Renix, OBD-I, and OBD-II explained
- Ch 3: How the Stock System Works — sensors, actuators, the feedback loop
- Ch 4: What Open Source ECUs Are (and Are Not)

### Part 2 — Before You Touch a Wire
- Ch 5: Tools and Safety
- Ch 6: Identifying Your Era — how to confirm what you actually have
- Ch 7: Documenting the Stock System — pinouts, connector IDs, baseline datalogs
- Ch 8: Pre-Swap Health Check — injectors, sensors, harness condition
- Ch 9: Planning Your Swap — scope decisions, ECU selection, IAC strategy

### Part 3 — The Wiring
- Ch 10: XJ Harness Anatomy — engine harness, chassis harness, firewall connectors
- Ch 11: Connectors — identification, removal, replacement by family
- Ch 12: Grounds — why they matter, the required refresh
- Ch 13: Era 1 Wiring — Renix-specific considerations
- Ch 14: Era 2 Wiring — SBEC-specific considerations
- Ch 15: Era 3 Wiring — JTEC, distributor vs coil rail, 1996 notes
- Ch 16: New ECU Wiring — power supply, ASD relay, sensor inputs, outputs
- Ch 17: IAC Wiring and Strategy
- Ch 18: AW4 Automatic Transmission Interaction

### Part 4 — Configuration and First Start
- Ch 19: Initial ECU Configuration — engine constants, injector settings, sensor calibration
- Ch 20: Base Map and First Start
- Ch 21: Verifying Ignition Timing

### Part 5 — Tuning
- Ch 22: Understanding the VE Table
- Ch 23: Idle Tuning
- Ch 24: Cruise Tuning and Closed Loop
- Ch 25: WOT Tuning
- Ch 26: Tuning for the Trail

### Part 6 — Living With It
- Ch 27: Diagnostics and Fault Finding
- Ch 28: Datalogging and Ongoing Tuning
- Ch 29: OBD-II Compliance Considerations
- Ch 30: Community Resources

### Appendices
- A: Era Quick Reference — specs, trigger patterns, connectors at a glance
- B: Common Sensor Specifications
- C: Recommended Parts and Vendors
- D: Glossary

## File linkage
This deliverable currently maps to broader repo domains plus active transitional ECU swap paths:
- Chapters 2–3 → `vehicle/era*/overview.md`
- Chapters 6–8 → stock-baseline and inspection support from `vehicle/` and, as it matures, `work/inspections/`
- Chapter 9 → `swap/ecu-selection/requirements.md` and related selection files
- Chapter 11 → `swap/wiring/connectors/` now, with future sourcing-facing material expected under `sourcing/connectors/`
- Chapter 12 → `swap/wiring/grounds.md`
- Chapters 13–15 → `vehicle/era*/wiring.md`
- Chapter 16 → `swap/wiring/harness.md`
- Chapter 17 → `swap/ecu-selection/iac-strategy.md`
- Chapter 18 → `swap/wiring/aw4-tps.md` + `vehicle/trans/aw4.md`
- Chapter 27 → current diagnostics material in `swap/` and `vehicle/era*/diagnostics.md`, with future migration toward `diagnostics/`
- Appendix C → current recommendations may span `swap/` and future `sourcing/` branches
- Chapters 22–26 and 28 → `swap/tuning/`