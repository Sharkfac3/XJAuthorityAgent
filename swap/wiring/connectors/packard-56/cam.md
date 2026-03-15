# Packard 56: Cam Sensor Connector

## Used on
- Camshaft position sensor (cam sensor / sync pulse generator) — Era 2 and Era 3 (1996–1999)
- Era 3 (2000–2001): Cam sensor moves to front of engine — connector style may differ, verify against FSM

## Physical description
- 3-pin connector
- Hall effect sensor — requires power, ground, and signal (unlike VR CPS which only needs 2 signal wires)

## Pinout
| Pin | Circuit |
|---|---|
| A | 8V or 5V supply (check FSM for specific year) |
| B | Ground |
| C | Signal output (0V / 5V square wave) |

## Notes
- Hall effect sensor — polarity and power supply pin must be correct
- Incorrect power supply voltage will damage sensor
- Signal output goes directly to ECU cam input — no conditioning required
- On 2000–2001 coil rail vehicles, the cam sensor relocates to the front of the engine; verify connector style at the new location before assuming Packard 56 family
