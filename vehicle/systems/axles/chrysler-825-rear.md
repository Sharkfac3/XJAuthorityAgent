# Chrysler 8.25 Rear Axle — Architecture and Advantages

## Purpose
Document the Chrysler 8.25 rear axle architecture, its bolt-in shaft retention, spline variants, and why it is the preferred stock rear axle for the XJ.

## Scope
Factory Chrysler 8.25 rear axle as installed on 1991–2001 Jeep Cherokee XJ models. This file covers architecture and comparison context — not dimensional specifications (see [stock-specs.md](stock-specs.md)).

---

## Identity

| Attribute | Value |
|-----------|-------|
| Designation | Chrysler 8.25 (also called Chrysler 8-1/4) |
| Type | Semi-float |
| Ring gear diameter | 8.25" |
| Axle tube OD | 3.0" |
| Shaft retention | **Bolt-in (flange-retained)** — no C-clips |
| Differential | Open (standard), Trac-Lok limited slip (optional) |
| Spring type | Leaf spring, spring-under-axle |

### Spline count by year

| Year range | Spline count |
|------------|-------------|
| 1991–1996 | 27-spline |
| 1997–2001 | 29-spline |

The 29-spline shafts are stronger and are the preferred configuration for any modified XJ.

### Years installed

| Year range | Status |
|------------|--------|
| 1991–1996 | Optional — installed on non-ABS models; ABS-equipped XJs received the Dana 35 |
| 1997–2001 | **Standard on all XJs** |

The Chrysler 8.25 replaced the Dana 35 as the default rear axle starting in 1997. From 1991–1996, whether an XJ received the C8.25 or Dana 35 was primarily determined by ABS: non-ABS models got the C8.25, ABS-equipped models got the Dana 35. This was not tied to a specific trim level. See [identification.md](identification.md) for details.

---

## Bolt-in shaft retention — why it matters

Unlike the Dana 35's C-clip retention, the Chrysler 8.25 uses **flange-retained (bolt-in) axle shafts**. Each axle shaft has a flange at the outboard end that bolts to a retainer plate at the axle tube end. The bearing sits outboard of the axle tube, and the flange/retainer physically prevents the shaft from sliding out.

**If a Chrysler 8.25 axle shaft breaks, the wheel stays attached to the vehicle.** The bearing and retainer plate hold the hub in place mechanically, regardless of shaft condition. This eliminates the most dangerous failure mode of the Dana 35.

---

## Trac-Lok limited slip differential

The Trac-Lok was a factory option on the Chrysler 8.25. It is the same **friction-disc (clutch-pack) type** limited slip as offered on the Dana 35.

| Attribute | Detail |
|-----------|--------|
| Type | Friction disc (clutch pack) |
| Gear oil requirement | **Must use friction modifier additive** (limited-slip additive) in the gear oil |
| Identification | Axle ID tag on the differential cover or axle tube. Alternatively: jack up both rear wheels, place in neutral, rotate one wheel — if the other turns the same direction, it has Trac-Lok. |
| Maintenance | Clutch packs wear over time. A worn Trac-Lok progressively acts more like an open diff. Clutch pack rebuild is possible. |
| Friction modifier | Without friction modifier additive, the clutch packs chatter on tight turns (a characteristic chirping/barking sound from the rear). This is the most common complaint and is solved by draining the gear oil and refilling with the correct additive. |

---

## Ring and pinion ratios

Factory-installed gear ratios for the XJ Chrysler 8.25:

| Ratio | Typical application |
|-------|-------------------|
| 3.07 | Highway-oriented, automatic transmission |
| 3.55 | Most common 4.0L / automatic combination |
| 3.73 | Common on 4.0L / manual transmission |

The Chrysler 8.25 was not factory-paired with a 4.10 ratio in XJs (4.10 was a 4-cylinder ratio on the Dana 35). Aftermarket 4.10 and 4.56 gear sets are available.

The front and rear axle ratios must always match. Mismatched ratios cause driveline binding in 4WD.

---

## Why the Chrysler 8.25 is preferred over the Dana 35

| Attribute | Dana 35 | Chrysler 8.25 |
|-----------|---------|---------------|
| Ring gear diameter | 7.5625" | **8.25"** |
| Axle tube OD | 2.5" | **3.0"** |
| Spline count | 27 | 27 (91–96) / **29 (97–01)** |
| Shaft retention | C-clip (dangerous failure mode) | **Bolt-in (wheel stays on)** |
| Practical strength ceiling | ~31" tires | **~35" tires** |
| Relative strength | Weakest XJ rear axle | **Comparable to Dana 44** |

The Chrysler 8.25 is a direct bolt-in replacement for the Dana 35 on any XJ. Same spring pad spacing, same width, same bolt pattern. A junkyard 8.25 from a 1997–2001 XJ is the single most cost-effective rear axle upgrade available.

---

## How to identify a Chrysler 8.25

If you are unsure whether your XJ has a Dana 35 or Chrysler 8.25:

| Method | Dana 35 | Chrysler 8.25 |
|--------|---------|---------------|
| Differential cover shape | Round, 10 bolts | Roughly oval/irregular shape, 10 bolts |
| Axle tube diameter | 2.5" — visibly thinner | 3.0" — noticeably thicker |
| Axle ID tag | Stamped tag on axle tube or diff cover reads "Dana 35" or "Model 35" | Tag reads "8-1/4" or "8.25" with ratio and build date |
| Year shortcut | 1984–1990: Dana 35. 1991–1996: Dana 35 if ABS-equipped | 1991–1996 non-ABS: likely C8.25. 1997–2001: always C8.25 |

---

## Dimensional specifications
For complete dimensional specs (housing width, tube OD, spring pad measurements, weight), see [stock-specs.md](stock-specs.md).

## Cross-links
- Axle identification guide: [identification.md](identification.md)
- Gear ratio identification: [gear-ratio-identification.md](gear-ratio-identification.md)
- Locker and LSD options: [locker-options.md](locker-options.md)
- Stock specs and dimensions: [stock-specs.md](stock-specs.md)
- Axle family overview and year matrix: [overview.md](overview.md)
- Dana 35 rear axle and C-clip failure: [dana35-rear.md](dana35-rear.md)
- Dana 30 front axle: [dana30-front.md](dana30-front.md)

## Boundary links
- Rear axle swap execution: [`../../../work/swaps/axles/index.md`](../../../work/swaps/axles/index.md)
- Axle sourcing and interchange: `sourcing/interchange/axles/`

## Sources
Community-verified via NAXJA, JeepForum, CherokeeTalk, CherokeeForum; cross-referenced against Chrysler parts catalog data and aftermarket gear set specifications.
