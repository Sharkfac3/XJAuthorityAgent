# Dana 30 Front Axle — Architecture and Components

## Purpose
Document the Dana 30 front axle architecture, component types by year, and known weak points. This file covers what the parts are and how they are arranged — not dimensional specifications (see [stock-specs.md](stock-specs.md)) and not service procedures (see `work/`).

## Scope
Factory Dana 30 front axle on all 4WD 1984–2001 Jeep Cherokee XJ models. 2WD XJs have no front axle assembly.

---

## Identity

| Attribute | Value |
|-----------|-------|
| Designation | Dana 30 |
| Design | Open-knuckle, solid front axle (not independent) |
| Ring gear cut | Reverse-cut (high-pinion — pinion sits above the axle centerline) |
| Ring gear diameter | 7.125" |
| Axle shaft spline count | 27-spline (all years) |
| Spring type | Leaf spring, spring-under-axle |
| Pinion rotation | Reverse (ring gear on passenger side) |
| Used on | Every 4WD XJ from 1984–2001 |

The XJ Dana 30 is a **reverse-cut** (also called high-pinion) design. The pinion gear enters from above the axle centerline. This improves front driveshaft angle on lifted vehicles compared to a standard-rotation (low-pinion) Dana 30 found on other platforms.

---

## Axle shaft types by year

The XJ Dana 30 used two fundamentally different outer axle shaft designs across its production run:

### 1984–1986: CV joint (Rzeppa-type) outer shafts

Early XJs used a constant-velocity (CV) joint at the outer end of each axle shaft, inside the steering knuckle. These are **Rzeppa-type CV joints** — not birfield joints (birfield is a Toyota-specific design and was never used on any XJ).

| Attribute | Detail |
|-----------|--------|
| Outer joint type | Rzeppa CV joint |
| Inner spline | 27-spline |
| Strength | Weaker than later U-joint shafts |
| Availability | Rare — most have been converted to U-joint shafts |
| Advantage | CV joint maintains constant velocity at high steering angles; a broken CV shaft can be gutted on-trail to limp home |

**Status: needs verification** — Whether all 1984–1986 XJs had CV shafts or only some is debated. Community consensus is that CV was the default for these years, but some late-1986 production may have transitioned early.

### 1987–2001: U-joint outer shafts

Starting approximately 1987, the XJ switched to standard Spicer U-joints at both the inner and outer axle shaft positions. This became the dominant and preferred configuration.

| Year range | Inner U-joint size | Outer U-joint size |
|------------|-------------------|-------------------|
| 1987–1994 (non-ABS) | Spicer 5-260x | Spicer 5-260x |
| 1989–1994 (ABS) | Spicer 5-297x | Spicer 5-260x |
| 1995–2001 (all ABS) | Spicer 5-297x | Spicer 5-260x |

The 297-size inner U-joint is significantly stronger than the 260 and is a common upgrade for earlier XJs. The outer U-joint remained 260-size across all U-joint years.

**Upgrade note:** Spicer 5-760x U-joints are the same physical dimensions as the 5-297x but use a thicker trunnion (cross) for higher strength. They are a direct replacement upgrade.

---

## Inner axle shaft and CAD

The passenger-side inner axle shaft configuration depends on whether the XJ has the Central Axle Disconnect (CAD):

- **CAD-equipped (1984–~1991 Command-Trac):** The passenger inner shaft is a **two-piece design** with a spline collar that slides to connect or disconnect the shaft halves. The vacuum actuator on the axle housing controls this collar. See [`../4wd/front-axle-disconnect.md`](../4wd/front-axle-disconnect.md).
- **Non-CAD (1992+ all, and all Selec-Trac):** The passenger inner shaft is a **one-piece shaft** identical in concept to the driver side. No disconnect mechanism.

The driver-side inner shaft is always one-piece on all years.

---

## Steering knuckle

The XJ Dana 30 uses **ball joints** on all years (1984–2001). Upper and lower ball joints connect the steering knuckle to the axle tube C-bracket.

**The XJ never used king pins.** King pin steering knuckles are a CJ-5/CJ-7 and earlier full-size Jeep design. If someone references "king pins on an XJ," they are either confused or referring to a non-XJ axle swap.

### Knuckle and hub evolution

| Era | Knuckle type | Hub/bearing type |
|-----|-------------|-----------------|
| 1984–1989 | AMC-design knuckle | Roller bearing hub assembly (serviceable bearings) |
| 1990–1994 | Revised knuckle | Updated hub assembly |
| 1995–2001 | ABS-compatible knuckle | Sealed unit bearing with integral ABS tone ring |

The 1995+ unit bearing is a sealed, non-serviceable assembly. When the bearing fails, the entire unit is replaced. The earlier roller bearing hubs can be repacked and adjusted.

**1995+ unit bearings are not interchangeable with pre-1995 hubs** without also swapping the matching knuckle, rotor, and caliper.

---

## Ring and pinion ratios

Factory-installed gear ratios for the XJ Dana 30:

| Ratio | Typical application |
|-------|-------------------|
| 3.07 | 4-cylinder models, highway-oriented packages |
| 3.55 | Most common 4.0L / automatic combination |
| 3.73 | Common on 4.0L / manual transmission |
| 4.10 | 4-cylinder models (compensating for lower torque) |

The front and rear axle ratios must always match. Mismatched ratios cause driveline binding in 4WD.

---

## Known weak points

Listed in order of frequency for stock and mildly modified XJs:

1. **Unit bearings (1995+):** The sealed unit bearing is the most commonly replaced front axle component on later XJs. Symptoms: humming/growling noise that changes with speed, ABS light from damaged tone ring, wheel play.

2. **U-joints:** Both inner and outer U-joints wear over time. The 260-size outer joint is the weakest link in the U-joint chain. Symptoms: clicking or clunking on turns (especially in 4WD), vibration at speed, visible rust or play in the joint caps.

3. **Ball joints:** Upper and lower ball joints wear with mileage and off-road use. Symptoms: clunking over bumps, wandering steering, uneven tire wear. Death wobble is often traced to worn ball joints in combination with other worn steering components.

4. **Outer stub shaft:** Under heavy off-road load (large tires, aggressive wheeling), the outer stub shaft is the first shaft component to fail. The 260-size U-joint yoke area is the typical fracture point.

5. **CV joints (1984–1986 only):** On the rare XJs still running original CV shafts, the CV joint boot can tear, leading to contamination and joint failure. Symptoms: clicking on turns with wheels under power.

---

## Dimensional specifications
For complete dimensional specs (housing width, tube OD, spring pad measurements, weight), see [stock-specs.md](stock-specs.md). This file intentionally does not duplicate those tables.

## Cross-links
- Stock specs and dimensions: [stock-specs.md](stock-specs.md)
- Axle family overview and year matrix: [overview.md](overview.md)
- Central Axle Disconnect: [`../4wd/front-axle-disconnect.md`](../4wd/front-axle-disconnect.md)
- 4WD engagement system: [`../4wd/overview.md`](../4wd/overview.md)
- Locking hub clarification: [`../4wd/locking-hubs.md`](../4wd/locking-hubs.md)

## Boundary links
- Front axle service and maintenance: `work/maintenance/axles/`
- One-ton front axle swap: [`../../../work/swaps/axles/one-ton-front/index.md`](../../../work/swaps/axles/one-ton-front/index.md)
- Axle diagnostics: `diagnostics/driveline/`

## Sources
Community-verified via NAXJA, JeepForum, CherokeeTalk, CherokeeForum, Pirate4x4; cross-referenced against Spicer U-joint catalog specifications and factory parts catalog data.
