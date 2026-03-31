# Suspension Overview — Jeep Cherokee XJ

## Architecture

The XJ uses a solid-axle suspension front and rear across its entire 1984–2001 production run. There were no independent-suspension variants.

| End | Type |
|-----|------|
| Front | Solid Dana 30 axle, coil springs, four-link control arms (2 upper + 2 lower), lateral track bar |
| Rear | Solid rear axle, leaf springs |

Jeep called this the **Quadra-Link** front suspension. Four control arms locate the axle longitudinally and control axle rotation. The track bar locates the axle laterally. Coil springs carry vertical load. Each function is handled by a dedicated component — this is why geometry changes so predictably at lift.

---

## Axles

| Axle | Position | Years | Notes |
|------|----------|-------|-------|
| Dana 30 | Front | 1984–2001 (4WD) | Every 4WD XJ. No exceptions. |
| Dana 35 | Rear | 1984–1996 (standard) | C-clip axle shafts. Weak past 31" tires. |
| Chrysler 8.25 | Rear | 1991–1996 (non-ABS), 1997–2001 (all) | Bolt-in shafts, no C-clips. Best common stock rear. |
| Dana 44 | Rear | 1987–1989 Tow Package only | Extremely rare. |

**Note:** The AMC Model 20 rear axle is sometimes mentioned in XJ discussions but is incorrect — no XJ ever used the AMC Model 20. That axle belongs to the CJ and full-size SJ platforms. See `vehicle/systems/axles/identification.md` for the full year matrix and visual ID guide.

For full axle architecture, specs, and identification: `vehicle/systems/axles/`

---

## Stock ride height and ground clearance

| Measurement | Stock value |
|-------------|------------|
| Ride height (hub center to fender flare) | ~17 inches |
| Ground clearance at front diff (225/75 tires) | ~8.3 inches |
| Ground clearance at rear diff (225/75 tires) | ~7.3 inches |
| UpCountry package lift over base | +1 inch |

Ground clearance is measured at the differential housings — the lowest points of the vehicle. The front diff typically sits higher than the rear because the Dana 30 is smaller than the rear axle housings.

---

## Why lift creates geometry problems

Lifting the XJ changes the angles and effective lengths of every suspension component simultaneously. The stock geometry was optimized at ride height. At lift:

- **Caster decreases** — the axle rotates as it moves down relative to the chassis, pointing the top of the knuckle rearward less than stock
- **Track bar angle steepens** — the frame-side mount is now higher than the axle-side mount; at sufficient lift the ball joint reaches its range-of-motion limit
- **Control arm angles change** — affecting axle centering and leverage
- **Driveshaft angles increase** — particularly the rear driveshaft into the transfer case slip yoke

These are not separate problems — they are all consequences of the same geometry shift. A lift done without addressing them trades one set of problems for another.

See `vehicle/systems/suspension/lift-geometry.md` for the full treatment.

---

## Child leaves

- `front.md` — control arms, track bar, caster, ball joints, coil spring specs
- `rear.md` — leaf spring specs, shackles, add-a-leaf, SOA, rear axle identification
- `lift-geometry.md` — what changes at lift and the standard correction approaches

## Related branches

- Full axle specs and identification: `vehicle/systems/axles/`
- Steering geometry (track bar and drag link relationship): `vehicle/systems/steering/overview.md`
- Death wobble root causes: `vehicle/systems/steering/death-wobble.md`

## Sources

NAXJA forums; CherokeeTalk XJ specs thread; JeepForum; CherokeeForum; Quadratec XJ suspension product pages; 2001 Jeep Cherokee factory specifications (cdn.xjjeeps.com); JeepDatabase.com XJ specs.
