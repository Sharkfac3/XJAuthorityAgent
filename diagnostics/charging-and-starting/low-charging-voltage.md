# Low Charging Voltage

## Purpose
Provide a starter fault-isolation path for XJs that show weak running voltage, dim lights, or a battery that is not recovering after starting.

## Symptom definition
Use this leaf when the engine runs, but system voltage remains suspiciously low or electrical load drags the system down more than expected.

## Do not use this leaf when
- the engine will not crank at all and the main symptom is starter engagement
- the complaint is a parked-vehicle battery drain
- the main question is preventive cable cleanup with no active charging complaint

## First checks
1. Confirm the belt is present, correctly routed, and not obviously slipping.
2. Confirm battery terminals are clean, tight, and not heat-damaged.
3. Confirm major grounds and cable ends are intact before condemning the alternator.
4. Compare voltage at the battery and at the alternator output path if access and tooling allow.
5. Note whether the problem appears only at idle, only under heavy load, or all the time.

## Common branches

### Connection-loss branch
Corroded or loose battery terminals, block grounds, and charging-path connections can mimic a bad alternator.
Start with [`work/maintenance/charging-starting/cable-and-ground-service/overview.md`](../../work/maintenance/charging-starting/cable-and-ground-service/overview.md) if the connection path is visibly degraded.

### Belt-drive branch
If the complaint gets worse with load or wet conditions, inspect the belt and accessory-drive side before replacing electrical parts.
A weak charging system can be mechanical before it is electrical.

### Alternator-output branch
If belt and connection basics are good, continue toward alternator output testing and repair-level follow-up under [`work/repairs/charging-starting/index.md`](../../work/repairs/charging-starting/index.md).

### Battery-confusion branch
A badly weak battery can distort charging complaints.
If the battery itself is suspect, verify it before treating every low-voltage reading as an alternator fault.

## Split points to confirm
If the complaint depends on connector, fuse, relay, or harness assumptions, confirm the stock era context first:
- [`vehicle/systems/charging-starting/year-changes.md`](../../vehicle/systems/charging-starting/year-changes.md)
- [`vehicle/era3/1996-notes.md`](../../vehicle/era3/1996-notes.md) for 1996 vehicles

## Exit criteria
Route out of this starter leaf when the evidence clearly points to:
- maintenance-related cable and ground neglect
- a repair-level alternator, starter-feed, or power-distribution fault
- a battery condition problem rather than an alternator problem
