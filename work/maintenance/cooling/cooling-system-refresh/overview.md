# Cooling System Refresh Overview

## Purpose
Scope a baseline cooling-service package for XJs with unknown history, aging hoses, or overdue coolant maintenance.

## Use this package when
- the vehicle is new to you and cooling-service history is unclear
- hoses, clamps, cap, bottle, or coolant condition are obviously aged
- you want to reduce failure risk before a longer trip or summer use
- the system is functioning, but maintenance is overdue

## Do not use this package when
- the vehicle is actively overheating and the fault path is not yet isolated
- there is a known failed component that belongs in `work/repairs/`
- the main question is which replacement part family to buy

If the symptom is active overheating, start with [`diagnostics/cooling/overheating-at-idle.md`](../../../../diagnostics/cooling/overheating-at-idle.md) or the relevant cooling diagnostic leaf.

## Baseline checks before starting
1. Confirm engine family and transmission type.
2. Confirm whether the job will touch fan wiring, switches, or relays.
3. If electrical-side cooling assumptions matter, load the era wiring context listed in [`vehicle/systems/cooling/year-changes.md`](../../../../vehicle/systems/cooling/year-changes.md).
4. Decide whether the job is still maintenance or has become a repair because of leakage, cracked plastic, or a failed fan component.

## Child leaves
- [`procedure.md`](procedure.md) — maintenance sequence and decision points for a baseline refresh

## Supporting canon
- Stock baseline: [`vehicle/systems/cooling/overview.md`](../../../../vehicle/systems/cooling/overview.md)
- Split points before parts ordering: [`vehicle/systems/cooling/year-changes.md`](../../../../vehicle/systems/cooling/year-changes.md)
- Cooling diagnostics: [`diagnostics/cooling/index.md`](../../../../diagnostics/cooling/index.md)
- Cooling sourcing tradeoffs: [`sourcing/oem-vs-aftermarket/cooling/index.md`](../../../../sourcing/oem-vs-aftermarket/cooling/index.md)

## Next likely child files
- `required-parts.md`
- `validation.md`
- `fan-clutch-and-shroud-checks.md`
