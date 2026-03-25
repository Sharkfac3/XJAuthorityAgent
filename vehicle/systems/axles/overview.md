# Axles Overview

## Purpose
Stock XJ axle families, variants, and year/package differences.

## Scope
Factory axle configurations for the 1984–2001 Jeep Cherokee XJ. This branch covers what the XJ left the factory with — not aftermarket upgrades or donor swaps.

## What belongs here
- stock axle architecture and component families
- factory year, era, package, or drivetrain splits
- links to narrower factual leaves as this branch grows

## What does not belong here
- service or installation procedures → `work/`
- symptom-first diagnostics → `diagnostics/`
- donor-part sourcing or interchange → `sourcing/`
- swap execution → `work/swaps/axles/`

---

## Stock axle families

### Front — Dana 30
Every 4WD XJ from 1984–2001 used the Dana 30 front axle. Open-knuckle, reverse-cut ring gear, leaf-sprung. Key year split: 1995+ ABS models got the stronger 297-size inner U-joints (earlier models use 260-size).

### Rear — Dana 35
The default rear axle for most XJ years. Semi-float with C-clip shaft retention. Adequate for stock tires but the weakest link for any modified XJ. Not recommended past 31" tires.

### Rear — Chrysler 8.25
Available 1992–2001 and standard on 1997–2001 models. Bolt-in shafts (no C-clips), 29-spline on 97+. Comparable in strength to a Dana 44. The best stock rear axle commonly found in XJs.

### Rear — Dana 44 (Tow Package only)
1987–1989 XJs with the factory Towing Package received a Dana 44 rear. 30-spline, bolt-in shafts. Direct bolt-in to any XJ. Extremely rare find.

## Year / package matrix

| Year range | Front | Rear (standard) | Rear (optional/package) |
|------------|-------|-----------------|------------------------|
| 1984–1986 | Dana 30 (260 U-joints) | Dana 35 | — |
| 1987–1989 | Dana 30 (260 U-joints) | Dana 35 | Dana 44 (Tow Package) |
| 1990–1991 | Dana 30 (260 U-joints) | Dana 35 | — |
| 1992–1994 | Dana 30 (260 U-joints) | Dana 35 | Chrysler 8.25 (27-spline) |
| 1995–1996 | Dana 30 (297 U-joints, ABS) | Dana 35 | Chrysler 8.25 (27-spline) |
| 1997–2001 | Dana 30 (297 U-joints, ABS) | Chrysler 8.25 (29-spline) | — |

**2WD models:** No front axle assembly. Rear axle follows the same matrix.

## Child leaves
- [stock-specs.md](stock-specs.md) — dimensional and specification tables for every stock XJ axle variant

## Expected child branches
- `year-changes.md` when time-based splits become substantial
- `variants.md` when multiple stock families need separation
