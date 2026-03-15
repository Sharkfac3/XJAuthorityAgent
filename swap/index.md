# Swap Workflow Index

This repo is organized around one core job:
helping a user replace the stock Jeep XJ engine control system with an open-source aftermarket ECU.

The era folders exist to explain what the Jeep currently has. The swap folders exist to explain what to do next.

## How to use this index
1. Start from the swap stage you are in.
2. Load the era-specific vehicle files only as needed to identify stock hardware, wiring, and exceptions.
3. Keep year/era context attached to the actual swap decision.

## Stage 1 — Identify the stock control system
Load:
- `vehicle/engine.md`
- one of:
  - `vehicle/era1/overview.md`
  - `vehicle/era2/overview.md`
  - `vehicle/era3/overview.md`
- if 1996 may be involved: `vehicle/era3/1996-notes.md`

Use this stage to answer:
- Which ECU family does the Jeep have?
- Which ignition architecture does it use?
- Which sensors/connectors are likely present?
- Which year-specific exceptions matter before planning the swap?

## Stage 2 — Check whether the Jeep is a good swap candidate
Load:
- era `diagnostics.md`
- era `wiring.md`
- `vehicle/trans/aw4.md` or `vehicle/trans/manual.md`

Use this stage to answer:
- Is the stock harness healthy enough to reuse or adapt?
- Are there sensor or relay issues that must be understood before conversion?
- Does the transmission create special constraints?

## Stage 3 — Choose the swap strategy
Load:
- `swap/ecu-selection/requirements.md`
- relevant platform file under `swap/ecu-selection/`
- `swap/ecu-selection/iac-strategy.md` when idle control matters
- `swap/ecu-selection/wideband.md` when closed-loop/tuning hardware is in scope

Use this stage to answer:
- Which aftermarket ECU platform fits the XJ use case?
- What idle strategy is realistic?
- Which supporting hardware is required?

## Stage 4 — Plan the wiring integration
Load:
- `swap/wiring/grounds.md`
- `swap/wiring/harness.md`
- era `power-relay.md`
- era `wiring.md`
- `swap/wiring/connectors/index.md` + needed family file
- `swap/wiring/aw4-tps.md` if AW4 is present

Use this stage to answer:
- What stock power architecture must be replicated?
- Which connectors can be reused, replaced, or adapted?
- What harness strategy makes sense for this era?
- What transmission-related wiring must remain intact?

## Stage 5 — Configure for first start
Load:
- `swap/tuning/first-start.md`
- `swap/tuning/ignition.md`
- `swap/tuning/idle-tuning.md`
- era `trigger.md`
- era `injectors.md`
- needed sensor files under `vehicle/eraX/sensors/`

Use this stage to answer:
- What engine constants and trigger settings are required?
- How should injectors and sensors be configured?
- What must be verified before cranking?

## Stage 6 — Tune and validate
Load:
- `swap/tuning/ve-table.md`
- `swap/tuning/afr-targets.md`
- `swap/tuning/closed-loop.md`
- `swap/tuning/wot-tuning.md`
- `swap/tuning/trail-tuning.md`
- `vehicle/trans/aw4.md` if automatic behavior matters

Use this stage to answer:
- How should the base calibration be improved safely?
- What matters for drivability and trail reliability?
- How do transmission behavior and ECU tuning interact?

## Scope rule
If a question is about what the Jeep came with, load `vehicle/`.
If a question is about how to make the swap work, load `swap/` first and pull in `vehicle/` only for the stock-context facts you need.
