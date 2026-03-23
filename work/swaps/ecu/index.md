# ECU Swaps Index

## Purpose
Route the canonical Jeep XJ aftermarket ECU conversion workflow.

Use this branch when the main question is how to plan, wire, start, validate, or tune an aftermarket ECU installation in an XJ.

## Do not start here when
- the question is mainly about stock factory configuration → [`../../../vehicle/index.md`](../../../vehicle/index.md)
- the question is mainly about non-ECU job execution → [`../../index.md`](../../index.md)
- the question is mainly about symptom diagnosis → [`../../../diagnostics/index.md`](../../../diagnostics/index.md)
- the question is mainly about parts, donor, connector, or kit choice with no execution focus → [`../../../sourcing/index.md`](../../../sourcing/index.md)
- the task is reader-facing informational writing → [`../../../book/README.md`](../../../book/README.md) plus the owning technical branch

## How to use this index
1. Identify the stock era and transmission first.
2. Enter the ECU-swap stage that matches the current decision.
3. Pull in stock `vehicle/` files only where the swap decision depends on them.
4. Pull in `diagnostics/` or `work/inspections/` only when the Jeep must be proven healthy before conversion.

## Stage 1 — Identify the stock control system
Load:
- [`../../../vehicle/engine.md`](../../../vehicle/engine.md)
- one of:
  - [`../../../vehicle/era1/overview.md`](../../../vehicle/era1/overview.md)
  - [`../../../vehicle/era2/overview.md`](../../../vehicle/era2/overview.md)
  - [`../../../vehicle/era3/overview.md`](../../../vehicle/era3/overview.md)
- if 1996 may be involved: [`../../../vehicle/era3/1996-notes.md`](../../../vehicle/era3/1996-notes.md)
- transmission baseline: [`../../../vehicle/systems/transmission/overview.md`](../../../vehicle/systems/transmission/overview.md)

Use this stage to answer:
- Which ECU family does the Jeep have?
- Which ignition architecture does it use?
- Which year-specific exceptions matter before planning the swap?
- Does AW4 vs manual change the plan immediately?

## Stage 2 — Prove the stock Jeep is a valid swap candidate
Load:
- Era 1: [`../../../vehicle/era1/diagnostics.md`](../../../vehicle/era1/diagnostics.md)
- Era 2: [`../../../vehicle/era2/diagnostics.md`](../../../vehicle/era2/diagnostics.md)
- Era 3 diagnostics: [`../../../diagnostics/engine/era3-control-system-triage.md`](../../../diagnostics/engine/era3-control-system-triage.md)
- Era 3 inspection: [`../../inspections/pre-swap/era3-health-check.md`](../../inspections/pre-swap/era3-health-check.md)
- era wiring file
- AW4 or manual stock baseline as needed

Use this stage to answer:
- Is the stock harness healthy enough to reuse or adapt?
- Are there existing faults that will poison swap work?
- Does transmission choice create special constraints?

## Stage 3 — Choose the ECU strategy
Load:
- [`ecu-selection/index.md`](ecu-selection/index.md)
- [`ecu-selection/requirements.md`](ecu-selection/requirements.md)
- relevant platform file under `ecu-selection/`
- [`ecu-selection/iac-strategy.md`](ecu-selection/iac-strategy.md) when idle control matters
- [`sensors-and-inputs/wideband-o2.md`](sensors-and-inputs/wideband-o2.md) when tuning hardware is in scope

## Stage 4 — Plan wiring integration
Load:
- [`wiring/index.md`](wiring/index.md)
- [`wiring/grounds.md`](wiring/grounds.md)
- [`wiring/harness-strategy.md`](wiring/harness-strategy.md)
- era `power-relay.md`
- era `wiring.md`
- [`wiring/connectors/index.md`](wiring/connectors/index.md) plus needed family file
- [`integration/aw4-tps.md`](integration/aw4-tps.md) if AW4 is present
- [`wiring/platform-specific/index.md`](wiring/platform-specific/index.md) when board-specific translation work is needed

## Stage 5 — Configure for first start
Load:
- [`first-start-and-validation/index.md`](first-start-and-validation/index.md)
- [`first-start-and-validation/first-start.md`](first-start-and-validation/first-start.md)
- [`tuning-and-calibration/ignition-timing.md`](tuning-and-calibration/ignition-timing.md)
- era `trigger.md`
- era `injectors.md`
- needed sensor files under `vehicle/eraX/sensors/`

## Stage 6 — Tune and validate
Load:
- [`tuning-and-calibration/index.md`](tuning-and-calibration/index.md)
- [`tuning-and-calibration/ve-table.md`](tuning-and-calibration/ve-table.md)
- [`tuning-and-calibration/afr-targets.md`](tuning-and-calibration/afr-targets.md)
- [`tuning-and-calibration/closed-loop.md`](tuning-and-calibration/closed-loop.md)
- [`tuning-and-calibration/wot-tuning.md`](tuning-and-calibration/wot-tuning.md)
- [`tuning-and-calibration/trail-tuning.md`](tuning-and-calibration/trail-tuning.md)
- AW4 baseline if automatic behavior matters

## Branch routers
- ECU platform choice → [`ecu-selection/index.md`](ecu-selection/index.md)
- Wiring strategy and translation → [`wiring/index.md`](wiring/index.md)
- Stock-subsystem coexistence → [`integration/index.md`](integration/index.md)
- Sensors and auxiliary inputs → [`sensors-and-inputs/index.md`](sensors-and-inputs/index.md)
- First-start workflow → [`first-start-and-validation/index.md`](first-start-and-validation/index.md)
- Tuning and calibration → [`tuning-and-calibration/index.md`](tuning-and-calibration/index.md)

## Boundary links
- Stock baseline needed before conversion: [`../../../vehicle/index.md`](../../../vehicle/index.md)
- Pre-swap inspections: [`../../inspections/pre-swap/index.md`](../../inspections/pre-swap/index.md)
- Setup-and-calibration router for ECU work: [`../../setup-and-calibration/ecu/index.md`](../../setup-and-calibration/ecu/index.md)
