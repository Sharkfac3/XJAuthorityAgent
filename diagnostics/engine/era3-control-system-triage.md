# Era 3 Control-System Triage

## Purpose
Route first-pass engine-management diagnosis for 1996–2001 XJs using the Era 3 OBD-II control system.

## Scope
Use this file when the main question is what stored code, sensor fault, or control-system signal should be checked next on a stock or stock-style Era 3 engine-management system.

## Read codes first
Connect a generic OBD-II scanner to the 16-pin data link connector under the driver-side dash.

- No key-cycling method is needed.
- Read stored and pending codes before clearing anything.
- Record freeze-frame or live-data context when available.

## Common Era 3 codes and first checks
| Code | Description | Common XJ cause |
|---|---|---|
| P0107 | MAP low voltage | failed MAP sensor, cracked or disconnected vacuum hose |
| P0108 | MAP high voltage | MAP wiring short, sensor fault |
| P0117 | CTS low voltage | shorted coolant-temperature sensor or wiring |
| P0118 | CTS high voltage | open CTS circuit or disconnected sensor |
| P0121 | TPS range/performance | worn TPS, intermittent sweep fault |
| P0122 | TPS low voltage | TPS ground fault, sensor fault, wiring issue |
| P0123 | TPS high voltage | TPS reference or signal wiring fault |
| P0131 | Upstream O2 low voltage | failed upstream O2, mixture issue, wiring fault |
| P0134 | Upstream O2 no activity | dead sensor, open circuit, sensor not heating |
| P0136 | Downstream O2 low voltage | failed downstream O2 or wiring fault |
| P0300 | Random misfire | multiple possible causes; inspect ignition, fuel, and mechanical condition |
| P0301–P0306 | Cylinder misfire | injector, plug, wire, compression, or cylinder-specific fault |
| P0335 | CPS no signal | failed crank sensor, wiring issue, connector problem |
| P0340 | Cam sensor no signal | distributor-sync or cam-sensor fault |
| P0441 | EVAP incorrect purge | purge solenoid, hose routing, canister fault |
| P0455 | EVAP large leak | loose gas cap, cracked hose, system leak |
| P1297 | No change in MAP | MAP stuck or vacuum signal problem |
| P1391 | Intermittent CPS or cam loss | connector corrosion, intermittent sensor failure |

## Triage priorities
Start with faults that can prevent normal running or corrupt multiple downstream readings:
1. crank and cam sync faults
2. TPS and MAP signal faults
3. power, grounds, and connector condition
4. misfire and oxygen-sensor faults
5. EVAP faults after core running issues are sorted

## Boundary note
This file is for diagnostics and first-pass fault isolation.

If you are evaluating whether a donor or project vehicle is healthy enough before an ECU swap, use `work/inspections/pre-swap/era3-health-check.md`.

## Transition note
This file is the diagnostics destination split out of `vehicle/era3/diagnostics.md`.
