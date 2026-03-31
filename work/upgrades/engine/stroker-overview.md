# Stroker Overview — Jeep 4.0L Inline-Six

## What "stroking" means

Stroking an engine increases displacement by replacing the factory crankshaft with one that moves the pistons through a longer stroke. A longer stroke means each cylinder sweeps more volume per revolution, which increases displacement and — when the rest of the engine is built to match — produces more torque across a wider RPM range.

The 4.0L inline-six is a well-suited stroker candidate. The block has adequate room for a longer crank throw without wall interference, the head bolt pattern and bore dimensions are shared across decades of AMC/Jeep inline-six production, and the community has accumulated extensive documented build experience going back to the early 2000s. JeepStrokers.com (run by builder Russ Pottenger) is the primary reference community for this platform.

---

## Stock 4.0L baseline

| Spec | Value |
|------|-------|
| Bore | 3.875″ |
| Stroke | 3.411″ |
| Displacement | 242ci (3,964cc) |

---

## The stroker crank: AMC 258 (4.2L)

The most common and community-proven path is to install the **AMC/Jeep 258ci (4.2L) crankshaft**, which has a **3.895″ stroke**. The 258 and 4.0L share the same main journal and rod journal dimensions, so the 258 crank drops into the 4.0L block without journal modification.

### Displacement by bore size

| Bore | Configuration | Displacement |
|------|---------------|-------------|
| Stock 3.875″ | 258 crank only | 276ci (~4.5L) |
| +0.030″ overbore | 258 crank + bore | ~280ci (~4.6L) |
| +0.060″ overbore | 258 crank + bore | ~284ci (~4.7L) |

The community frequently calls the +0.030" overbore build a "4.6L stroker" and the +0.060" overbore a "4.7L stroker." A stock-bore 258-crank build is technically ~4.5L but will be called a stroker in any context.

---

## Recommended block foundation

The **1996+ NVH block** is the community-preferred foundation for stroker builds. The 1996 redesign added main bearing web ribbing and a main bearing stud girdle that provide real structural benefit under higher cylinder pressures.

See `vehicle/era2/ho-engine.md` → Block compatibility section for NVH block identification, casting numbers, and Group A/Group B motor mount compatibility. Motor mount group compatibility is a more urgent concern than block year — a Group B block in a Group A chassis requires fabrication regardless of how good the internals are.

---

## What a stroker changes

- **Displacement and torque:** The primary gain is a broader, stronger torque curve. Documented results from the 4.6L build show torque increasing from approximately 240 lb-ft to 280 lb-ft with a wider powerband starting from 1,600 RPM.
- **Required Fuel calculation:** The ECU calculates injector pulse width from displacement. A larger-displacement engine changes the fuel demand equation — see `work/upgrades/engine/stroker-ecu-implications.md`.
- **Head and induction demand:** A stroked engine will expose restrictions in the stock head and intake sooner. See `work/upgrades/engine/stroker-head-and-intake.md`.
- **Internals:** Pistons must be selected for the resulting bore and deck clearance. Connecting rod choice affects the rod-to-stroke ratio, which is a real engineering concern at 1.50:1 minimum for street use.

---

## See also

- `work/upgrades/engine/stroker-combinations.md` — specific parts lists for the 4.6L and 4.7L builds
- `work/upgrades/engine/stroker-ecu-implications.md` — ECU and injector considerations
- `work/upgrades/engine/stroker-head-and-intake.md` — head, intake, cam, and exhaust for a stroked engine
- `vehicle/era2/ho-engine.md` — block selection, NVH blocks, valve train baseline

## Sources

JeepStrokers.com (Russ Pottenger), NAXJA forums, JeepForum, Wrangler TJ Forum; displacement math verified against JeepStrokers.com compression ratio calculator.
