# Era 2: Idle Air Control (IAC) Valve

## Specs
- Type: 4-wire stepper motor
- Coil resistance: ~50–55 ohm per coil
- Wiring: Coil A (A+, A−) and Coil B (B+, B−)
- Step range: ~0 (fully closed) to ~125 steps (fully open)
- Connector: Metri-Pack 150 — see `swap/wiring/connectors/metri-pack/mp150-3pin.md`
- Location: Throttle body

## Testing
- Measure resistance across each coil pair — should be ~50 ohm
- At key-on, listen for stepping/clicking as ECU initializes position
- Cross-coil resistance (A to B terminal) should be open circuit

## Swap notes
- Same stepper motor type as Era 1 — same open source ECU support considerations apply
- Carbon buildup on pintle is common — clean before condemning
- See `swap/ecu-selection/iac-strategy.md` for options if open source ECU lacks native stepper support
