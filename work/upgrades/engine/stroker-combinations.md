# Stroker Combinations — Jeep 4.0L

The two community-proven builds are the **~4.6L stroker** (258 crank + +0.030" overbore) and the **~4.7L stroker** (258 crank + +0.060" overbore). Both use the same crankshaft. The difference is bore size and piston selection.

See `work/upgrades/engine/stroker-overview.md` for the displacement math and block selection background.

---

## Crankshaft: AMC/Jeep 258 (4.2L)

Both builds share the same crank. There are two variants in circulation:

| Casting / Part | Years | Counterweights | Snout | Notes |
|----------------|-------|---------------|-------|-------|
| #3727 | 1987–1990 | 4 | 54mm | **Preferred.** Direct fit to 4.0L harmonic balancer. 46 lbs. |
| #3235477 | 1981–1986 | 4 | 64mm | Requires 10mm snout spacer or machining to fit 4.0L balancer. 46 lbs. |
| 12-counterweight | 1971–1981 | 12 | 64mm | Heavier (66 lbs). Some builders prefer it for crawling/manual trans applications due to added flywheel effect. 64mm snout requires the same spacer work as the #3235477. |

The #3727 (1987–90) is the community's first choice because the 54mm snout fits the 4.0L harmonic balancer without modification.

**Journal dimensions:** The 258 and 4.0L cranks share the same main and rod journal diameters. No journal grinding is required to run the 258 crank in the 4.0L block. Grinding is only relevant if pushing stroke *beyond* 3.895" using smaller-journal rods (a different build class).

**Sourcing:** These cranks come from 1971–1990 AMC/Jeep inline-six applications — CJ, Cherokee (pre-XJ), Wagoneer, and J-series trucks. The 1987–90 examples are the most desirable and the most picked-over. Expect junkyard availability to vary significantly by region. Clean used examples with good journals can be run after magnaflux inspection, journal cleanup, and balance check.

---

## ~4.6L Stroker (most common)

**Target displacement:** ~280ci at +0.030" overbore.

| Component | Specification | Notes |
|-----------|--------------|-------|
| Block | 4.0L NVH block (1996+) | See `vehicle/era2/ho-engine.md` for Group A/B motor mount compatibility |
| Crankshaft | AMC 258 (3.895″ stroke) — #3727 preferred | Mag, clean, balance after acquisition |
| Connecting rods | 4.2L rods (5.875″ length) | The community standard recipe pairs 258 rods with the 258 crank for a better rod ratio (1.508:1). 4.0L rods (6.125″) can also be used and improve the rod ratio to ~1.573:1 — either is above the 1.50:1 minimum floor for street use. Confirm piston pin compatibility. |
| Pistons | KB (Keith Black) Silvolite forged slugs | KB #944 (21.7cc dish, ~9.5:1 CR) for stock-ish fuel systems. KB #945 (11.4cc dish, ~10.5:1 CR) for modified fuel systems and aggressive cams. Sized to the specific bore. |
| Head | Stock 4.0L HO head | 0630 or TUPY 0331 casting preferred. Port and polish recommended to keep up with the added displacement. See `vehicle/era2/ho-engine.md` for head casting notes. |
| Head gasket | Mopar/Victor Performance 0.043″ | Supports appropriate quench height |
| Cam | Stock HO cam is a starting point | Aftermarket grinds (Comp Cams Xtreme 4×4 line) give better results at this displacement — see `work/upgrades/engine/stroker-head-and-intake.md` |

**Expected results (documented, naturally aspirated):** ~240 hp @ 5,250 RPM, ~280 lb-ft @ 3,500 RPM. Broad torque band from ~1,600 RPM.

---

## ~4.7L Stroker (bore + stroke)

**Target displacement:** ~284ci at +0.060" overbore. Same crank as above.

| Component | Specification vs 4.6L build |
|-----------|-----------------------------|
| Crankshaft | Identical — AMC 258, 3.895″ stroke |
| Bore | +0.060″ over stock (3.935″) |
| Pistons | Same KB forged family, sized to the +0.060" bore |
| Everything else | Same as 4.6L build |

The displacement gain over the 4.6L build is approximately 4ci — meaningful but not transformative. The additional overbore adds cost (machining, piston selection) and removes future rebuild margin. Most builders who prioritize budget choose the 4.6L build. The 4.7L is worth it if the block is already being bored, or if maximum displacement is the goal.

---

## What is NOT needed for the basic 258-crank stroker

- **Rod journal grinding:** Not needed. The 258 crank fits the 4.0L block on shared journal dimensions. Grinding is only for offset-stroke builds pushing beyond 3.895".
- **Crank spacers for snout:** Only needed if using a pre-1987 (64mm snout) crank with a 4.0L harmonic balancer.
- **Custom rods:** Not required for either build. Factory 258 or 4.0L rods work within acceptable rod ratio limits.

---

## See also

- `work/upgrades/engine/stroker-overview.md` — what stroking means, block selection, displacement math
- `work/upgrades/engine/stroker-ecu-implications.md` — fuel and ignition management for a stroked engine
- `work/upgrades/engine/stroker-head-and-intake.md` — head, cam, intake, exhaust

## Sources

JeepStrokers.com crankshaft FAQ and build recipes (Russ Pottenger); NAXJA build threads; JeepForum stroker discussions; displacement calculations from JeepStrokers.com calculator.
