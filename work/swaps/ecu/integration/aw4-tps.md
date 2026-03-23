# AW4 TPS Integration

## Purpose
Keep the AW4 automatic transmission control module seeing a correct TPS signal during an aftermarket ECU swap.

## The problem
The AW4 automatic transmission TCM reads TPS voltage directly from the engine harness to control shift points and torque converter lockup. This wire is tapped from the TPS signal wire and runs to the TCM independently.

When the stock ECU is replaced, the TPS signal must remain intact and within the AW4's expected voltage range. Cutting, rerouting, or changing this wire will alter transmission behavior.

## What the AW4 expects
- Closed throttle: 0.5 V
- Wide open throttle: 4.5 V
- Reference: 5 V
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

## Use these files together
- stock AW4 baseline: [`../../../../vehicle/systems/transmission/aw4/overview.md`](../../../../vehicle/systems/transmission/aw4/overview.md)
- wiring strategy: [`../wiring/index.md`](../wiring/index.md)
- main ECU swap router: [`../index.md`](../index.md)
