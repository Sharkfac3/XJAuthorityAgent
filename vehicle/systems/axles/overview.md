# Axles Overview

**Branch router:** [index.md](index.md)

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
Available 1991–2001 and standard on 1997–2001 models. On 1991–1996 XJs, the determining factor was ABS: non-ABS models received the C8.25, ABS-equipped models got the Dana 35. Bolt-in shafts (no C-clips), 29-spline on 97+. Comparable in strength to a Dana 44. The best stock rear axle commonly found in XJs.

### Rear — Dana 44 (Tow Package only)
1987–1989 XJs with the factory Towing Package received a Dana 44 rear. 30-spline, bolt-in shafts. Direct bolt-in to any XJ. Extremely rare find.

## Year / package matrix

| Year range | Front | Rear (standard) | Rear (optional/package) |
|------------|-------|-----------------|------------------------|
| 1984–1986 | Dana 30 (260 U-joints) | Dana 35 | — |
| 1987–1989 | Dana 30 (260 U-joints) | Dana 35 | Dana 44 (Tow Package) |
| 1990 | Dana 30 (260 U-joints) | Dana 35 | — |
| 1991–1994 | Dana 30 (260 U-joints) | Dana 35 | Chrysler 8.25 (27-spline, non-ABS) |
| 1995–1996 | Dana 30 (297 U-joints) | Dana 35 | Chrysler 8.25 (27-spline, non-ABS) |
| 1997–2001 | Dana 30 (297 U-joints, ABS) | Chrysler 8.25 (29-spline) | — |

**2WD models:** No front axle assembly. Rear axle follows the same matrix.

## Child leaves
- [identification.md](identification.md) — how to identify which axle your XJ has by year, visual inspection, and tag
- [gear-ratio-identification.md](gear-ratio-identification.md) — how to read or count gear ratios, factory ratio options, and ratio selection for tire changes
- [locker-options.md](locker-options.md) — factory Trac-Lok and aftermarket locker/LSD options by axle
- [stock-specs.md](stock-specs.md) — dimensional and specification tables for every stock XJ axle variant
- [dana30-front.md](dana30-front.md) — Dana 30 front axle architecture, axle shaft types (CV vs. U-joint by year), and known weak points
- [dana35-rear.md](dana35-rear.md) — Dana 35 rear axle C-clip retention, failure modes, and mitigation options
- [chrysler-825-rear.md](chrysler-825-rear.md) — Chrysler 8.25 rear axle bolt-in retention, spline variants, and Trac-Lok

## Related branches
- 4WD engagement and front axle disconnect: [`../4wd/overview.md`](../4wd/overview.md)
