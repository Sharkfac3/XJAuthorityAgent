# Critical Unknowns

This file lists **likely high-risk knowledge areas** for a Jeep XJ ECU swap project.

These are not confirmed repo deficiencies.
They are hypothesis targets for auditing, research planning, and backlog building.

## Purpose
Use this file to focus project-building work on the topics most likely to block a real swap, create costly mistakes, or weaken trust in the repo.

## Status rule
Each item here starts as a likely unknown.
Only move an item into confirmed gap language after a real audit of the relevant canonical files.

## Priority hypothesis list

### 1. 1996 transition-year behavior
Why it matters:
- 1996 can differ from both earlier OBD-I-style assumptions and later JTEC assumptions.
- Wrong assumptions here can corrupt wiring, diagnostics, and planning.

Likely impact:
- swap-blocking
- swap-risking

Likely destinations:
- `vehicle/era3/1996-notes.md`
- related era 3 leaf files

Questions to ask:
- What architecture differences materially affect swap planning?
- Which wiring, sensor, or diagnostic assumptions break in 1996?
- Which procedures need explicit 1996 callouts?

### 2. AW4 integration and TPS coexistence
Why it matters:
- Automatic transmission behavior can make an otherwise-running engine swap behave badly.
- TPS handling is a likely failure point.

Likely impact:
- swap-blocking
- swap-risking

Likely destinations:
- `vehicle/trans/aw4.md`
- `swap/wiring/aw4-tps.md`
- relevant tuning/wiring docs

Questions to ask:
- What signals must the TCU still receive?
- Can the aftermarket ECU share, split, or emulate those signals?
- What symptoms show incorrect TPS scaling or wiring?

### 3. Trigger pattern and sync setup by era
Why it matters:
- If trigger interpretation is wrong, the engine may not start or may run dangerously.

Likely impact:
- swap-blocking

Likely destinations:
- `vehicle/era1/trigger.md`
- `vehicle/era2/trigger.md`
- `vehicle/era3/trigger.md`
- `swap/tuning/ignition.md`

Questions to ask:
- What exact trigger architecture does each era use?
- What decoder names apply in supported ECU platforms?
- What year-range exceptions exist?

### 4. Injector characterization by era
Why it matters:
- Injector size, impedance, and dead time directly affect base fueling and first-start success.

Likely impact:
- swap-risking
- trust-reducing if vague

Likely destinations:
- `vehicle/eraX/injectors.md`
- `swap/tuning/first-start.md`

Questions to ask:
- What injector specs are known for each era?
- Which values are measured vs estimated?
- Which base assumptions are safe for first start?

### 5. Sensor calibration and compatibility mapping
Why it matters:
- Many swap failures are really sensor interpretation failures.

Likely impact:
- swap-blocking
- swap-risking

Likely destinations:
- `vehicle/eraX/sensors/*.md`
- `swap/tuning/first-start.md`
- `swap/ecu-selection/requirements.md`

Questions to ask:
- Which stock sensors are reusable?
- What calibration data is required?
- Which sensors force a platform or wiring decision?

### 6. Relay, power, and ground replication requirements
Why it matters:
- Poor power design causes unstable behavior, intermittent faults, and hard-to-debug no-starts.

Likely impact:
- swap-blocking
- swap-risking

Likely destinations:
- `vehicle/eraX/power-relay.md`
- `swap/wiring/grounds.md`
- `swap/wiring/harness.md`

Questions to ask:
- What stock power architecture must be preserved functionally?
- Which circuits need isolated grounding practices?
- What common grounding mistakes need explicit warnings?

### 7. Connector coverage and sourcing strategy
Why it matters:
- Even if the logic is correct, the swap stalls if the physical connection strategy is unclear.

Likely impact:
- swap-blocking
- trust-reducing

Likely destinations:
- `swap/wiring/connectors/index.md`
- connector family leaf files

Questions to ask:
- What family is each critical connector?
- Can it be reused, repinned, replaced, or adapted?
- What modern alternatives exist when OEM parts are scarce?

### 8. Ignition architecture splits within era 3
Why it matters:
- Distributor and coil-rail assumptions are not interchangeable.

Likely impact:
- swap-blocking
- swap-risking

Likely destinations:
- `vehicle/era3/ignition/distributor.md`
- `vehicle/era3/ignition/coil-rail.md`
- `swap/tuning/ignition.md`

Questions to ask:
- What changes in hardware, wiring, and ECU config across these systems?
- What should the reader verify before choosing a strategy?

### 9. First-start validation sequence
Why it matters:
- A strong first-start workflow prevents avoidable damage and confusion.

Likely impact:
- swap-risking

Likely destinations:
- `swap/tuning/first-start.md`
- related tuning and wiring files

Questions to ask:
- What must be verified before cranking?
- What signs indicate safe vs unsafe continuation?
- What should be checked in software vs at the vehicle?

### 10. Troubleshooting flows and failure-mode coverage
Why it matters:
- Without a troubleshooting path, users get stuck even when the technical facts exist somewhere in the repo.

Likely impact:
- swap-risking
- trust-reducing

Likely destinations:
- `swap/tuning/` files
- possible future troubleshooting docs under `swap/`

Questions to ask:
- What are the top likely no-start, sync-loss, idle, and sensor-fault failure modes?
- Where should those flows live canonically?

### 11. ECU platform decision tradeoffs for real XJ use
Why it matters:
- Generic platform comparison is not enough; the repo needs XJ-specific tradeoffs.

Likely impact:
- swap-risking
- trust-reducing

Likely destinations:
- `swap/ecu-selection/requirements.md`
- `swap/ecu-selection/speeduino.md`
- `swap/ecu-selection/rusefi.md`
- future platform files if needed

Questions to ask:
- Which platforms realistically fit the XJ use case?
- What are the practical tradeoffs for idle, trigger support, AW4, logging, and supportability?

### 12. Beginner comprehension gaps in advanced topics
Why it matters:
- A technically complete file can still fail the target audience.

Likely impact:
- trust-reducing
- quality-of-life

Likely destinations:
- `book/audience.md`
- `book/writing/style.md`
- affected leaf files

Questions to ask:
- Are terms defined on first use?
- Is “why before how” preserved?
- Are assumptions about prior ECU experience creeping in?

## How to use this file
- coverage audit → check these topics first
- research planning → break one item into smaller answerable tasks
- backlog planning → rank these against real audit findings
- release hardening → verify critical unknowns are no longer weak areas

## Do not do this
- Do not cite this file as evidence that the repo lacks a fact.
- Do not move technical claims from this file into canonical docs without validation.
