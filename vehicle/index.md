# Vehicle Index

## Purpose
Route agents and humans to canonical stock Jeep XJ platform facts.

## Scope
This branch is for stock vehicle truth: what the XJ came with, how factory systems are arranged, and what changed by year, era, package, or configuration.

## What belongs here
- year and era differences
- stock subsystem architecture
- package and configuration baselines
- factual interchange baselines for stock parts
- factory hardware changes and compatibility boundaries

## What does not belong here
- step-by-step work procedures
- symptom-first diagnostics trees
- donor buying advice or kit recommendations
- agent operating instructions

## Child branches
- [`vehicle/years/index.md`](years/index.md) — time-based routing for era and model-year differences
- [`vehicle/systems/index.md`](systems/index.md) — subsystem-based stock facts
- [`vehicle/packages/index.md`](packages/index.md) — package-defined stock differences
- [`vehicle/configurations/index.md`](configurations/index.md) — stock configuration matrices and baseline combinations
- [`vehicle/interchange-baselines/index.md`](interchange-baselines/index.md) — factual stock interchange limits

## Transition notes
- Existing canonical era material remains valid under `vehicle/era1/`, `vehicle/era2/`, and `vehicle/era3/` until migration is complete.
- Existing transmission baselines remain valid under `vehicle/trans/` until they are migrated into `vehicle/systems/transmission/`.
