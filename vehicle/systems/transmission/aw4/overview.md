# AW4 Overview

## Purpose
Provide the stock Jeep XJ baseline for the AW4 automatic transmission.

## Scope
Factory AW4 identity, stock control relationships, and stock operating facts that matter before maintenance, diagnostics, or swap work.

## Identity
- Full name: Aisin Warner 4-speed automatic
- XJ years: 1987–2001
- Forward gears: 4
- Reverse gears: 1
- Uses a torque converter with lockup

## Stock control relationships
### TCM and TPS
The AW4 transmission control module reads throttle position sensor voltage directly from the engine harness.

In stock form, that TPS signal affects:
- shift aggressiveness and kickdown behavior
- torque-converter lockup timing

Expected TPS range at the AW4/TCM side:
- closed throttle: about 0.5 V
- wide open throttle: about 4.5 V
- reference supply: 5 V
- signal type: continuous analog voltage

### Torque-converter lockup
In stock form, the converter clutch is part of normal highway-speed operation to reduce slip and heat and improve fuel economy.

## Stock architecture notes
- The AW4 uses a dedicated transmission control module rather than direct serial communication with the engine ECU.
- The TPS signal branch to the TCM is part of the stock harness architecture and matters any time engine-management wiring is changed.

## Modified-state pointer
If the vehicle is getting an aftermarket or open-source ECU, do not use this file as the wiring procedure.

Use:
- `work/swaps/ecu/integration/aw4-tps.md` for ECU-swap TPS-sharing procedure
- `work/swaps/ecu/index.md` for the full ECU-swap workflow

## Detailed AW4 leaf
For gear ratios, fluid spec, solenoid logic, and common failures, see the flat leaf file:
- [`../aw4.md`](../aw4.md)
