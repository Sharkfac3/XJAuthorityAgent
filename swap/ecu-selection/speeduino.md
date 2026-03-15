# ECU Selection: Speeduino

## What it is
Speeduino is an open source ECU hardware and firmware project. Hardware is available as a DIY kit or pre-assembled board from multiple vendors. Firmware is actively maintained. Tuning is done via TunerStudio MS software.

## XJ trigger support
- Era 1 Renix: **Renix 44-2-2** trigger pattern — auto-scales to 66-2-2-2 for 6-cylinder configuration
- Era 2 / Era 3: Jeep 18-2-2-2 — confirm in current firmware documentation before purchasing

## IAC support
Speeduino supports 4-wire stepper motor IAC natively on boards with stepper driver circuitry. Confirm the specific board variant includes the stepper driver — not all Speeduino boards do. See `swap/ecu-selection/iac-strategy.md`.

## Ignition outputs
Standard Speeduino boards provide up to 4 ignition outputs. Sufficient for Era 3 2000–2001 waste spark (3 outputs needed).

## Strengths for XJ application
- Strong community with documented XJ installs
- TunerStudio is well-documented and beginner-accessible
- Hardware is inexpensive relative to other options
- Renix 44-2-2 trigger is specifically named — Era 1 owners have a clear path

## Considerations
- Hardware quality varies by vendor — research current recommended vendors before purchasing
- Firmware updates are frequent — check compatibility with TunerStudio version
- Board form factor varies — verify physical dimensions fit chosen enclosure

## Community resources
- Speeduino forum: speeduino.com/forum
- TunerStudio documentation: tunerstudio.com
- XJ-specific threads: Search "Jeep XJ Speeduino" on Speeduino forum and NAXJA forum

⚠️ Open source projects evolve. Verify all trigger pattern names and feature support against current firmware documentation — do not rely solely on this file.
