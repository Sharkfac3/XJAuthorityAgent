# ECU Setup And Calibration Index

## Purpose
Route engine-management setup and calibration topics after ecu changes or major engine-management work.

## Scope
Engine-management setup and calibration topics after ECU changes or major engine-management work.

## What belongs here
- concrete job folders and procedure leaves for this branch
- local compatibility notes when year, drivetrain, ABS, or donor differences materially change the work
- required-parts, procedure, and validation leaves when the topic grows beyond a single page
- narrow cross-links to `vehicle/`, `diagnostics/`, or `sourcing/` when support context is needed

## What does not belong here
- stock baseline facts with no action context
- symptom-first troubleshooting trees
- sourcing-only comparisons as the primary topic
- unrelated work classes or repo-governance content

## Expected child branches
- `base-map-and-first-start/` for initial calibration and startup setup
- `sensor-calibration/` for TPS, coolant, MAP, wideband, or related input setup
- `idle-and-warmup-tuning/` for early-stage drivability refinement
