# Drivability Setup And Calibration Index

## Purpose
Route calibration and setup tasks tied to idle, throttle response, and running quality.

## Scope
Calibration and setup tasks tied to idle, throttle response, and running quality.

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
- `idle-setup/` for final idle-speed or idle-quality adjustment work
- `throttle-and-tv-cable-adjustment/` for response and shift-related setup where applicable
- `post-repair-running-quality-checks/` for final drivability validation
