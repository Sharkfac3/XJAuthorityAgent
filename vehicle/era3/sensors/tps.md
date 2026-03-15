# Era 3: Throttle Position Sensor (TPS)

## Specs
Identical to Era 2. See `vehicle/era2/sensors/tps.md` for full specs.
Output: 0.5V closed throttle → 4.5V WOT. Reference: 5V.

## Connector
- 1996: Era 2 connector (Metri-Pack 150 3-pin) — see `vehicle/era3/1996-notes.md`
- 1997–2001: Metri-Pack 150 3-pin — same as Era 2

## AW4 interaction
Unchanged from Era 2. TPS signal wire still tapped by AW4 TCM on automatic vehicles.
See `swap/wiring/aw4-tps.md`.

## Swap notes
Same as Era 2. Calibrate closed throttle and WOT endpoints in ECU software after installation.
