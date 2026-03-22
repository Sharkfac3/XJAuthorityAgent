# Wiring: AW4 TPS Interaction

## The problem
The AW4 automatic transmission TCM reads TPS voltage directly from the engine harness to control shift points and torque converter lockup. This wire is tapped from the TPS signal wire and runs to the TCM independently.

When the stock ECU is replaced, the TPS signal must remain intact and within the AW4's expected voltage range. Cutting, re-routing, or changing this wire will alter transmission behavior.

## What the AW4 expects
- Closed throttle: 0.5V
- Wide open throttle: 4.5V
- Reference: 5V
- Signal: Continuous analog — the TCM reads it in real time

## Where the tap lives
The TPS signal wire branches in the engine harness — one leg goes to the ECU, one leg goes to the AW4 TCM via the firewall connector. Both legs must remain connected.

## Correct wiring with open source ECU

```
TPS signal wire (from TPS sensor)
    ├── → Open source ECU TPS input pin
    └── → AW4 TCM (via existing harness tap — do not cut)
```

The open source ECU TPS input is high impedance — sharing the signal with the AW4 does not load the circuit enough to cause problems.

## Symptoms of incorrect TPS-to-AW4 wiring
- Harsh or erratic upshifts
- No torque converter lockup at highway speed
- Transmission shifts at wrong throttle positions
- Kickdown not functioning

## Torque converter lockup wiring
The TCC (torque converter clutch) solenoid is a separate circuit from the TPS signal. It receives a ground-side command from the ECU/TCM to engage lockup.

For stock AW4 baseline and control relationships, see `vehicle/systems/transmission/aw4/overview.md`.
For the target-state work-branch route during migration, see `work/swaps/ecu/integration/aw4-tps.md`.
