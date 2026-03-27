# Renix Ground Upgrades

## Purpose
Add supplemental ground cables to Renix-era (1987–1990) XJ and MJ vehicles beyond what the factory provided.

## Why upgrade
The factory ground paths are undersized and rely on too few connection points. Adding dedicated cables creates redundant, lower-resistance paths that reduce sensor ground resistance and improve driveability — especially after the factory grounds have been refreshed per `work/maintenance/electrical/renix-ground-refresh.md`.

---

## Upgrade 1: Firewall to intake manifold

Provides a heavy direct ground between the chassis (firewall) and the engine.

| Spec | Value |
|------|-------|
| Wire gauge | #4 |
| Length | ~18″ |
| Lug size | 3/8″ on each end |
| NAPA part number | 781116 |

### Installation
1. Attach one end to the existing firewall ground strap bolt (where the factory braided cable mounts).
2. Attach the other end to a bolt on the rear of the intake manifold — the heat shield bolt or a fuel rail bolt works.
3. Clean both mounting surfaces to bare metal.
4. Apply OxGard to all contact surfaces.

---

## Upgrade 2: Battery to chassis

Provides a heavy direct ground between the battery negative terminal and the chassis, bypassing the factory path through the engine block.

| Spec | Value |
|------|-------|
| Wire gauge | #4 |
| Length | ~10″ |
| Lug size | 3/8″ on each end |
| NAPA part number | 781115 |

### Installation
1. Attach one end to the negative battery bolt.
2. Attach the other end to the closest 10mm bolt on the radiator support forward of the battery.
3. Clean the radiator support mounting point to bare metal.
4. Apply OxGard to all contact surfaces.

---

## Results
These upgrades combined with a full ground refresh have been documented to reduce TPS ground resistance from 1.7 Ω to 0.8 Ω — a significant improvement in ground path quality for all engine sensors.

## Custom cable alternative
For professionally manufactured ground and battery cable upgrades: jeepcables.com

---

## See also
- `work/maintenance/electrical/renix-ground-refresh.md` — refresh factory grounds first (prerequisite)
- `vehicle/era1/wiring.md` — Era 1 wiring overview and ground locations
- `work/swaps/ecu/wiring/grounds.md` — grounds in the context of ECU swaps

## Source
Cruiser54 — cruiser54.com, "Renix Ground Refreshing"
