# Era 1: Renix (1988–1990)

## Identity
- ECU: Single Renix fuel ECU + separate Ignition Control Module (ICM)
- Diagnostic system: Pre-OBD — no Check Engine Lamp, no DTCs, no key-cycle codes
- Scan tool: Renix-proprietary only (rare); diagnosis is FSM + DVOM

## What makes this era distinct
The Renix system is a Bosch-licensed design from a Renault/Bendix joint venture. It is the oldest and most failure-prone system in scope. Unlike Era 2/3, the ignition path runs through a separate ICM — the fuel ECU and ignition module are two distinct boxes working in parallel, not a single PCM.

## Leaf files
| Topic | File |
|---|---|
| Crank/cam trigger system | `vehicle/era1/trigger.md` |
| Fuel/ignition power relay | `vehicle/era1/power-relay.md` |
| Injectors | `vehicle/era1/injectors.md` |
| MAP sensor | `vehicle/era1/sensors/map.md` |
| TPS | `vehicle/era1/sensors/tps.md` |
| CTS | `vehicle/era1/sensors/cts.md` |
| IAT | `vehicle/era1/sensors/iat.md` |
| O2 sensor | `vehicle/era1/sensors/o2.md` |
| IAC valve | `vehicle/era1/sensors/iac.md` |
| Knock sensor | `vehicle/era1/sensors/knock.md` |
| Wiring specifics | `vehicle/era1/wiring.md` |
| Diagnostics / pre-swap check | `vehicle/era1/diagnostics.md` |

## Common failures
- ECU capacitor failure (electrolytic caps dry out with age)
- CPS weak signal at low RPM / cold
- CPS air gap from flywheel/flexplate wear
- Renix MAP sensor failure
- Injector connector degradation (EV1 connectors become brittle)
- Corroded firewall multi-pin connectors
- ICM failure
