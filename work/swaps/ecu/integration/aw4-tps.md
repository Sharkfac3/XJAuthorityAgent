# AW4 TPS Integration

## Purpose
Route ECU-swap integration work where the AW4 automatic transmission must keep seeing a valid TPS signal.

## Transitional status
The current live procedure remains `swap/wiring/aw4-tps.md` during migration.

Use this file as the target-state work-branch destination for AW4/ECU integration routing.

## What matters
- the AW4 TCM reads TPS voltage directly from the engine harness
- the AW4 expects a normal 0.5 V to 4.5 V TPS sweep on a 5 V reference
- cutting, rerouting, or distorting that signal changes shift timing and lockup behavior

## Use these files together
- stock AW4 baseline: `vehicle/systems/transmission/aw4/overview.md`
- current live wiring procedure: `swap/wiring/aw4-tps.md`

## Transition note
This file receives the modified-state routing split out of `vehicle/trans/aw4.md` without duplicating the full live procedure.
