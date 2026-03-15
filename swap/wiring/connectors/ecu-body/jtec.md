# ECU Body Connector: JTEC

## Used on
- Chrysler JTEC — Era 3 (1996–2001)
- Located behind the glovebox, slim silver/gray box

## Physical description
- Two connectors: C1 (large, ~64 pin) and C2 (smaller, ~32 pin)
- Delphi/Packard multi-pin bodies — similar family to SBEC but different pin count and layout
- ⚡ 1996: Same JTEC connector as 1997–2001, but harness wiring reflects Era 2 architecture

## Key circuits for open source ECU swap
All Era 2 SBEC circuits are present, plus the following additions:

| Function | Notes |
|---|---|
| Downstream O2 signal | Post-cat — not needed for engine management |
| EVAP purge solenoid output | Optional to replicate — see `vehicle/era3/evap.md` |
| EVAP vent valve output | Optional |
| Additional diagnostic circuits | OBD-II specific |

## 2000–2001 coil rail additions
| Function | Notes |
|---|---|
| Coil 1 trigger (cyl 1&6) | Replaces single coil trigger |
| Coil 2 trigger (cyl 2&5) | Additional ignition output |
| Coil 3 trigger (cyl 3&4) | Additional ignition output |
| Cam sensor (front of engine) | Different routing from 1996–1999 |

## Full pinout
Confirm against FSM. The JTEC pinout differs from the SBEC — do not transfer a SBEC pinout to a JTEC application. The XJ community has documented JTEC pinouts thoroughly; cross-reference multiple sources before finalizing an adapter harness.

## Adapter harness strategy
Same approach as SBEC. JTEC connector bodies and terminals are available. Note that 2000–2001 vehicles need 3 ignition output circuits instead of 1 — plan the open source ECU selection accordingly before building the harness. See `swap/ecu-selection/requirements.md`.
