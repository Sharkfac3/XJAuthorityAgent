# Era 2: Diagnostics

## Reading blink codes
1. Turn ignition ON-OFF-ON-OFF-ON within 5 seconds (end on ON, do not crank)
2. Count CEL flash patterns: short blinks = tens digit, pause, short blinks = units digit
3. Code 55 always appears last — signals end of sequence
4. Record all codes before clearing

## Common OBD-I codes
| Code | Circuit | Common XJ cause |
|---|---|---|
| 11 | No crank reference | CPS failure, wiring, connector corrosion |
| 12 | Memory power lost | Battery recently disconnected — normal |
| 13 | MAP sensor | Failed sensor, cracked vacuum hose |
| 14 | MAP voltage low | Vacuum leak at sensor port |
| 21 | O2 sensor | Failed sensor, open circuit |
| 22 | CTS voltage low | Shorted CTS, wiring |
| 23 | CTS voltage high | Open CTS circuit, loose connector |
| 24 | TPS voltage high | Failed TPS, wiring |
| 25 | TPS voltage low | TPS ground issue |
| 27 | Injector circuit | Open injector or wiring |
| 37 | TCC solenoid | AW4 torque converter lockup solenoid |
| 42 | ASD relay | ASD relay wiring or relay failure |
| 43 | Ignition coil | Coil driver circuit |
| 55 | End of codes | Always last |

## Pre-swap checklist
- [ ] Read and record all current codes
- [ ] CPS signal verified (no code 11)
- [ ] TPS sweep smooth, no dead spots
- [ ] MAP reads barometric at key-on engine-off
- [ ] CTS resistance at ambient matches Chrysler curve
- [ ] O2 sensor oscillating at warm idle
- [ ] All injectors clicking during cranking
- [ ] Fuel pressure at 39 psi key-on
- [ ] ASD relay activates at key-on (fuel pump primes)
- [ ] All sensor connectors inspected — no corrosion, broken locks
- [ ] Ground straps clean and tight (block-to-chassis, head-to-firewall)
