# One-Ton Driveshaft Specifications

U-joint series, shaft length, and driveshaft configuration guide for XJ Cherokee builds running 2005+ Super Duty Dana 60 front and Sterling 10.50 rear axles.

---

## U-joint series

### What the components use

| Connection point | U-joint series | Notes |
|-----------------|---------------|-------|
| NP231 transfer case (rear output) | 1310 (stock XJ) | May need SYE conversion — see below |
| NP231 transfer case (front output) | 1310 (stock XJ) | CV / double-cardan joint required for steep angles |
| Dana 60 front pinion yoke | 1350 or 1410 | Depends on donor configuration and yoke selection |
| Sterling 10.50 pinion flange | 1410 | Most common on 05+ Super Duty |

### Series strength comparison

| Series | Cap diameter | Relative strength | Typical application |
|--------|------------|-------------------|-------------------|
| 1310 | 1.062" | Stock half-ton | Stock XJ, stock transfer case output |
| 1330 | 1.062" (wider) | Slightly above 1310 | Some aftermarket XJ shafts |
| 1350 | 1.188" | One-ton capable | Common for Dana 60 builds |
| 1410 | 1.188" (wider) | Full one-ton | Sterling 10.50, heavy builds |
| 1480 | 1.375" | Overkill for XJ | Super Duty OEM axle shafts — not driveshafts |

**Recommendation:** Build both driveshafts to **1350 minimum**. If the Sterling pinion uses a 1410 flange, run a 1350x1410 combination joint or build the rear shaft entirely in 1410. The transfer case end limits you to 1310 unless you upgrade the output yoke.

---

## Transfer case output — SYE (Slip Yoke Eliminator)

The NP231 transfer case uses a slip yoke on the rear output. At high lift heights (6"+), the slip yoke operates at extreme extension, which causes:
- Vibration from the yoke running at the end of its travel
- Driveline binding at steep angles
- Premature wear on the output seal and bushing

**SYE conversion is strongly recommended for any one-ton build.** The SYE replaces the slip yoke with a fixed flange output, and the slip joint moves to the driveshaft itself (or a CV joint is used).

Common SYE kits:
- **Tom Woods / JB Conversions** — most popular, well-proven
- **Advance Adapters** — another established option
- **Rough Country** — budget option, adequate

After SYE installation, the rear driveshaft is built as a **fixed-length shaft with a CV (double-cardan) joint** at the transfer case end to handle the operating angle.

### Front output
The NP231 front output uses a fixed yoke (no slip yoke). The front driveshaft needs a **double-cardan (CV) joint** at the transfer case end to handle the steep angle created by 6–8" of lift. The axle end uses a standard single U-joint.

---

## Driveshaft length

Shaft length depends on:
1. Lift height (more lift = more distance between transfer case and axle)
2. Final axle width after narrowing (affects front shaft angle slightly)
3. SYE vs stock slip yoke (SYE changes the effective output point)
4. Pinion angle

**You cannot determine shaft length from a chart.** Measure with the axles installed at ride height:
- Rear: measure from the transfer case rear output flange (or SYE flange) to the Sterling pinion flange, center-to-center
- Front: measure from the transfer case front output yoke to the Dana 60 pinion yoke, center-to-center

Order shafts from a driveshaft shop with these measurements. Most builders use a local driveshaft shop or a mail-order specialist (Tom Woods, Adams Driveshaft, JE Reel).

### Typical length ranges (for reference only — always measure)

| Shaft | Approximate length range | Notes |
|-------|------------------------|-------|
| Rear (with SYE) | 28–34" | Varies with lift and wheelbase |
| Front | 24–30" | Shorter than rear; steep angle |

---

## Pinion flange vs yoke

| Axle | Common configuration | Notes |
|------|---------------------|-------|
| Dana 60 front | Yoke (1350) | Some run 1410 yoke — specify when ordering shaft |
| Sterling 10.50 rear | Flange (1410) | Bolt-on flange, not a press-fit yoke. Driveshaft must have a matching flange or a flange-to-yoke adapter |

**Flange bolt patterns vary.** When ordering a driveshaft for the Sterling, provide the bolt count and bolt circle diameter of the pinion flange to the driveshaft shop.

---

## Double-cardan (CV) joints

Both the front and rear driveshafts in a one-ton XJ build typically use a double-cardan constant-velocity (CV) joint at the transfer case end. This is required because:
- 6–8" of lift creates steep operating angles at the transfer case
- A single U-joint at steep angles creates speed variation (vibration) per revolution
- The CV joint cancels this variation by using two U-joints in a yoke assembly

**The axle pinion end uses a standard single U-joint** in most configurations, because the pinion angle is set to minimize the operating angle at that end.

---

## Driveshaft work procedures

For measurement, fabrication, and installation procedures, see:
[`../../../work/swaps/axles/support-work/driveshaft-work.md`](../../../work/swaps/axles/support-work/driveshaft-work.md)
