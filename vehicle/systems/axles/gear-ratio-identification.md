# Gear Ratio Identification and Selection

## Purpose
How to determine the installed gear ratio, understand factory ratio options, and conceptualize ratio selection for tire size changes.

## Scope
Factory gear ratios on 1984–2001 XJ axles. Concept-level guidance on regearing — not installation procedures (see [`work/swaps/axles/support-work/gearing-install.md`](../../../work/swaps/axles/support-work/gearing-install.md) for that).

---

## How to read the axle tag

The axle ID tag (see [identification.md](identification.md) for tag locations) typically has the gear ratio stamped as a code or decimal. Examples:
- "355" or "3.55" = 3.55:1 ratio
- "307" or "3.07" = 3.07:1 ratio
- A "T" or "Trac-Lok" marking indicates a limited-slip differential is present

If both front and rear tags are present, check both — factory XJs always had matching front and rear ratios.

---

## How to count the gear ratio manually

If the tag is missing or unreadable, the ratio can be determined by counting driveshaft rotations.

**Method 1 — one wheel off the ground (open diff):**
1. Raise one rear wheel off the ground. Leave the other on the ground.
2. Mark the raised tire and the rear driveshaft.
3. Rotate the raised tire exactly **two** full revolutions.
4. Count the driveshaft rotations. Divide by two.
5. The result is the gear ratio (e.g., 7.1 driveshaft turns ÷ 2 = 3.55:1).

With an open differential, one wheel off the ground means the driveshaft turns twice per wheel revolution — hence dividing by two.

**Method 2 — differential locked or limited slip:**
1. Raise one rear wheel off the ground.
2. Mark the tire and the driveshaft.
3. Rotate the tire exactly **one** full revolution.
4. Count the driveshaft rotations directly — that is the ratio.

This works when both axle shafts are forced to turn together (locker engaged, or Trac-Lok providing enough resistance).

---

## Factory gear ratios by engine and transmission

| Ratio | Engine | Transmission | Package / Notes |
|-------|--------|-------------|-----------------|
| 3.07 | 4.0L I6 | AX15 manual | Standard pairing for 4.0L manual XJs |
| 3.55 | 4.0L I6 | AW4 auto | Most common XJ ratio overall (~90% of automatics) |
| 3.73 | 4.0L I6 | AW4 auto | Tow Package or UpCountry Package |
| 4.10 | 2.5L I4 | AX5 manual | Standard pairing for 4-cylinder manuals |

### Less common factory ratios

| Ratio | Configuration | Confidence |
|-------|--------------|------------|
| 3.73 | 2.5L I4 + auto | `Status: needs verification` — some sources say I4 autos got 3.73, others say 3.55 |
| 4.56 | 2.5L I4 + auto + off-road/tow package | `Status: needs verification` — single-source claim |
| 3.31 | Pre-1987 2.8L V6 + "Fuel Economy" package | Rare; documented in early XJ build sheets |
| 3.54 | 4.0L I6 + AW4 auto + Dana 44 (Tow Package) | `Status: needs verification` — one source; may be the same as 3.55 rounded differently |

**General rule of thumb:** If you have a 4.0L automatic, you almost certainly have 3.55 gears (unless tow package, then 3.73). If you have a 4.0L manual, you almost certainly have 3.07 gears. If you have a 2.5L, you almost certainly have 4.10 gears.

---

## Which axles support which ratios

All factory ratios are available in the Dana 30 front and Dana 35 rear. The Chrysler 8.25 and Dana 44 have slightly different ranges.

| Axle | Factory ratios | Notes |
|------|---------------|-------|
| Dana 30 (front) | 3.07, 3.55, 3.73, 4.10 | See [dana30-front.md](dana30-front.md) |
| Dana 35 (rear) | 3.07, 3.55, 3.73, 4.10 | See [dana35-rear.md](dana35-rear.md) |
| Chrysler 8.25 (rear) | 3.07, 3.55, 3.73 | `Status: needs verification` — one forum source reports C8.25 with 4.10 from I4 XJs; not confirmed by multiple sources |
| Dana 44 (rear) | 3.07, 3.55 | Tow Package only; see [stock-specs.md](stock-specs.md) |

Aftermarket ring-and-pinion sets extend available ratios significantly (4.10, 4.56, 4.88, 5.13 are all available for the Dana 30, Dana 35, and C8.25 from manufacturers like Yukon Gear and Revolution Gear).

---

## Why front and rear ratios must match in 4WD

The transfer case (NP231 or NP242) mechanically locks the front and rear driveshafts together when 4WD is engaged. If the front and rear axles have different gear ratios, the axles are forced to turn at different speeds while locked together.

The result:
- Driveline binding on hard surfaces
- Excessive wear on the transfer case chain, axle internals, and U-joints
- Potential breakage of the weakest link (often the Dana 35 or transfer case)

**This applies to all XJ 4WD modes** — part-time (Command-Trac) and full-time (Selec-Trac). Full-time mode has a center differential that can absorb *small* differences, but mismatched axle ratios exceed what it can handle.

When regearing, always do both axles to the same ratio.

---

## Choosing a ratio for larger tires

Larger tires effectively raise (numerically lower) the final drive ratio. The engine has to work harder to maintain highway speed, losing acceleration and increasing fuel consumption. Regearing restores the RPM range the engine was designed to operate in.

### The concept

```
(new tire diameter ÷ old tire diameter) × current ratio ≈ target ratio
```

Example: Stock 29" tires with 3.55 gears, upgrading to 33" tires:
- 33 ÷ 29 × 3.55 = 4.04 → closest available gear set is **4.10**

### Common tire-to-gear pairings (4.0L I6)

| Tire size | Starting from 3.55 | Starting from 3.07 |
|-----------|--------------------|--------------------|
| 30–31" | 3.55 adequate, 3.73 ideal | 3.55 |
| 33" | 4.10 | 3.73–4.10 |
| 35" | 4.56 | 4.10–4.56 |
| 37" | 4.88 | 4.56 |

These are guidelines, not absolutes. The right ratio depends on driving style, highway vs. trail use, and whether the vehicle has an automatic or manual transmission. Automatics with torque converter slip are more forgiving of slightly tall gearing.

---

## Cross-links

- Axle identification and tag locations → [identification.md](identification.md)
- Stock specs with all ratio tables → [stock-specs.md](stock-specs.md)
- Dana 30 ratio details → [dana30-front.md](dana30-front.md)
- Dana 35 ratio details → [dana35-rear.md](dana35-rear.md)
- Chrysler 8.25 ratio details → [chrysler-825-rear.md](chrysler-825-rear.md)
- Locker and LSD options → [locker-options.md](locker-options.md)

## Boundary links

- Gearing installation procedure → [`../../../work/swaps/axles/support-work/gearing-install.md`](../../../work/swaps/axles/support-work/gearing-install.md)
- Transfer case overview (why ratios must match) → [`../transfer-case/overview.md`](../transfer-case/overview.md)
