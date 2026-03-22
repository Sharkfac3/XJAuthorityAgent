# Cooling Year Changes

## Purpose
Identify the split points that most often change XJ cooling answers before maintenance, diagnostics, or parts ordering begins.

## Scope
This file is a stock-baseline routing aid. It does not attempt to list every radiator, fan, or hose variant.

## Confirm these dimensions first

### 1. Engine family
Engine family changes the cooling answer first.
At minimum, confirm whether the vehicle is using the 4.0L or 2.5L baseline before assuming radiator, hose-routing, fan-package, or thermostat-housing details.

### 2. Transmission type
Transmission type matters any time the job touches the radiator or cooler provisions.
If the vehicle is automatic, confirm whether the stock radiator family also supports transmission cooling before treating the radiator as a simple engine-cooling-only part.

### 3. A/C and fan package
A/C presence and fan-control hardware materially change auxiliary-fan assumptions.
If a cooling question involves the electric fan, relay, switch, or harness side of the system, confirm the actual fan package on the vehicle instead of assuming one stock arrangement.

### 4. Era wiring context
When a cooling job touches switches, relays, fan wiring, or harness-side connectors, load the stock era wiring context first:
- [`vehicle/era1/wiring.md`](../../era1/wiring.md)
- [`vehicle/era2/wiring.md`](../../era2/wiring.md)
- [`vehicle/era3/wiring.md`](../../era3/wiring.md)

### 5. 1996 transition-year caution
If the vehicle is a 1996 model, treat connector and harness assumptions carefully.
Use [`vehicle/era3/1996-notes.md`](../../era3/1996-notes.md) before ordering electrical-side cooling parts or assuming later-era harness details.

## Practical use
Use this file to decide whether the next stop should be:
- stock baseline work in this `vehicle/systems/cooling/` branch
- service work under [`work/maintenance/cooling/`](../../../work/maintenance/cooling/)
- symptom isolation under [`diagnostics/cooling/`](../../../diagnostics/cooling/)
- parts-selection guidance under [`sourcing/oem-vs-aftermarket/cooling/`](../../../sourcing/oem-vs-aftermarket/cooling/)

## Current limits
- radiator-family detail not yet split out
- fan-family detail not yet split out
- heater-side baseline detail not yet split out

## Next likely child files
- `fan-families.md`
- `radiator-and-tank-families.md`
- `heater-circuit-baseline.md`
