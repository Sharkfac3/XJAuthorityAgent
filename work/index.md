# Work Index

## Purpose
Route job-oriented Jeep XJ content: maintenance, repair, restoration, upgrades, swaps, inspections, and setup work.

## Scope
Use this branch when the main question is how to do a job on or to the vehicle.

## What belongs here
- procedures and workflow stubs
- project execution branches
- setup, adjustment, and post-work validation guidance
- action-oriented stock-service and modified-state work

## What does not belong here
- pure stock platform facts with no action context
- symptom-first diagnostics trees
- buying-only guidance
- repo governance

## Child branches
- [`maintenance/index.md`](maintenance/index.md)
- [`repairs/index.md`](repairs/index.md)
- [`restoration/index.md`](restoration/index.md)
- [`upgrades/index.md`](upgrades/index.md)
- [`swaps/index.md`](swaps/index.md)
- [`inspections/index.md`](inspections/index.md)
- [`setup-and-calibration/index.md`](setup-and-calibration/index.md)

## Transition notes
- `work/` is the broad home for action-oriented XJ guidance.
- Current ECU swap execution content remains canonical under `swap/` until migration into `work/swaps/ecu/`.
- Use `work/swaps/index.md` and `work/swaps/ecu/index.md` as the target-state routing model, but follow `swap/` for the live ECU execution branch today.
- New non-ECU procedural content should be added under this `work/` architecture rather than under `swap/`.
