# Era 1: Idle Air Control (IAC) Valve

## Specs
- Type: 4-wire stepper motor
- Coil resistance: ~50–55 ohm per coil
- Wiring: Coil A (A+, A−) and Coil B (B+, B−)
- Step range: ~0 (fully closed) to ~125 steps (fully open)
- Location: Throttle body

## Testing
- Measure resistance across each coil pair — should be ~50 ohm
- At key-on, listen for stepping/clicking as ECU initializes IAC position
- Resistance between any A and B terminal should be open circuit

## Swap notes
- Open source ECU must support 4-wire stepper motor IAC output
- If ECU does not support stepper IAC natively, options are: add-on stepper driver board, swap to a 2-wire PWM IAC valve (requires physical adapter at throttle body), or manual idle air bypass screw (trail-only builds)
- The B+ latch relay on Era 1 exists specifically to let the IAC reset at key-off — see `vehicle/era1/power-relay.md`
- Carbon buildup on the valve pintle is common — clean with throttle body cleaner before condemning
