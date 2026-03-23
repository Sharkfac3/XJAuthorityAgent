# ECU Setup And Calibration Index

## Purpose
Route engine-management setup and calibration work after ECU changes or major engine-management work.

## Use this branch when
The ECU is already installed or the task is mainly about configuration, sensor setup, idle behavior, warmup behavior, or tune refinement rather than wiring conversion.

## Canonical support files
Load this branch for the `work/` classification, then follow into the ECU-swap execution leaves under [`../../swaps/ecu/tuning-and-calibration/index.md`](../../swaps/ecu/tuning-and-calibration/index.md) and [`../../swaps/ecu/first-start-and-validation/index.md`](../../swaps/ecu/first-start-and-validation/index.md) when you need the XJ aftermarket ECU workflow.

## What belongs here
- base-map and startup setup
- sensor calibration and input validation
- idle, warmup, and drivability refinement
- cross-links to stock trigger, injector, and sensor baselines that affect configuration

## What does not belong here
- stock baseline facts with no action context
- harness-build procedures
- symptom-first troubleshooting as the primary topic
- sourcing-only comparisons as the primary topic

## Planned high-value child branches
- `base-map-and-first-start/`
- `sensor-calibration/`
- `idle-and-warmup-tuning/`

## Boundary links
- ECU swap execution router: [`../../swaps/ecu/index.md`](../../swaps/ecu/index.md)
- ECU swap tuning files: [`../../swaps/ecu/tuning-and-calibration/index.md`](../../swaps/ecu/tuning-and-calibration/index.md)
- Vehicle era and sensor baselines: [`../../../vehicle/years/index.md`](../../../vehicle/years/index.md)
