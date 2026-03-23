# No Spark

## Purpose
Provide a fault-isolation starter path for XJs that crank normally but appear to have no ignition spark.

## Symptom definition
Use this leaf when the engine rotates on the starter, but spark is absent or the ignition system is the leading suspect.

## Do not use this leaf when
- the engine will not crank at all
- the complaint is a clear fuel no-prime condition
- the complaint is a running misfire rather than complete spark loss

## First checks
1. Confirm this is truly a **crank-no-start** complaint, not a no-crank complaint.
2. Identify the era before assuming ignition architecture:
   - Era 1 / Renix: [`../../vehicle/era1/overview.md`](../../vehicle/era1/overview.md)
   - Era 2 / SBEC: [`../../vehicle/era2/overview.md`](../../vehicle/era2/overview.md)
   - Era 3 / JTEC: [`../../vehicle/era3/overview.md`](../../vehicle/era3/overview.md)
3. On 2000–2001 vehicles, confirm whether the Jeep uses the stock coil-rail layout: [`../../vehicle/era3/ignition/coil-rail.md`](../../vehicle/era3/ignition/coil-rail.md)
4. On distributor-era vehicles, keep the era overview and trigger file loaded before assuming cap, rotor, coil, or cam-sync details.
5. If 1996 is involved, confirm the transition-year sensor and harness caveat first: [`../../vehicle/era3/1996-notes.md`](../../vehicle/era3/1996-notes.md)

## Common branches

### Crank-signal branch
A lost or weak crank signal is a top-priority no-spark cause across all eras.
Use the matching era trigger file to confirm what the crank sensor reads and what signal family applies:
- [`../../vehicle/era1/trigger.md`](../../vehicle/era1/trigger.md)
- [`../../vehicle/era2/trigger.md`](../../vehicle/era2/trigger.md)
- [`../../vehicle/era3/trigger.md`](../../vehicle/era3/trigger.md)

Era-specific clues already in canon:
- Era 1 CPS signal is weak at cranking RPM and is a known failure point
- Era 2 blink code **11** indicates no crank reference
- Era 3 code **P0335** indicates CPS no signal and **P1391** can indicate intermittent crank/cam loss

### Cam-sync branch
The era trigger files also make clear that the XJ ignition system depends on cam-sync context.
If the crank signal exists but spark is still absent or unstable, continue with the era-appropriate cam-sensor path.

Clues already in canon:
- Era 3 code **P0340** indicates cam-sensor no signal
- Era 1 and Era 2 distributor systems house the cam sensor in the distributor
- 2000–2001 moves the cam sensor to the front of the engine with coil-rail ignition

### Ignition-architecture branch
The hardware that actually delivers spark changes by era:
- Era 1 uses a separate ICM and distributor ignition architecture
- Era 2 and 1996–1999 Era 3 use distributor-based single-coil ignition without a separate ICM
- 2000–2001 Era 3 uses a coil rail with three paired outputs

Load the correct stock file before assuming cap, rotor, coil, or driver behavior.

### Power and relay branch
If trigger inputs appear valid, continue toward power-supply and relay-path checks for the ignition system.
Useful stock context:
- [`../../vehicle/era1/power-relay.md`](../../vehicle/era1/power-relay.md)
- [`../../vehicle/era2/power-relay.md`](../../vehicle/era2/power-relay.md)
- [`../../vehicle/era3/power-relay.md`](../../vehicle/era3/power-relay.md)

### Code-driven branch
For eras with code support, read codes before replacing parts:
- Era 2 blink-code guide: [`../../vehicle/era2/diagnostics.md`](../../vehicle/era2/diagnostics.md)
- Era 3 OBD-II triage: [`../engine/era3-control-system-triage.md`](../engine/era3-control-system-triage.md)

Renix has no stored DTC shortcut:
- [`../../vehicle/era1/diagnostics.md`](../../vehicle/era1/diagnostics.md)

## Exit criteria
Route out of this starter leaf when the evidence clearly points to:
- lost crank reference
- lost cam-sync input
- ignition power / relay-path failure
- era-specific secondary hardware such as distributor, coil, cap, rotor, wires, or coil rail
