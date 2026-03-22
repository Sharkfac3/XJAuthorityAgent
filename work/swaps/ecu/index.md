# ECU Swaps Index

## Purpose
Route Jeep XJ ECU and engine-management architecture conversion work without pretending the migration is already finished.

## Scope
Use this branch for ECU swap planning, wiring integration, first-start work, and post-install engine-management setup.

## Transitional status
- Current live ECU swap execution content remains canonical under `swap/` during migration.
- Use this router as the preferred target-state branch inside `work/`, then follow into `swap/` for the current live execution files.
- Do not treat `swap/` as the center of the whole repo; treat it as the active compatibility branch for ECU swap execution.

## What belongs here
- ECU conversion project routing and compatibility notes
- links to selection, wiring, sensor, startup, and tuning sub-branches
- future migrated procedure stacks from the current `swap/` tree
- cross-links to stock-era wiring or engine baselines when they materially affect the conversion

## What does not belong here
- generic stock vehicle facts with no conversion context
- symptom-first fault isolation after the swap unless the main task is diagnosis
- sourcing-only comparisons with no execution context
- unrelated non-ECU swap work

## Expected child branches
- `planning/` for project definition, scope boundaries, and conversion-path selection
- `ecu-selection/` for choosing the control strategy before following live content under `swap/ecu-selection/`
- `wiring/` for harness integration and stock-interface routing via `swap/wiring/`
- `integration/` for stock-subsystem coexistence topics such as AW4 TPS sharing
- `sensors-and-inputs/` for trigger, sync, and sensor strategy decisions tied to the conversion
- `first-start-and-validation/` for startup sequencing and immediate post-install checks
- `tuning-and-calibration/` for the live migration bridge into `swap/tuning/` and later `work/setup-and-calibration/ecu/`

## Current live route
- workflow router → `swap/index.md`
- ECU selection → `swap/ecu-selection/`
- wiring integration → `swap/wiring/`
- first start and tuning → `swap/tuning/`
