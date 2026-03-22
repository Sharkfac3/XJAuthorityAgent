# Overheating At Idle

## Purpose
Provide a starter fault-isolation path for XJs that run hot in traffic, at long idle, or during slow trail movement.

## Symptom definition
Use this leaf when the temperature problem is strongest at low vehicle speed and improves once road speed and airflow increase.

## Do not use this leaf when
- the vehicle overheats equally at all speeds
- coolant is disappearing with no confirmed idle-only pattern
- the main symptom is poor cabin heat with normal engine temperature

## Why this symptom matters
Idle-only overheating usually points first toward an airflow or low-speed heat-rejection problem rather than a pure highway-load problem.
That makes fan operation, shroud integrity, debris blockage, and baseline coolant condition higher-value first checks than a blind parts swap.

## First checks
1. Confirm the symptom is real and repeatable.
2. Check coolant level and obvious leak evidence before running the engine longer.
3. Confirm the fan shroud is present and intact.
4. Inspect the radiator and condenser face for packed debris or bent fins.
5. Check whether the mechanical-fan side and any auxiliary electric-fan side are both doing their jobs for the vehicle's configuration.
6. Confirm the belt and water-pump drive are not slipping.

## Common branches

### Airflow branch
If the XJ cools down once vehicle speed increases, check low-speed airflow first:
- weak or failed fan clutch
- non-functioning auxiliary electric fan where equipped
- missing or damaged shroud
- debris blocking the radiator or condenser face

### Coolant-condition branch
If airflow basics look acceptable, check whether poor coolant condition or overdue maintenance is reducing heat transfer:
- badly aged coolant
- collapsed or internally degraded hoses
- cap or recovery-system issues
- general unknown-history cooling neglect

Start service-oriented baseline work at [`work/maintenance/cooling/cooling-system-refresh/overview.md`](../../work/maintenance/cooling/cooling-system-refresh/overview.md).

### Circulation or restriction branch
If the system still overheats after airflow and maintenance checks, escalate toward repair-level causes such as:
- restricted radiator core
- thermostat problems
- pump or circulation problems
- heater-side blockage clues that suggest broader cooling restriction

## Split points to confirm
If the symptom path touches fan wiring, relays, switches, or connectors, confirm the vehicle's era wiring context first:
- [`vehicle/era1/wiring.md`](../../vehicle/era1/wiring.md)
- [`vehicle/era2/wiring.md`](../../vehicle/era2/wiring.md)
- [`vehicle/era3/wiring.md`](../../vehicle/era3/wiring.md)
- [`vehicle/era3/1996-notes.md`](../../vehicle/era3/1996-notes.md) for 1996 vehicles

## Exit criteria
Route out of this starter leaf when you have enough evidence to say the problem is mainly:
- maintenance-related → [`work/maintenance/cooling/`](../../work/maintenance/cooling/)
- repair-related → `work/repairs/cooling/`
- part-choice related → [`sourcing/oem-vs-aftermarket/cooling/index.md`](../../sourcing/oem-vs-aftermarket/cooling/index.md)
