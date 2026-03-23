# No Crank

## Purpose
Provide a starter fault-isolation path for XJs that do not crank when the key is turned to start.

## Symptom definition
Use this leaf when the engine does **not** rotate normally on the starter.
This includes dead-silence, a single click, or repeated relay / solenoid clicking without real crank speed.

## Do not use this leaf when
- the engine cranks normally but will not start
- the engine cranks slowly enough that the main complaint is weak cranking speed rather than no starter engagement
- the main complaint is low running voltage after the engine starts

For those cases, route instead to:
- ignition or fuel diagnosis if it is a crank-no-start complaint
- `slow-crank.md` when that leaf exists
- [`low-charging-voltage.md`](low-charging-voltage.md) for a running-voltage complaint

## First checks
1. Confirm the battery terminals are tight, clean, and not heat-damaged.
2. Confirm the main grounds are intact before condemning the starter.
3. Watch what happens when the key is turned to start:
   - no sound at all
   - single click
   - repeated clicking
   - brief engagement then drop-out
4. If tooling allows, confirm battery condition before chasing deeper wiring faults.
5. Confirm whether the Jeep is AW4 automatic or manual because the start-enable path can differ by transmission family.

## Common branches

### Battery and cable branch
A weak battery or bad cable end can present as total no-crank.
Start with visible connection condition before replacing the starter.
If the cable and ground path is visibly degraded, route through [`work/maintenance/charging-starting/cable-and-ground-service/overview.md`](../../work/maintenance/charging-starting/cable-and-ground-service/overview.md).

### Supply-path branch
If the battery is known good but the starter does not engage, inspect the high-current path and major grounds.
A connection-loss problem can mimic a failed starter.

### Starter / solenoid branch
If power supply and connection basics are good, continue toward repair-level starter-feed or starter-motor follow-up under [`work/repairs/charging-starting/index.md`](../../work/repairs/charging-starting/index.md).

### Start-enable branch
Transmission family matters here.
- AW4 vehicles may require automatic-transmission context before assuming the start path
- Manual-transmission vehicles do not use the AW4 TCM path and may have year/configuration-specific clutch or neutral inputs

Load stock baseline first:
- [`../../vehicle/systems/transmission/aw4/overview.md`](../../vehicle/systems/transmission/aw4/overview.md)
- [`../../vehicle/systems/transmission/manual/overview.md`](../../vehicle/systems/transmission/manual/overview.md)

### Era and wiring branch
If the problem depends on relay, connector, or harness assumptions, identify the era first.
Load:
- [`../../vehicle/systems/charging-starting/year-changes.md`](../../vehicle/systems/charging-starting/year-changes.md)
- [`../../vehicle/years/index.md`](../../vehicle/years/index.md)
- [`../../vehicle/era3/1996-notes.md`](../../vehicle/era3/1996-notes.md) for 1996 vehicles

## Exit criteria
Route out of this starter leaf when the evidence clearly points to:
- battery or cable neglect
- a starter or starter-feed repair problem
- a start-enable / transmission-context problem
- a year-specific harness or relay-path issue that requires era-specific stock context
