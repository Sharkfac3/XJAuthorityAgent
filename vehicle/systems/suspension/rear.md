# Rear Suspension — Jeep Cherokee XJ

## System layout

The XJ rear suspension is a solid-axle leaf spring setup across all 1984–2001 model years. There are no year-dependent exceptions — every XJ uses the same basic rear suspension architecture.

- **Leaf spring pack** — multi-leaf stack, one assembly per side
- **Shackles** — short links at the rear spring eye; allow the spring to arc through travel
- **Fixed front hanger** — forward spring eye mounts solidly to the frame
- **Shocks** — mounted separately

---

## Rear axle identification

Three rear axles were fitted to the XJ. Identifying which one a specific Jeep has requires knowing the year and options:

| Axle | Years | Determining factor |
|------|-------|--------------------|
| Dana 35 | 1984–1996 standard | ABS-equipped 1991–1996 models; base for 1984–1990 |
| Chrysler 8.25 | 1991–1996 non-ABS; 1997–2001 standard | Non-ABS 1991–1996; universal on 1997+ |
| Dana 44 | 1987–1989 Tow Package only | Extremely rare |

The fastest visual tells:
- **Dana 35**: completely round diff cover, 2.5" axle tube, C-clip axle shaft retention (no retainer plate at the wheel)
- **Chrysler 8.25**: rectangular diff cover with a flat bottom section ~3–4" wide, 3.0" axle tube, bolt-in shaft retention (retainer plate with 4 bolts at wheel hub)
- **Dana 44**: round diff cover (larger than Dana 35), 3.125" axle tube, bolt-in retention

See `vehicle/systems/axles/identification.md` for the complete visual ID guide and the ABS/C8.25 connection.

---

## Leaf spring specs

Stock leaf spring specifications vary by trim and load code. The spring code is stamped on a tag on the spring pack.

| Spec | Stock value (Sport/base) |
|------|--------------------------|
| Approximate overall length | ~51.6" |
| Number of leaves (base) | 4 |
| Approximate arch (free height) | ~5.5" |
| Approximate load rating | ~745 lb |

Factory spring codes and their load ratings:

| Code | Free arch | Load rating |
|------|-----------|-------------|
| LL | 3.125" | ~405 lb |
| LM | 5.625" | ~605 lb |
| LS | 6.0" | ~675 lb |
| LT | 7.0" | ~755 lb |

Higher load code springs are stiffer and sit taller. A sagged LL spring may sit lower than a fresh LS spring on the same vehicle. Age and accumulated load cycles significantly affect actual ride height independent of the spring code.

---

## Shackles

The rear shackle connects the rear spring eye to the frame. The shackle swings as the spring arcs through travel.

**Ideal geometry:** At static ride height, the rear shackle should sweep rearward at approximately 45°. This geometry gives the best ride quality and most balanced compression/extension travel. When the shackle is nearly vertical (too short) or nearly horizontal (too long), spring behavior degrades.

### Shackle-based lift

Extended shackles are a common budget lift method:

| Shackle type | Approximate lift |
|-------------|-----------------|
| Stock | 0 |
| Extended HD (boomerang style) | ~1" |
| Adjustable (5.5"–7.0" eye-to-eye) | ~1.25"–2.0" |
| Adjustable (7.5"–9.0" eye-to-eye) | ~2.25"–3.0" |

**Shackle lift math:** Extending shackle length by X inches adds approximately half that amount in ride height, because the spring arcs through a radius as the shackle swings.

**Caution:** Shackle-only lifts on worn or sagged stock spring packs accelerate spring fatigue. Extended shackles work best paired with replacement springs designed for the new geometry.

---

## Add-a-leaf (AAL)

An add-a-leaf inserts one additional leaf into the existing spring pack. It is the lowest-cost approach to adding rear lift and load capacity.

**What it does:**
- Adds approximately 1"–1.5" of rear lift
- Stiffens the spring rate
- Helps prevent axle wrap under acceleration (does not cause wrap — this is a common misconception)

**What it requires:**
- Longer center bolt/pin to accommodate the extra pack thickness
- Re-torquing of U-bolts

An AAL on a sagged spring pack produces less lift than on a fresh pack. For a vehicle that has lost significant arch through age, a full spring pack replacement is more predictable than an AAL.

**Lift blocks:** Blocks placed between the spring pack and the axle perch add lift but introduce axle wrap risk under power. Blocks are the least preferred lift option for the rear — they are not recommended on a vehicle that sees off-road or any spirited driving.

---

## Full spring pack replacement

Replacement spring packs are available in lift heights from 2" to 4.5" from multiple vendors. A correctly rated replacement pack gives predictable lift, a consistent spring rate, and restores the shackle to proper geometry.

For lifts of 2.5" and above, full pack replacement is the correct approach rather than stacking AALs or shackle extensions on worn springs.

---

## See also

- `vehicle/systems/suspension/overview.md` — full system layout
- `vehicle/systems/suspension/lift-geometry.md` — driveshaft angle and rear geometry at lift
- `vehicle/systems/axles/identification.md` — rear axle identification by year and visual inspection
- `vehicle/systems/axles/dana35-rear.md` — Dana 35 C-clip failure modes
- `vehicle/systems/axles/chrysler-825-rear.md` — Chrysler 8.25 architecture

## Sources

NAXJA forums (leaf spring specs, shackle geometry discussion); CherokeeForum; JeepForum leaf spring threads; Rusty's Off-Road and Quadratec XJ spring product pages (spec data); CORE4X4 adjustable shackle specifications; JKS Manufacturing shackle product data.
