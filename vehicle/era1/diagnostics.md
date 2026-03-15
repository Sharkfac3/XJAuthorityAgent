# Era 1: Diagnostics

## No CEL, no DTCs
The Renix system is pre-OBD. There is no Check Engine Lamp, no malfunction indicator light, and no stored fault codes of any kind. This is not a fault — it is by design. Many inspection stations incorrectly flag the absence of a CEL bulb as a failure.

## How to diagnose Renix
Diagnosis is entirely symptom-based using a DVOM and the factory service manual (FSM). There is no shortcut. The FSM contains voltage and resistance specifications for every sensor and actuator — work through them methodically.

A Renix-compatible scan tool exists (rare, expensive, and mostly irrelevant to the swap process).

## Pre-swap checklist
- [ ] CPS signal present during cranking — check with oscilloscope or DVOM (AC millivolts) at CPS connector while cranking
- [ ] CPS air gap within spec — 0.020"–0.050" between sensor tip and flywheel/flexplate
- [ ] MAP sensor output at key-on engine-off: ~4.5V (atmospheric)
- [ ] MAP vacuum hose intact — no cracks, kinks, or soft spots
- [ ] TPS sweep smooth from 0.5V to 4.5V — no dead spots
- [ ] CTS resistance at ambient matches Renix curve — see `vehicle/era1/sensors/cts.md`
- [ ] IAT resistance at ambient plausible
- [ ] IAC audible stepping at key-on
- [ ] All injectors clicking during cranking (listen with a mechanic's stethoscope)
- [ ] Fuel pressure at 39 psi key-on
- [ ] Fuel pump relay activates at key-on
- [ ] O2 sensor oscillating at warm idle
- [ ] All Renix-native sensor connectors inspected — photograph before removal
- [ ] ECU capacitors inspected — any bulging or leaking caps = ECU needs recapping before swap
- [ ] Grounds: block-to-chassis, head-to-firewall, battery negative — clean and tight
- [ ] Firewall multi-pin connector inspected and cleaned

## ECU capacitor note
Renix ECUs fail when the electrolytic capacitors on the circuit board dry out with age. If the ECU is original, budget for a recap (replace capacitors) before or during the swap. A failing ECU will cause intermittent no-start, rough running, and misfires that mimic sensor failures.
