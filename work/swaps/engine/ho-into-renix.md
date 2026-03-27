# HO Engine into Renix Chassis Swap

## Purpose
Install a 1991–1995 HO (High Output) 4.0L engine into a 1987–1990 Renix-era XJ or MJ while retaining the Renix ECU and management system.

## Overview
This swap is more straightforward than commonly described. The Renix intake manifold, sensors, wiring, distributor, flywheel/flexplate, and valve cover all transfer to the HO block. The HO block provides the same bottom end with updated internals.

---

## Block compatibility

| Block family | Compatible with |
|-------------|-----------------|
| XJ Cherokee / ZJ Grand Cherokee ('93–'98) | Each other |
| 2000+ TJ Wrangler / WJ Grand Cherokee ('99–'04) | Each other |
| YJ Wrangler / 1997–1999 TJ | XJ/ZJ applications |
| XJ/ZJ blocks | **Not** compatible with 2000+ TJ/WJ without significant modification (motor mount and accessory mount locations differ) |

---

## What transfers from the Renix vehicle

- Intake manifold (HO intake ports are slightly different — use a **new Renix intake gasket**)
- Exhaust manifold (exhaust ports are identical; Renix manifold fits directly)
- All sensors and wiring
- Renix distributor (required — HO distributor is incompatible with Renix ECU)
- Flywheel or flexplate (required — Renix reluctor ring is needed for correct CPS signal; see `diagnostics/engine/renix-cps-test.md`)
- Valve cover (retains the Renix CCV system without modification)

---

## Required HO block modifications

### 1. Coolant temperature sensor port
The HO block has a **plug** in the coolant galley on the driver's side, closest to the front. This plug must be removed to install the Renix coolant temp sensor.

- Use a **5/16″ square drive** or a 3/8″ drive ground down to fit.
- **Do this before installing the engine** — access is nearly impossible once it's in the vehicle.

### 2. Knock sensor
Located just above the oil pan on the driver's side of the block, approximately mid-length. The threaded provision should be present. If drilled but not tapped, tap it before installation.

### 3. Temperature gauge sender (1996+ HO blocks)
Beginning in 1996, the rear head drilling for the temperature gauge sender was eliminated. Solutions:
- Relocate to the threaded hole in the thermostat housing sourced from an HO engine, with extended wiring.
- Drill and tap the HO head.

---

## Exhaust manifold options

**Option A — Keep Renix manifold:** bolt-on, no modifications needed.

**Option B — Use HO manifold with HO headpipe:**
- Thread the O2 sensor into the HO headpipe.
- Weld a bung into the HO manifold to accept the EGR tube.

---

## Vehicle code reference

| Code | Vehicle |
|------|---------|
| XJ | Cherokee '84–'01 (not Grand Cherokee) |
| ZJ | Grand Cherokee '93–'98 |
| WJ | Grand Cherokee '99–'04 |
| YJ | Wrangler '87–'95 |
| TJ | Wrangler '97–'06 |

---

## See also
- `diagnostics/engine/renix-cps-test.md` — verify CPS voltage after swap (Renix flywheel required)
- `work/setup-and-calibration/engine/renix-distributor-indexing.md` — index the distributor after installation
- `vehicle/era1/wiring.md` — Renix sensor and wiring overview
- `vehicle/era1/sensors/` — individual sensor specs for reinstallation reference

## Source
Cruiser54 — cruiser54.com, "HO into Renix Swap"
