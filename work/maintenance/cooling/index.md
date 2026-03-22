# Cooling Maintenance Index

## Purpose
Route cooling-system service, refresh, and wear-item maintenance.

## Scope
Use this branch when the main question is how to baseline or maintain the stock cooling system rather than diagnose a fault or choose parts.

## What belongs here
- scheduled or catch-up cooling service
- refresh work for unknown-history vehicles
- maintenance tasks that reduce future overheating risk
- cross-links to stock baselines, diagnostics, and sourcing when support context is needed

## What does not belong here
- stock cooling architecture with no action context
- symptom-first overheating diagnosis
- brand or donor selection as the primary topic
- unrelated repair or upgrade workflows

## Current child packages
- [`cooling-system-refresh/overview.md`](cooling-system-refresh/overview.md) — narrow starter package for baseline cooling refresh work

## Cross-domain routes
- Stock cooling baseline: [`vehicle/systems/cooling/overview.md`](../../../vehicle/systems/cooling/overview.md)
- Cooling diagnostics: [`diagnostics/cooling/index.md`](../../../diagnostics/cooling/index.md)
- Cooling sourcing tradeoffs: [`sourcing/oem-vs-aftermarket/cooling/index.md`](../../../sourcing/oem-vs-aftermarket/cooling/index.md)

## Next likely child packages
- `coolant-flush/`
- `belt-and-fan-service/`
- `heater-hose-and-clamp-renewal/`
