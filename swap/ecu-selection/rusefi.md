# ECU Selection: rusEFI

## What it is
rusEFI is an open source ECU firmware project with multiple supported hardware platforms. Tuning is done via TunerStudio. Hardware options range from DIY boards to pre-assembled units with professional enclosures.

## XJ trigger support
rusEFI has a dedicated Jeep section with named trigger patterns:
- Era 1 Renix: **Renix 66/2/2/2** — explicitly named and supported
- Era 2 / Era 3: **Jeep 18-2-2-2** — explicitly named and supported
- See: github.com/rusefi/rusefi/wiki/All-Supported-Triggers (Jeep & Renix section)

## IAC support
rusEFI supports 4-wire stepper motor IAC on hardware platforms with stepper driver outputs. Confirm the specific hardware platform includes stepper outputs. See `swap/ecu-selection/iac-strategy.md`.

## Ignition outputs
Most rusEFI hardware platforms support multiple ignition outputs. Verify the specific board supports 3 outputs for Era 3 2000–2001 waste spark configuration.

## Strengths for XJ application
- Both Renix and Jeep 18-2-2-2 patterns explicitly named — no guesswork
- Strong firmware development team and active community
- Hardware options at multiple price points
- Frankenso and Proteus boards are commonly used for XJ installs

## Considerations
- More hardware platform variety than Speeduino — research which platform suits the application
- rusEFI firmware and TunerStudio ini files update frequently — maintain version alignment
- Some hardware platforms are better suited to professional installation than DIY

## Community resources
- rusEFI forum: rusefi.com/forum
- rusEFI wiki: github.com/rusefi/rusefi/wiki
- Discord: Active development and support community
- Trigger reference: github.com/rusefi/rusefi/wiki/All-Supported-Triggers

⚠️ Open source projects evolve. Verify all trigger pattern names and feature support against current firmware documentation — do not rely solely on this file.
