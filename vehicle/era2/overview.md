# Era 2: OBD-I / SBEC (1991–1995)

## Identity
- ECU: Chrysler SBEC (Single Board Engine Controller) — single black box with cooling fins
- Diagnostic system: OBD-I CEL blink codes via key cycle (ON-OFF-ON-OFF-ON); DRB-II scan tool for full data; codes end with 55
- No separate ICM — SBEC controls ignition directly while the ASD relay supplies ignition/injector/fuel-pump power

## What makes this era distinct
Chrysler replaced the Renix system entirely in 1991. The SBEC is a single PCM handling both fuel and ignition. The ASD (Automatic Shut Down) relay is the key architectural difference from Era 1 — it simultaneously supplies the coil, injectors, and fuel pump, and is killed by the PCM on CPS signal loss.

## CPS connector split
- 1991–1992: Round-pin Packard connector
- 1993–1995: Flat-pin Packard connector
Same sensor, different pigtail. Confirm before ordering.

## Leaf files
| Topic | File |
|---|---|
| HO engine identity and mechanical profile | `vehicle/era2/ho-engine.md` |
| Crank/cam trigger system | `vehicle/era2/trigger.md` |
| ASD relay / power circuit | `vehicle/era2/power-relay.md` |
| Injectors | `vehicle/era2/injectors.md` |
| Fuel system (pump, tank, regulator) | `vehicle/systems/fuel/index.md` |
| MAP sensor | `vehicle/era2/sensors/map.md` |
| TPS | `vehicle/era2/sensors/tps.md` |
| CTS | `vehicle/era2/sensors/cts.md` |
| IAT | `vehicle/era2/sensors/iat.md` |
| O2 sensor | `vehicle/era2/sensors/o2.md` |
| IAC valve | `vehicle/era2/sensors/iac.md` |
| Wiring specifics | `vehicle/era2/wiring.md` |
| Diagnostics / pre-swap check | `vehicle/era2/diagnostics.md` |

## Common failures
- CPS connector corrosion (especially round-pin 1991–92)
- ASD relay contacts burning from age
- SBEC capacitor failure
- TPS wear (dead spots in potentiometer wiper)
- Injector connector degradation (EV1 connectors age poorly)
