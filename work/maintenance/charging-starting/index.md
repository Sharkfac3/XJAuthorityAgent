# Charging And Starting Maintenance Index

## Purpose
Route battery, cable, starter, and charging-system upkeep.

## Scope
Use this branch when the main question is preventive service or baseline upkeep rather than fault isolation.

## What belongs here
- battery and cable upkeep
- ground-service work
- belt and charging-system baseline checks
- maintenance tasks that reduce no-crank and low-voltage failures

## What does not belong here
- stock architecture with no action context
- symptom-first no-crank or low-voltage diagnosis
- upgrade or donor selection as the primary topic
- unrelated chassis electrical work

## Current child packages and leaves
- [`cable-and-ground-service/overview.md`](cable-and-ground-service/overview.md) — narrow starter package for recurring cable and ground upkeep

## Cross-domain routes
- Stock charging and starting baseline: [`vehicle/systems/charging-starting/overview.md`](../../../vehicle/systems/charging-starting/overview.md)
- Charging and starting diagnostics: [`diagnostics/charging-and-starting/index.md`](../../../diagnostics/charging-and-starting/index.md)
- Electrical sourcing and interchange: [`sourcing/interchange/electrical/index.md`](../../../sourcing/interchange/electrical/index.md)

## Next likely child packages
- `battery-service/`
- `belt-and-charging-checks/`
- `starter-cable-refresh/`
