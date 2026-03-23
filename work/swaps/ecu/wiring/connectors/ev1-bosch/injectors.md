# EV1 / Bosch Jetronic: Injector Application

## Pinout
| Pin | Circuit | Wire color (typical) |
|---|---|---|
| 1 | Injector power (12V from ASD/fuel relay) | Pink or pink/white |
| 2 | Injector ground (ECU low-side control) | Gray or tan |

## Release procedure
1. Disconnect battery negative
2. Depress locking tab with EV1 removal pick — insert from the side, not the top
3. Pull connector straight off injector — do not twist
4. Inspect tab condition before reconnecting

## Pigtail replacement
If connector body is cracked or tab is broken:
- Cut harness side pigtail ~4" from connector
- Solder new pigtail to harness wires
- Use adhesive-lined heat shrink on each joint
- Do not use push-in splice connectors on injector circuits — vibration causes failure

## Aftermarket injector compatibility
Any injector with an EV1 (Jetronic) connector body fits directly. Confirm:
- High impedance (12+ ohm) for saturated drive — all Era 1/2/3 ECUs use saturated drive
- Flow rate appropriate for 4.0L application — see era injector file for target range
