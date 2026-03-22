# No Prime

## Purpose
Provide a starter fault-isolation path for XJs that do not show an obvious fuel-pump prime at key-on or do not build fuel delivery during early no-start checks.

## Symptom definition
Use this leaf when the fuel-pump prime is absent, inconsistent, or suspected to be missing.

## Important caution
No audible pump prime is not, by itself, proof that the pump is dead.
Confirm the complaint with a pressure check, a voltage check, or both before turning one missing sound into a parts decision.

## First checks
1. Confirm battery state and main power supply first.
2. Confirm the complaint is fuel-related and not already explained by an ignition or crank-signal problem.
3. Check the relevant fuse and relay path before condemning the pump.
4. Listen for prime, but also verify whether the pump receives power during crank if key-on behavior is unclear.
5. Inspect obvious connector and ground issues at accessible points before treating the module itself as failed.

## Era split matters here
Fuel-pump control logic is not identical across all XJ eras.
Load the correct stock power-relay context before making assumptions about what should be powered together.

- Era 1: [`vehicle/era1/power-relay.md`](../../vehicle/era1/power-relay.md)
- Era 2: [`vehicle/era2/power-relay.md`](../../vehicle/era2/power-relay.md)
- Era 3: [`vehicle/era3/power-relay.md`](../../vehicle/era3/power-relay.md)
- 1996 caution: [`vehicle/era3/1996-notes.md`](../../vehicle/era3/1996-notes.md)

## Common branches

### Fuse or relay path branch
If there is no pump command or no pump feed, confirm the fuse, relay, and feed side before dropping the tank.
Era 1 and Era 2/3 route related loads differently enough that the stock era file should be loaded first.

### Pump-ground or connector branch
If command appears present but pump operation is still absent, inspect the connector and ground path.
Connector-family identification and repair-choice routing belong under [`sourcing/connectors/index.md`](../../sourcing/connectors/index.md) when the next question becomes what repair parts to buy.

### Crank-signal and control branch
If the vehicle only loses fuel delivery during crank or after the initial prime window, confirm whether the control side is intentionally dropping the fuel path because of a crank-signal or control issue.
That branch may require engine or ignition diagnostics as well.

### Pump/module branch
Only move to pump or module replacement after feed, ground, and control logic have been checked enough to make the module the most likely fault.

## Exit criteria
Route out of this starter leaf when you can state that the next job is mainly:
- electrical/control diagnosis
- tank-side repair work
- connector or terminal sourcing
- non-fuel no-start diagnosis
