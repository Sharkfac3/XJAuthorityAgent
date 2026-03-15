# Era 1: Trigger System

## Crank position sensor (CPS)
- Type: Variable Reluctance (VR) — passive magnetic, sine wave output
- Location: Driver's side bellhousing
- Reads: Toothed ring on flywheel (manual) or flexplate (automatic)
- Pattern: **Renix 66-2-2-2** — 66 base teeth with three evenly-spaced gaps at 120° apart
- Signal amplitude: Increases with RPM. Weak at cranking speed — known failure point
- Air gap: Critical. Wear on flywheel/flexplate changes gap and reduces signal

## Cam position sensor
- Type: Hall effect — active, square wave output (0V / 5V)
- Location: Inside the distributor body
- Purpose: Required — the 66-2-2-2 crank pattern is radially symmetrical and cannot determine engine phase alone. Cam signal tells the ECU which cylinder is on compression stroke.

## Distributor
- Conventional cap-and-rotor unit
- Houses the cam sensor — is not itself an optical trigger
- No optical disc — this is a common misconception

## Open source ECU configuration
- rusEFI trigger name: **Renix 66/2/2/2**
- Speeduino trigger name: **Renix 44-2-2** (auto-scales to 66-2-2-2 when cylinders = 6)
- Input type: VR (not Hall) — set accordingly in ECU software
- Cam sync: Required for sequential injection and accurate ignition timing

## Swap notes
- Renix CPS signal at cranking RPM is weak. Verify the open source ECU's VR input sensitivity before committing, or plan for a VR signal conditioner.
- The Renix flywheel/flexplate pattern is NOT interchangeable with Era 2/3 — different tooth count and spacing.
- Swapping in an Era 2/3 flywheel/flexplate is a valid path to use the more common Jeep 18-2-2-2 pattern, but requires verifying flywheel compatibility with the manual transmission or flexplate with the AW4.
