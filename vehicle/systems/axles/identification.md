# Axle Identification Guide

## Purpose
How to identify which axles a specific Jeep Cherokee XJ has — by year, by visual inspection, and by axle tag.

## Scope
Factory axle identification on 1984–2001 XJ. Does not cover aftermarket or donor axles.

---

## Quick lookup by year

| Year range | Front axle | Rear axle (standard) | Rear axle (if optioned) |
|------------|-----------|---------------------|------------------------|
| 1984–1986 | Dana 30 (260 U-joints) | Dana 35 | — |
| 1987–1989 | Dana 30 (260 U-joints) | Dana 35 | Dana 44 (Tow Package) |
| 1990 | Dana 30 (260 U-joints) | Dana 35 | — |
| 1991–1994 | Dana 30 (260 U-joints) | Dana 35 | Chrysler 8.25 (27-spline) |
| 1995–1996 | Dana 30 (297 U-joints) | Dana 35 | Chrysler 8.25 (27-spline) |
| 1997–2001 | Dana 30 (297 U-joints) | Chrysler 8.25 (29-spline) | — |

**2WD models** have no front axle assembly. Rear axle follows the same matrix.

For full specs, see [stock-specs.md](stock-specs.md). For the narrative year/package matrix, see [overview.md](overview.md).

---

## Front axle — Dana 30

Every 4WD XJ from 1984–2001 used the Dana 30 front axle. No exceptions.

**No XJ ever came with a Dana 44 front axle from the factory.** This is a common misconception. The Dana 44 was available only as a *rear* axle on 1987–1989 Tow Package XJs. The confusion likely comes from the fact that other Jeep platforms (TJ Rubicon, full-size) used Dana 44 front axles — the XJ did not.

How to confirm a Dana 30 front:
- "Dana 30" is cast into the differential housing
- Stamped metal ID tag on the axle tube near the differential
- Open-knuckle design with leaf springs (spring-under-axle)

For architecture details, see [dana30-front.md](dana30-front.md).

---

## Rear axle identification

Three factory rear axles were used in the XJ: Dana 35, Chrysler 8.25, and Dana 44 (rare). The methods below will tell them apart.

### By axle ID tag

Most axles have a stamped metal tag attached to the differential housing or axle tube with a bolt. The tag typically includes:
- Axle model (e.g., "Model 35", "8-1/4")
- Gear ratio
- Build date
- Trac-Lok indicator (if equipped)

| Axle | Tag location |
|------|-------------|
| Dana 35 | Tag on a differential cover bolt or axle tube near the diff |
| Chrysler 8.25 | Tag on a differential cover bolt or axle tube near the diff |
| Dana 44 | Tag on the differential housing |

Tags can be missing, corroded, or painted over. If the tag is unreadable, use visual identification below.

### By visual inspection

#### Differential cover shape — the fastest visual tell

| Feature | Dana 35 | Chrysler 8.25 | Dana 44 |
|---------|---------|---------------|---------|
| Cover shape | Round | Roughly rectangular with a flat bottom section (~3–4" wide) | Round, larger diameter than Dana 35 |
| Cover bolt count | 10 | 10 | 10 |

Look at the bottom of the differential from underneath the vehicle. If there is a flat section on the bottom of the cover, roughly 3–4 inches wide, it is a Chrysler 8.25. If the cover is completely round, it is either a Dana 35 or Dana 44.

#### Axle tube diameter — the fastest measurable tell

Wrap a tape measure around the axle tube:

| Circumference | Tube OD | Axle |
|---------------|---------|------|
| ~7.85" | 2.5" | Dana 35 |
| ~9.42" | 3.0" | Chrysler 8.25 |
| ~9.82" | 3.125" | Dana 44 |

The difference between a 2.5" Dana 35 tube and a 3.0" Chrysler 8.25 tube is obvious by hand even without a tape measure.

#### Axle shaft retention — C-clip vs. bolt-in

Look at the outboard end of the axle tube near the wheel:

- **No retainer plate visible** → C-clip retention → **Dana 35**
- **Retainer plate with 4 bolts at the wheel hub flange** → bolt-in retention → **Chrysler 8.25 or Dana 44**

To distinguish a bolt-in C8.25 from a bolt-in Dana 44, use the tube diameter or cover shape checks above.

### By VIN or build sheet

The VIN alone does not reliably encode which rear axle is installed, especially on 1991–1996 XJs where both the Dana 35 and Chrysler 8.25 were possible. A factory build sheet or original window sticker is more reliable. Build sheets can be requested from Chrysler/Stellantis by VIN.

---

## ABS and the Chrysler 8.25 (1991–1996)

On 1991–1996 XJs, the determining factor for which rear axle was installed was **ABS**:

- **Non-ABS models** → most likely received the Chrysler 8.25 (27-spline)
- **ABS-equipped models** → received the Dana 35

This was not tied to a specific trim level. Any non-ABS Cherokee from 1991–1996 could have the C8.25 regardless of whether it was a base, Sport, or Country model.

From 1997 onward, the Chrysler 8.25 (29-spline) became standard across all XJs regardless of ABS.

---

## AMC Model 20 — not an XJ axle

The AMC Model 20 rear axle is sometimes confused with XJ axles because parts (such as pinion seals) can interchange with the Dana 35 due to similar dimensions. However, **no XJ ever used the AMC Model 20.** That axle belongs to the CJ series and full-size SJ Wagoneer/Cherokee platforms. All XJs from 1984 onward used the Dana 35 as the base rear axle.

---

## Cross-links

- Dana 30 front architecture → [dana30-front.md](dana30-front.md)
- Dana 35 rear architecture and C-clip failure modes → [dana35-rear.md](dana35-rear.md)
- Chrysler 8.25 rear architecture → [chrysler-825-rear.md](chrysler-825-rear.md)
- Stock specs and dimensions → [stock-specs.md](stock-specs.md)
- Axle family overview and year matrix → [overview.md](overview.md)
- Gear ratio identification → [gear-ratio-identification.md](gear-ratio-identification.md)
- Locker and limited-slip options → [locker-options.md](locker-options.md)

## Boundary links

- Axle swap execution → [`../../../work/swaps/axles/index.md`](../../../work/swaps/axles/index.md)
- 4WD engagement and front axle disconnect → [`../4wd/overview.md`](../4wd/overview.md)
