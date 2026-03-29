# Differential Locker and Limited Slip Options

## Purpose
Factory and aftermarket differential locking options for XJ axles. Covers locker types, axle compatibility, and why lockers matter for off-road use.

## Scope
Options for factory XJ axle housings: Dana 30 front, Dana 35 rear, Chrysler 8.25 rear. Does not cover one-ton swap axles — see [`work/swaps/axles/support-work/gearing-install.md`](../../../work/swaps/axles/support-work/gearing-install.md) for locker selection on Dana 60 and Sterling 10.50.

---

## Why lockers matter

An **open differential** (the factory default on most XJs) sends torque to the wheel with the **least resistance**. This is fine on pavement where both wheels have equal traction. Off-road on uneven terrain, one wheel lifts or loses grip — that wheel spins freely while the opposite wheel gets no power.

A locker or limited-slip differential addresses this by forcing both wheels to share torque, keeping the vehicle moving when traction is unequal.

---

## Differential types explained

### Open differential
- Factory default on all XJ axles unless Trac-Lok was optioned
- Splits torque evenly but allows unlimited speed difference between wheels
- Adequate for street driving; poor off-road on uneven terrain

### Limited slip differential (LSD)
- Progressively transfers torque toward the wheel with more traction
- Does not fully lock — allows some speed difference between wheels
- Factory Trac-Lok is this type (friction-disc clutch pack)
- Aftermarket examples: Detroit Truetrac (helical gear), Auburn Grip-N-Loc (cone clutch)
- Wears over time (clutch-pack types); helical-gear types have no wear components

### Automatic locker
- Locks both axle shafts together by default
- Unlocks mechanically when the outer wheel needs to turn faster in a turn
- Examples: Detroit Locker, lunchbox/drop-in lockers (Spartan, Lock-Right)
- On-road behavior: clicking or banging on tight turns, occasional tire chirp
- Full lock under power — both wheels always turn together when throttle is applied

### Selectable locker
- Driver-controlled: fully open when disengaged, fully locked when engaged
- Types: air-actuated (ARB Air Locker), cable-actuated (OX Locker), electrically actuated (OX E-Locker)
- Best of both worlds: open-diff street manners with full lock available on demand
- Requires additional hardware (onboard air compressor for ARB, cable routing for OX)
- Most expensive option but most versatile

---

## Factory Trac-Lok

Trac-Lok is Chrysler's name for their friction-disc limited slip differential. It was a factory option on the Dana 35 and Chrysler 8.25 rear axles. It was **not** available on the Dana 30 front from the factory.

How it works:
- Clutch packs (friction discs) between the side gears and the differential case
- When one wheel starts to slip, the clutch packs resist the speed difference and transfer some torque to the other wheel
- Progressive — not a hard lock. Provides a bias ratio, not 50/50 lock

Maintenance:
- **Requires friction modifier additive** in the gear oil (Mopar P/N 4318060 or equivalent)
- Without modifier: characteristic chirping or barking on tight turns
- Clutch packs wear over time and eventually the unit behaves like an open diff
- Clutch packs can be rebuilt with aftermarket kits

For Trac-Lok details specific to each axle, see [dana35-rear.md](dana35-rear.md) and [chrysler-825-rear.md](chrysler-825-rear.md).

---

## Aftermarket options by axle

### Dana 30 front

| Option | Type | Notes |
|--------|------|-------|
| ARB Air Locker | Selectable (air) | Most popular front locker for XJ; requires onboard air compressor; available for 27-spline |
| OX Locker | Selectable (cable/air/electric) | Mechanical cable actuation available — no compressor needed; also offered in air and electric versions; 27-spline and 30-spline |
| Lunchbox lockers (Spartan, Lock-Right) | Automatic (drop-in) | Budget option; replaces spider gears only, no carrier swap needed |
| Detroit Locker | Automatic (full case) | Available but **not recommended for front axle** — harsh on-road behavior, binding in turns on pavement |

**Front locker guidance:** Selectable lockers (ARB, OX) are strongly preferred for the front axle. Automatic lockers in the front cause clicking, binding, and unpredictable steering behavior on pavement. A selectable locker stays fully open during street driving and locks only when needed off-road.

For Dana 30 architecture, see [dana30-front.md](dana30-front.md).

### Dana 35 rear

A few aftermarket options exist for the Dana 35:
- Lunchbox lockers (Lock-Right, Spartan) — drop-in, budget-friendly
- ARB Air Locker — available but rarely recommended for this axle

**Community consensus: upgrade the axle before adding a locker.** The Dana 35 with its C-clip retention and 27-spline shafts is the weakest axle in the XJ. Adding a locker increases the load on an already-weak axle — with 31"+ tires, axle shaft breakage risk increases significantly. The money spent on a Dana 35 locker is better put toward a Chrysler 8.25 swap (or stronger), then adding a locker to the stronger axle.

For Dana 35 strength ceiling and failure modes, see [dana35-rear.md](dana35-rear.md).

### Chrysler 8.25 rear

The C8.25 is the recommended rear axle platform for lockers on a stock-axle XJ.

| Option | Type | Spline | Notes |
|--------|------|--------|-------|
| ARB Air Locker (RD93) | Selectable (air) | 29-spline only | Requires onboard air compressor. If your C8.25 is 27-spline (1991–1996), you must upgrade to 29-spline axle shafts to install this locker. |
| Detroit Truetrac (912A553) | Helical gear LSD | 29-spline | No clutch packs to wear; quiet; progressive torque bias. Fits 2.73 and numerically higher ratios. Do not use synthetic gear oil or friction modifiers. |
| Auburn Grip-N-Loc | Cone-clutch LSD | 27-spline and 29-spline | Available for both spline counts. Cone-clutch design with higher bias ratio than Trac-Lok. |
| Lunchbox lockers (Spartan, Lock-Right) | Automatic (drop-in) | Both | Budget option; drop-in spider gear replacement |

**29-spline note:** The ARB RD93 and Detroit Truetrac 912A553 are both 29-spline units. If you have a 1991–1996 C8.25 with 27-spline shafts, the Auburn Grip-N-Loc is the only option that fits without an axle shaft upgrade.

For C8.25 architecture and spline identification, see [chrysler-825-rear.md](chrysler-825-rear.md).

---

## Choosing a locker — summary

| Use case | Front recommendation | Rear recommendation |
|----------|---------------------|---------------------|
| Mild trail use, stock tires | Open or lunchbox | Trac-Lok rebuild or Truetrac |
| Moderate trail, 31–33" tires | ARB or OX (selectable) | Truetrac or Auburn on C8.25 |
| Serious off-road, 33"+ tires | ARB or OX (selectable) | ARB on C8.25 (or upgrade axle first if Dana 35) |
| Daily driver, occasional trail | Open front | Truetrac on C8.25 (quiet, no on-road behavior change) |

---

## Cross-links

- Factory Trac-Lok details (Dana 35) → [dana35-rear.md](dana35-rear.md)
- Factory Trac-Lok details (C8.25) → [chrysler-825-rear.md](chrysler-825-rear.md)
- Dana 30 front architecture → [dana30-front.md](dana30-front.md)
- Axle identification (which axle do I have?) → [identification.md](identification.md)
- Gear ratio identification → [gear-ratio-identification.md](gear-ratio-identification.md)

## Boundary links

- Axle swap execution (if upgrading before adding locker) → [`../../../work/swaps/axles/index.md`](../../../work/swaps/axles/index.md)
- Locker installation on one-ton axles → [`../../../work/swaps/axles/support-work/gearing-install.md`](../../../work/swaps/axles/support-work/gearing-install.md)
