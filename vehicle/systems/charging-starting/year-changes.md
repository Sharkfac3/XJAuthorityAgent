# Charging Starting Year Changes

## Purpose
Identify the split points that most often change XJ charging and starting answers.

## Scope
This file is a stock-baseline routing aid for battery, cable, starter, alternator, and power-distribution questions. It is not a full parts catalog.

## Confirm these dimensions first

### 1. Era and power-distribution layout
Era is the first charging-and-starting split.
Fuse, relay, and harness expectations change enough by era that cable routing, relay checks, and connector assumptions should not be copied blindly across the full production run.

Load the matching stock wiring context first when the job touches the harness side:
- [`vehicle/era1/wiring.md`](../../era1/wiring.md)
- [`vehicle/era2/wiring.md`](../../era2/wiring.md)
- [`vehicle/era3/wiring.md`](../../era3/wiring.md)

### 2. 1996 transition-year caution
1996 uses a mixed architecture.
Before assuming later-era connector or harness details, read [`vehicle/era3/1996-notes.md`](../../era3/1996-notes.md).

### 3. Engine family and accessory drive
Engine family can change alternator mounting, bracket assumptions, and belt-drive context.
Confirm the actual engine baseline before treating alternator service or belt routing as universal.

### 4. Work type matters
Charging and starting questions split quickly by intent:
- stock baseline and architecture stay here in `vehicle/`
- service work belongs under [`work/maintenance/charging-starting/`](../../../work/maintenance/charging-starting/)
- symptom isolation belongs under [`diagnostics/charging-and-starting/`](../../../diagnostics/charging-and-starting/)
- part-choice questions belong under [`sourcing/interchange/electrical/`](../../../sourcing/interchange/electrical/)

## Current limits
- alternator family detail not yet split out
- starter family detail not yet split out
- grounds and power-distribution detail not yet split out

## Next likely child files
- `battery-and-cable-baseline.md`
- `alternator-families.md`
- `starter-and-solenoid-baseline.md`
- `grounds-and-power-distribution.md`
