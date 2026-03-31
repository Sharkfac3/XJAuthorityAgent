# Transmission Overview

## Purpose
Route stock Jeep XJ transmission facts and provide the year/family baseline.

## Scope
Factory transmission families, year splits, gear ratios, and stock control baselines.

## Use this branch for
- identifying which transmission a given XJ was built with
- stock gear ratios and operating characteristics
- factory control relationships that affect wiring and behavior
- year or family differences that matter before maintenance, diagnostics, or swap work

## Do not use this branch for
- service or installation procedures → `work/`
- symptom-first diagnostics → `diagnostics/`
- donor or purchasing guidance → `sourcing/`
- ECU-swap execution steps → `work/swaps/ecu/`

---

## Factory transmission matrix

| Year | Engine | Transmission | Type |
|------|--------|--------------|------|
| 1987–early 1989 | 4.0L I6 | BA-10/5 | 5-speed manual (Peugeot) |
| 1989–1999 | 4.0L I6 | AX-15 | 5-speed manual (Aisin) |
| 2000–2001 (SE only) | 4.0L I6 | NV3550 | 5-speed manual (New Venture) |
| 1988–1994 | 2.5L I4 | AX-5 | 5-speed manual (Aisin) |
| 1987–2001 | 4.0L I6 | AW4 | 4-speed automatic (Aisin Warner) |
| 1987–1990 | 2.5L I4 | AW4 | 4-speed automatic (Aisin Warner) |

Notes:
- The AX-15 replaced the BA-10/5 mid-model-year 1989 (approximately March 1989 production).
- The 4.0L was never offered with a 3-speed automatic — the AW4 is the only automatic option.
- The NV3550 appeared only in 2000–2001 SE trim; most late XJs still have the AX-15.
- 2WD XJs have a transmission but no transfer case.

---

## Leaf files

| File | Content |
|------|---------|
| [`aw4.md`](aw4.md) | AW4 gear ratios, fluid spec, shift solenoids, TPS dependency, common failures |
| [`ax15.md`](ax15.md) | AX-15 gear ratios, fluid spec, known strengths and failure points |
| [`ba10.md`](ba10.md) | BA-10/5 identity, known failure modes, AX-15 swap context |

Deeper routing files (wiring, ECU relationships):
- [`aw4/overview.md`](aw4/overview.md) — AW4 TCM/TPS wiring context and ECU-swap pointer
- [`manual/overview.md`](manual/overview.md) — Manual transmission stock control notes

---

## Boundary links
- AW4 TPS wiring in ECU-swap context: `work/swaps/ecu/integration/aw4-tps.md`
- Full ECU-swap workflow: `work/swaps/ecu/index.md`
- Transfer case families: [`../transfer-case/overview.md`](../transfer-case/overview.md)

## Sources
Community-verified via NAXJA, JeepForum, CherokeeTalk; cross-referenced against Novak Conversions technical guides and Jeep Cherokee TSBs.
