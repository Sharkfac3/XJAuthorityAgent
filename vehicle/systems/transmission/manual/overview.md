# Manual Transmission Overview

## Purpose
Provide the stock Jeep XJ baseline for factory manual-transmission families.

## Scope
Factory manual-transmission identity, year-family splits, and stock operating facts that matter before maintenance, diagnostics, or swap work.

## Factory manual families
| Transmission | Years | Notes |
|---|---|---|
| BA10/5 | 1988–1989 | Peugeot-sourced 5-speed. Known as weak and often replaced with AX15. |
| AX5 | 1988–1994 | Aisin 5-speed used behind the 2.5L. Adequate for stock power levels. |
| AX15 | 1989–2001 | Aisin 5-speed used behind the 4.0L. Preferred factory manual in the XJ. |

## Stock control relationships
Manual transmissions do not use a separate transmission control module.

There is no AW4-style TPS-sharing requirement, no lockup-solenoid control path, and no transmission-specific ECU coexistence issue in normal manual-transmission configurations.

## Stock architecture notes
- Clutch-switch presence and function vary by year and configuration.
- Some years may use neutral or clutch inputs that matter to idle behavior, start interlock, or decel fuel logic.
- Confirm the actual year-era wiring before changing engine-management architecture.

## Modified-state pointer
If the question is about an aftermarket or open-source ECU swap, use this file only for the stock baseline.

Then route into:
- `work/swaps/ecu/` for ECU-swap execution work
