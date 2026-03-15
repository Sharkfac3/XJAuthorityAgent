# Era 3: OBD-II / JTEC (1996–2001)

## Identity
- ECU: Chrysler JTEC (Jeep Truck Engine Controller) — slim silver/gray box
- Diagnostic system: OBD-II standard 16-pin DLC — any generic OBD-II scanner works
- No separate ICM — JTEC drives ignition via ASD relay (same as Era 2)

## What makes this era distinct
OBD-II compliance is the primary change from Era 2. The JTEC adds downstream O2 sensor monitoring, full EVAP system control, and additional emissions sensors. Ignition splits into two sub-eras based on year.

## Ignition sub-eras
| Years | Ignition type | File |
|---|---|---|
| 1996–1999 | Distributor (cap, rotor, single coil) | `vehicle/era3/ignition/distributor.md` |
| 2000–2001 | Coil rail — waste spark, no distributor | `vehicle/era3/ignition/coil-rail.md` |

## ⚡ 1996 transition year
1996 uses the JTEC OBD-II ECU but carries over OBD-I era sensors, harness connectors, and wiring architecture from Era 2. The ECU changed; the physical harness largely did not. See `vehicle/era3/1996-notes.md` before working on any 1996 vehicle.

## Leaf files
| Topic | File |
|---|---|
| Crank/cam trigger | `vehicle/era3/trigger.md` |
| ASD relay / power circuit | `vehicle/era3/power-relay.md` |
| Injectors | `vehicle/era3/injectors.md` |
| EVAP system | `vehicle/era3/evap.md` |
| 1996 transition notes | `vehicle/era3/1996-notes.md` |
| MAP sensor | `vehicle/era3/sensors/map.md` |
| TPS | `vehicle/era3/sensors/tps.md` |
| CTS | `vehicle/era3/sensors/cts.md` |
| IAT | `vehicle/era3/sensors/iat.md` |
| O2 sensors (upstream + downstream) | `vehicle/era3/sensors/o2.md` |
| IAC valve | `vehicle/era3/sensors/iac.md` |
| Wiring specifics | `vehicle/era3/wiring.md` |
| Diagnostics / pre-swap check | `vehicle/era3/diagnostics.md` |

## Common failures
- JTEC capacitor failure (same aging issue as SBEC)
- EVAP solenoid failure (sets codes, not critical for engine operation)
- Downstream O2 sensor failure (catalyst monitor only)
- CPS connector corrosion
