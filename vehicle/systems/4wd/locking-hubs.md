# Locking Hubs — Factory Configuration and Common Misconception

## Purpose
Clarify that the Jeep Cherokee XJ was never equipped with factory locking hubs, and document the aftermarket locking hub conversion option.

## Scope
All 1984–2001 XJ model years. This file exists because "locking hubs" is a frequently searched topic that leads to confusion between the XJ's actual factory front hub design and the locking hubs found on older Jeeps (CJ, SJ) and other 4WD trucks.

---

## The XJ does not have factory locking hubs

No Jeep Cherokee XJ — in any year, any trim, any drivetrain configuration — left the factory with locking hubs. This is a common misconception, especially among owners coming from CJ-5, CJ-7, or full-size Cherokee (SJ) / Wagoneer backgrounds where manual or automatic locking hubs were standard equipment.

### What the XJ uses instead: unit bearings

The XJ Dana 30 front axle uses **unit bearings** (also called hub/bearing assemblies). These are sealed, non-serviceable bearing units that bolt to the steering knuckle. The axle shaft splines directly into the unit bearing hub.

**The front axle shafts are always mechanically connected to the wheels.** There is no lock/free mechanism at the hub. The front axle shafts, differential gears, and ring gear spin any time the front wheels are turning — even in 2WD.

### How the factory reduced front driveline drag

Instead of locking hubs, the XJ used two different strategies to reduce parasitic drag in 2WD:

1. **1984–~1991 Command-Trac models: Central Axle Disconnect (CAD)** — a vacuum-operated disconnect at the passenger-side inner axle shaft inside the axle housing. This disconnects the passenger shaft so the differential does not drive the front driveshaft. See [front-axle-disconnect.md](front-axle-disconnect.md).

2. **1992–2001 (all) and all Selec-Trac models: no disconnect at all** — the front axle shafts are always connected via a one-piece passenger shaft. The front differential and driveshaft spin freely in 2WD. Chrysler determined the fuel economy penalty was negligible and eliminated the disconnect entirely.

### Hub/bearing assembly evolution

Three different unit bearing assemblies were used across XJ production:

| Era | Hub type | Notes |
|-----|----------|-------|
| 1984–1989 | AMC-design roller bearing hub | Original AMC hub, rotor, caliper, and steering knuckle design |
| 1990–1994 | Revised hub assembly | Updated design, same bolt pattern |
| 1995–2001 | ABS-compatible unit bearing | Integral ABS tone ring. 297-size inner U-joints. Not interchangeable with earlier hubs without matching knuckle, rotor, and caliper |

**Status: needs verification** — The exact hub assembly changeover years and cross-compatibility details need factory parts catalog confirmation. The 1995+ ABS unit bearing is the most clearly documented boundary.

---

## Common misconception: "locking hubs" vs. the CAD

People searching for "XJ locking hubs" are usually encountering one of these situations:

- **They have a CAD-equipped XJ and 4WD won't engage** — the problem is the vacuum disconnect system, not a locking hub. See [front-axle-disconnect.md](front-axle-disconnect.md).
- **They want to free-wheel the front axle in 2WD** — the XJ does not have a hub-level mechanism for this. The CAD did this internally (and was eliminated in 1992). Aftermarket locking hub conversion is the only way to add this capability.
- **They are coming from a CJ or SJ background** — those vehicles had factory locking hubs. The XJ never did.

---

## Aftermarket locking hub conversion

Manual locking hub conversion kits are available for the XJ Dana 30. These replace the factory unit bearings with a traditional serviceable hub assembly and a twist-lock hub cap.

### What the conversion includes
A complete kit typically replaces: unit bearings, axle shafts (to match the new hub spline), brake rotors, wheel bearings, seals, and the locking hub assemblies themselves. This is a full hub-outward replacement, not a bolt-on addition.

### Available kits
- Alloy USA / Rugged Ridge deluxe kit (27-spline chromoly shafts, machined rotors, manual hubs)
- Warn premium manual locking hubs (hub assemblies only — requires matching shaft and bearing setup)
- Yukon Gear hub conversion kit

### Cost
$1,400–$1,500+ for a complete kit with shafts. Hub assemblies alone are less, but require compatible shaft and bearing components.

### When it makes sense
- Dedicated trail rigs where eliminating all front driveline drag in 2WD matters for highway towing or long-distance road driving
- Builds where the owner wants manual control over front axle engagement independent of the transfer case
- Rigs already receiving aftermarket axle shafts and want to add free-wheeling capability at the same time

### When it does not make sense
- Most street-driven and weekend-wheeled XJs — the parasitic drag from spinning the front differential in 2WD is minimal
- Budget builds — the $1,400+ cost buys a lot of other upgrades with more tangible benefit
- XJs with aftermarket lockers in the front differential — some locking hub kits are incompatible with certain locker designs

---

## Cross-links
- Parent: [overview.md](overview.md) — 4WD engagement system overview
- Central Axle Disconnect: [front-axle-disconnect.md](front-axle-disconnect.md)
- Dana 30 front axle architecture: [`../axles/dana30-front.md`](../axles/dana30-front.md)
- Stock axle specs: [`../axles/stock-specs.md`](../axles/stock-specs.md)

## Sources
Community-verified via NAXJA, JeepForum, CherokeeForum; aftermarket kit specifications from Quadratec, 4WD.com, and manufacturer catalogs (Alloy USA, Warn, Yukon Gear).
