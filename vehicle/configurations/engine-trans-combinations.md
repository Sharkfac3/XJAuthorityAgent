# Engine And Transmission Combinations

## Purpose
Provide a first-hop stock matrix for XJ engine and transmission combinations that materially change stock facts, diagnostics, work routing, and ECU-swap planning.

## Scope
Use this file to narrow the vehicle before assuming TPS wiring, trigger hardware, cooling details, or transmission control behavior.

## Confirmed factory transmission families in current canon
| Transmission | Type | Confirmed years in current canon | Confirmed engine relationship in current canon |
|---|---|---|---|
| AW4 | Automatic | 1987–2001 | Automatic family used in the XJ. Confirm the actual engine and year before assuming cooling, wiring, or sensor details. |
| BA10/5 | Manual | 1988–1989 | Factory manual family documented in current canon. |
| AX5 | Manual | 1988–1994 | Used behind the 2.5L. |
| AX15 | Manual | 1989–2001 | Used behind the 4.0L. |

## High-value split points

### AW4 automatic vs manual matters immediately
If the Jeep has an AW4:
- load [`../systems/transmission/aw4/overview.md`](../systems/transmission/aw4/overview.md)
- preserve the TPS-to-TCM relationship on automatic-era wiring questions
- remember automatic vehicles use a flexplate, not a flywheel, in trigger-system context

If the Jeep has a manual transmission:
- load [`../systems/transmission/manual/overview.md`](../systems/transmission/manual/overview.md)
- there is no AW4-style TPS-sharing requirement
- trigger-system context uses a flywheel, not a flexplate

### 4.0L manual baseline in current canon
Current canon explicitly confirms:
- AX15 is the preferred factory manual behind the 4.0L: [`../systems/transmission/manual/overview.md`](../systems/transmission/manual/overview.md)
- 1988–1989 also includes BA10/5 as an early factory manual family: [`../systems/transmission/manual/overview.md`](../systems/transmission/manual/overview.md)

### 2.5L manual baseline in current canon
Current canon explicitly confirms:
- AX5 is the factory manual family documented behind the 2.5L for 1988–1994: [`../systems/transmission/manual/overview.md`](../systems/transmission/manual/overview.md)

## Why this matrix matters

### Wiring and control assumptions
Automatic XJs with AW4 use a TCM that reads TPS voltage directly from the engine harness.
That changes diagnosis, wiring preservation, and aftermarket ECU integration.

Relevant files:
- [`../systems/transmission/aw4/overview.md`](../systems/transmission/aw4/overview.md)
- [`../../work/swaps/ecu/integration/aw4-tps.md`](../../work/swaps/ecu/integration/aw4-tps.md)

### Trigger and starting context
Across the era trigger files, the crank sensor reads a toothed ring on:
- the **flywheel** on manual vehicles
- the **flexplate** on automatic vehicles

Relevant files:
- [`../era1/trigger.md`](../era1/trigger.md)
- [`../era2/trigger.md`](../era2/trigger.md)
- [`../era3/trigger.md`](../era3/trigger.md)

### Cooling and service assumptions
Current canon already warns that radiator-family assumptions can change when the vehicle is automatic because the stock radiator may also support transmission cooling.

Relevant file:
- [`../systems/cooling/year-changes.md`](../systems/cooling/year-changes.md)

## Current limits
This file is a first-hop narrowing tool, not a complete VIN-decoder matrix.
Current canon does **not** yet fully split:
- every year-by-year engine/transmission pairing
- complete 2.5L automatic coverage
- package-specific drivetrain combinations

If a precise factory pairing question cannot be answered from this file alone, narrow next by:
1. year or era → [`../years/index.md`](../years/index.md)
2. transmission family → [`../systems/transmission/overview.md`](../systems/transmission/overview.md)
3. engine family if cooling or service assumptions depend on it

## Cross-links
- Configuration routing root: [`index.md`](index.md)
- 2WD vs 4WD baseline: [`2wd-vs-4wd.md`](2wd-vs-4wd.md)
- ABS vs non-ABS baseline: [`abs-vs-non-abs.md`](abs-vs-non-abs.md)
