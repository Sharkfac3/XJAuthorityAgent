# Charging Starting Overview

## Purpose
Route stock Jeep XJ charging and starting baseline facts.

## Scope
Use this branch for factory battery, cable, starter, alternator, and power-distribution context that later maintenance, diagnostics, and sourcing work depends on.

## What belongs here
- stock charging and starting architecture
- major year or era split points that change power-distribution assumptions
- baseline relationships between battery, cables, starter, alternator, and grounds
- cross-links to action and diagnostic branches that depend on this stock context

## What does not belong here
- battery replacement or cable-cleaning procedures
- no-crank or low-voltage troubleshooting trees
- donor or upgrade recommendations as the primary topic
- modified-state charging upgrades except for routing pointers

## Current child leaves
- [`year-changes.md`](year-changes.md) — practical split points to confirm before service, diagnosis, or parts ordering

## Cross-domain routes
- Charging and starting maintenance: [`work/maintenance/charging-starting/index.md`](../../../work/maintenance/charging-starting/index.md)
- Charging and starting diagnostics: [`diagnostics/charging-and-starting/index.md`](../../../diagnostics/charging-and-starting/index.md)
- Electrical sourcing and connector decisions: [`sourcing/interchange/electrical/index.md`](../../../sourcing/interchange/electrical/index.md)

## Next likely child files
- `battery-and-cable-baseline.md`
- `alternator-families.md`
- `starter-and-solenoid-baseline.md`
- `grounds-and-power-distribution.md`
