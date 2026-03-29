# Era 3: Diagnostics

## Reading codes
No key-cycle blink codes. Connect any generic OBD-II scanner to the 16-pin DLC under the dash (driver's side).
- Generic scanner: reads and clears DTCs, shows live sensor data
- DRB-III: Chrysler factory scan tool — required for full live data, actuation tests, and cam sync verification on 2000–2001

All codes are 5-character SAE P-codes (P0xxx) or Chrysler-specific P1xxx codes.

## Common DTCs — 4.0L

| Code | Circuit | Common XJ cause |
|---|---|---|
| P0107 | MAP sensor voltage too low | Failed MAP sensor, broken or kinked vacuum hose, signal wire shorted to ground |
| P0108 | MAP sensor voltage too high | Failed MAP sensor, open circuit in signal wire |
| P0131 | Upstream O2 sensor low voltage | Failed upstream O2 sensor, exhaust leak before sensor |
| P0136 | Downstream O2 sensor circuit | Failed downstream O2 sensor — very common; downstream harness runs near driveshaft |
| P0141 | Downstream O2 heater circuit | Downstream O2 heater failure — same sensor, different failure mode |
| P0171 | System lean (bank 1) | Vacuum leak, failing MAP sensor, weak fuel pump, failing upstream O2 |
| P0172 | System rich (bank 1) | Leaking injector, failed downstream O2 feeding false signal |
| P0300 | Random / multiple misfire | CPS failure, coil or coil rail, fuel pressure, head gasket |
| P0301–P0306 | Cylinder-specific misfire | Same causes as P0300, cylinder identified |
| P0335 | CKP (crank) sensor circuit | Failed CPS, damaged wiring or connector, damaged reluctor ring |
| P0339 | CKP sensor intermittent | Same as P0335 but intermittent — typical before total failure |
| P0340 | CMP (cam) sensor circuit | Failed cam sensor; distributor stator on 1996–1999; cam sensor or sync out of range on 2000–2001 |
| P0344 | CMP sensor intermittent | Same as P0340 intermittent |
| P0441 | EVAP purge flow fault | Stuck-open or stuck-closed purge solenoid, large vacuum leak in EVAP plumbing |
| P0455 | EVAP large leak | Loose or missing fuel cap; cracked EVAP hose or canister |
| P1388 | ASD relay circuit — no voltage | ASD relay failed, wiring fault between PCM and relay |
| P1389 | ASD relay circuit — no ground | PCM not commanding relay; relay coil open |

## P0300 + P0335 combination
This pairing is the most common multi-code pattern on the 4.0L. A failing CPS produces an erratic or absent crank signal — the PCM logs P0335 and cannot fire injectors or coil reliably, producing P0300 misfires. Replace the CPS before chasing coil, plug, or fuel components.

## Pre-swap checklist

- [ ] Read and record all current codes with OBD-II scanner
- [ ] No P0335 / P0339 — CPS signal confirmed good
- [ ] No P0340 / P0344 — cam sensor confirmed good
- [ ] TPS sweep smooth, no dead spots (monitor with scanner live data)
- [ ] MAP reads barometric at key-on engine-off (~100 kPa at sea level)
- [ ] CTS resistance at ambient matches Chrysler NTC curve — see `vehicle/era2/sensors/cts.md`
- [ ] Upstream O2 oscillating at warm idle (~0.1–0.9V, approximately once per second)
- [ ] Downstream O2 active at warm idle (not flat)
- [ ] All injectors clicking during cranking (stethoscope or long screwdriver to rail)
- [ ] Fuel pressure 49 psi key-on (49 ± 5 psi acceptable; below 44 psi = weak pump; above 54 psi = stuck regulator)
- [ ] Pressure holds above 24 psi for 5 minutes after shutdown
- [ ] ASD relay activates at key-on (fuel pump primes — audible 2-second prime)
- [ ] EVAP codes only — note but not a swap blocker
- [ ] All sensor connectors inspected — no corrosion, broken locks, or backed-out pins
- [ ] Ground straps clean and tight (block-to-chassis, head-to-firewall)

## 2000–2001 coil rail specific checks

- [ ] All 3 coil outputs verified — each coil pair fires (1&6, 2&5, 3&4)
- [ ] Cam sync in range — DRB-III SET SYNC screen should show "IN RANGE" and 0°
- [ ] No P0340 without also having P0335 — isolated cam codes on DIS suggest sync issue, not sensor failure
