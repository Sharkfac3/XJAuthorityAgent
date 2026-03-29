# Dana 35 Rear Axle — Architecture, C-Clip Retention, and Failure Modes

## Purpose
Document the Dana 35 rear axle architecture, its C-clip retention system, known failure modes, and available mitigation options. This is the weakest stock rear axle in the XJ and the most common failure point for modified Jeeps.

## Scope
Factory Dana 35 rear axle as installed on the 1984–2001 Jeep Cherokee XJ. This file covers architecture and failure context — not dimensional specifications (see [stock-specs.md](stock-specs.md)).

---

## Identity

| Attribute | Value |
|-----------|-------|
| Designation | Dana 35 (also called Dana Model 35) |
| Type | Semi-float |
| Ring gear diameter | 7.5625" |
| Axle shaft spline count | 27-spline (all years) |
| Axle tube OD | 2.5" |
| Shaft retention | **C-clip** |
| Differential | Open (standard), Trac-Lok limited slip (optional) |
| Spring type | Leaf spring, spring-under-axle |

### Years installed
The Dana 35 was the standard rear axle on most XJ model years:
- **1984–1991:** Dana 35 on all XJs
- **1992–1996:** Dana 35 standard; Chrysler 8.25 optional
- **1997–2001:** Chrysler 8.25 became standard; Dana 35 no longer used

---

## C-clip retention — what it is and why it matters

The Dana 35 retains its axle shafts using **C-clips** (also called C-clamps or circlips) that seat in grooves machined into the inboard end of each axle shaft, inside the differential carrier.

### How C-clips work
1. The axle shaft slides into the axle tube from the outside.
2. The inboard end of the shaft passes through the side gear in the differential.
3. A small C-shaped clip is installed in a groove at the very end of the shaft, inside the differential.
4. The C-clip seats against the side gear, preventing the shaft from sliding outward.
5. The differential cross-pin (or pin bolt) holds the C-clip in position.

### Why C-clips are a critical weak point

If the axle shaft breaks — at the C-clip groove, at the spline, or anywhere along its length — the C-clip is no longer retained. The broken shaft, wheel, hub, brake assembly, and tire can **separate from the vehicle entirely** and roll away.

This is not a theoretical concern. It is a documented failure mode on Dana 35-equipped XJs and other C-clip axles, particularly during off-road use where side loads on the axle shaft are high.

On a bolt-in (flange-retained) axle like the Chrysler 8.25 or Dana 44, a broken shaft is still a breakdown — but the wheel stays attached to the vehicle because the bearing and flange retain it mechanically.

---

## Common failure modes

| Failure | Cause | Consequence |
|---------|-------|-------------|
| Shaft snap at C-clip groove | High torque combined with side load (wheeling on large tires, hard cornering under power) | Shaft breaks at the weakest point (the machined C-clip groove). Wheel can separate from the vehicle. |
| Shaft twist/snap along spline | Excessive torque from aggressive tire/locker combinations | Same as above — shaft failure leads to C-clip release |
| Ring and pinion wear | Normal high-mileage wear, or gear oil neglect | Whining or howling from the rear end, especially on deceleration |
| Differential bearing failure | Contaminated or depleted gear oil | Rumbling noise, eventually leading to ring gear contact damage |
| C-clip dislodge | Worn cross-pin, impact damage, or differential bearing play allowing side gear movement | Axle shaft walks outward intermittently; wheel feels loose; eventually shaft exits housing |

### The C-clip groove is the designed failure point
The groove machined for the C-clip creates a stress riser in the shaft. Under load, this is where the shaft will break first. The 27-spline shaft is already the smallest spline count of any XJ rear axle, and the C-clip groove further reduces the effective cross-section at the most critical point.

---

## Trac-Lok limited slip differential

The Trac-Lok was a factory option on the Dana 35. It is a **friction-disc (clutch-pack) type** limited slip differential.

| Attribute | Detail |
|-----------|--------|
| Type | Friction disc (clutch pack) |
| Engagement | Progressive — transfers torque to the wheel with more traction as the other wheel slips |
| Gear oil requirement | **Must use friction modifier additive** (also called limited-slip additive) in the gear oil. Without it, the clutch packs chatter and wear prematurely. |
| Identification | Axle ID tag on the differential cover or axle tube may indicate Trac-Lok. Alternatively, with both rear wheels on the ground and the vehicle in neutral, rotating one rear wheel by hand — if the other wheel rotates in the same direction, it has a limited slip. |
| Rebuild | Clutch packs wear over time and can be rebuilt. A worn Trac-Lok acts like an open differential. |

---

## Ring and pinion ratios

Factory-installed gear ratios for the XJ Dana 35:

| Ratio | Typical application |
|-------|-------------------|
| 3.07 | 4-cylinder models, highway-oriented |
| 3.55 | Most common 4.0L / automatic combination |
| 3.73 | Common on 4.0L / manual transmission |
| 4.10 | 4-cylinder models |

The front and rear axle ratios must always match. Mismatched ratios cause driveline binding in 4WD.

---

## Fix options for C-clip weakness

### C-clip eliminator kit
Aftermarket kits (Superior Axle, Yukon Gear) convert the Dana 35 from C-clip retention to **bolt-in (flange-retained) axle shafts**. The kit replaces the axle shafts, bearings, and seals with a flanged design that bolts to a retainer plate at the axle tube end.

**Result:** A broken shaft no longer allows the wheel to separate. The shaft fails in place, and the flange/bearing retains the wheel on the vehicle.

**Cost:** Approximately $400–600 for a complete kit with new shafts.

**Limitation:** The ring gear, housing, and tube diameter are still Dana 35 — the eliminator kit addresses the C-clip safety issue but does not increase the overall strength of the axle.

### Full axle swap
For XJs running 31"+ tires or doing aggressive off-road use, the community-standard recommendation is to replace the Dana 35 entirely:
- **Chrysler 8.25** from a 1992–2001 XJ — direct bolt-in, stronger in every dimension. See [chrysler-825-rear.md](chrysler-825-rear.md).
- **Dana 44** from a 1987–1989 XJ tow package (extremely rare) or other Jeep platform — direct bolt-in, strongest stock option.
- **One-ton axle swap** (Ford Sterling 10.50 or similar) — for builds running 35"+ tires. See [`../../../work/swaps/axles/index.md`](../../../work/swaps/axles/index.md).

---

## Strength ceiling

The Dana 35 is **not recommended past 31" tires** for any XJ that sees off-road use. With 33" tires, a locker, and any trail driving, shaft breakage is a matter of when, not if.

For street-only XJs on stock or 30" tires, the Dana 35 is adequate for the life of the vehicle with proper gear oil maintenance.

---

## Dimensional specifications
For complete dimensional specs (housing width, tube OD, spring pad measurements, weight), see [stock-specs.md](stock-specs.md).

## Cross-links
- Stock specs and dimensions: [stock-specs.md](stock-specs.md)
- Axle family overview and year matrix: [overview.md](overview.md)
- Chrysler 8.25 — the preferred stock upgrade: [chrysler-825-rear.md](chrysler-825-rear.md)

## Boundary links
- One-ton rear axle swap: [`../../../work/swaps/axles/one-ton-rear/index.md`](../../../work/swaps/axles/one-ton-rear/index.md)
- Rear axle diagnostics: `diagnostics/driveline/`
- Axle sourcing and interchange: `sourcing/interchange/axles/`

## Sources
Community-verified via NAXJA, JeepForum, CherokeeTalk, CherokeeForum, Pirate4x4; cross-referenced against Dana/Spicer axle identification guides and aftermarket kit specifications (Superior Axle, Yukon Gear).
