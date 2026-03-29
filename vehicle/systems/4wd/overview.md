# 4WD Engagement System Overview

## Purpose
Stock 4WD engagement architecture, transfer case mode positions, and front axle engagement mechanism for the 1984–2001 Jeep Cherokee XJ.

## Scope
Factory 4WD systems only. This branch covers how 4WD engages mechanically — transfer case families, mode positions, and the two-step engagement process (transfer case shift + front axle engagement).

## What belongs here
- stock transfer case mode positions and engagement behavior
- front axle engagement mechanism (CAD vs. always-engaged)
- year, package, and trim splits that determine which system a given XJ has
- links to narrower factual leaves as this branch grows

## What does not belong here
- transfer case dimensional specs or internal rebuild detail → [`../transfer-case/overview.md`](../transfer-case/overview.md)
- axle dimensional specs → [`../axles/stock-specs.md`](../axles/stock-specs.md)
- service or installation procedures → `work/`
- symptom-first diagnostics → `diagnostics/`
- donor-part sourcing → `sourcing/`

---

## How 4WD engagement works on the XJ

4WD engagement on the XJ is a **two-step mechanical process**, not a single event:

1. **Transfer case shift** — the driver moves the shift lever (or pushbutton on some late models) to select a 4WD mode. This connects the front driveshaft to the transfer case output.
2. **Front axle engagement** — the passenger-side inner axle shaft must be mechanically connected so torque can reach both front wheels. On CAD-equipped XJs, this happens via a vacuum-operated disconnect. On non-CAD XJs, the front axle shafts are always connected (one-piece passenger shaft).

If either step fails, the front wheels do not pull. A common diagnostic mistake is blaming the transfer case when the actual failure is at the front axle disconnect.

---

## Transfer case families by era

### Era 1 — 1984–1986: NP207 / NP228 / NP229

The first XJ generation used transfer cases inherited from the AMC/Jeep parts bin:

| Transfer case | Brand name | Type | Low range | Positions |
|--------------|------------|------|-----------|-----------|
| NP207 | Command-Trac | Part-time only | 2.61:1 | 2H – 4H – N – 4L |
| NP228 | Selec-Trac | Part-time + full-time | 2.61:1 | 2H – 4H Full-Time – 4H Part-Time – N – 4L |
| NP229 | Selec-Trac | Part-time + full-time | 2.61:1 | 2H – 4H Full-Time – 4H Part-Time – N – 4L |

The NP207 is chain-driven with an aluminum case, 21-spline input (manual) or 23-spline input (automatic). It is weaker than the NP231 that replaced it — smaller chain and lighter internals. The NP228/NP229 added a center differential for full-time 4WD capability.

**Status: needs verification** — NP228 vs. NP229 distinction and exact year/trim applicability for 1984–1986 XJs is less documented than later transfer cases. Community sources typically group them together.

### Era 2 — 1987–2001: NP231 / NP242

Starting in 1987, the XJ received the New Process 231 and 242 transfer cases that would remain through end of production:

| Transfer case | Brand name | Type | Low range | Positions |
|--------------|------------|------|-----------|-----------|
| NP231 | Command-Trac | Part-time only | 2.72:1 | 2H – 4H – N – 4L |
| NP242 | Selec-Trac | Part-time + full-time | 2.72:1 | 2H – 4H Full-Time – 4H Part-Time – N – 4L |

Both are chain-driven with aluminum cases. The NP231 is slightly lighter and has better aftermarket support (SYE kits, 4:1 low-range kits, "2-Lo" kits). The NP242 is approximately 20 lb heavier and hangs about 1" lower.

---

## Command-Trac vs. Selec-Trac

| Feature | Command-Trac (NP231) | Selec-Trac (NP242) |
|---------|----------------------|---------------------|
| 4WD type | Part-time only | Part-time + full-time |
| Safe on dry pavement in 4H? | **No** — causes driveline binding and premature wear | **Yes** — 4H Full-Time uses open center differential |
| Center differential | None — front and rear outputs locked 1:1 | Open center diff in Full-Time mode (approx. 48/52 front/rear torque split) |
| Center diff lock | N/A | Mechanically locked in 4H Part-Time and 4L |
| Low range ratio | 2.72:1 | 2.72:1 |
| Aftermarket support | Extensive (SYE, 4:1 kit, slip yoke eliminator) | More limited |
| Weight | Lighter | ~20 lb heavier |
| Front axle disconnect (CAD) | Yes, on 1987–~1991 models | **No** — front axle always engaged (one-piece shaft) |

### When to use each mode

**Command-Trac (NP231):**
- **2H** — normal driving, rear-wheel drive only
- **4H** — slippery surfaces only (snow, mud, gravel, sand). Front and rear axles locked 1:1. Do not use on dry pavement — driveline will bind.
- **4L** — low-speed off-road only. Same lock as 4H but with 2.72:1 gear reduction.

**Selec-Trac (NP242):**
- **2H** — rear-wheel drive only
- **4H Full-Time** — safe on any surface. Open center differential allows front and rear axles to turn at different speeds. Small fuel economy penalty vs. 2H.
- **4H Part-Time** — slippery surfaces only. Center differential locked. Equivalent to NP231 4H.
- **4L** — low-speed off-road. Center differential locked with 2.72:1 reduction.

---

## Year / package matrix

| Year range | Command-Trac (part-time) | Selec-Trac (full-time) | Front axle disconnect (CAD) |
|------------|--------------------------|------------------------|-----------------------------|
| 1984–1986 | NP207 | NP228 / NP229 | Yes (Command-Trac models) |
| 1987–~1991 | NP231 | NP242 | Yes (Command-Trac models) |
| 1992–2001 | NP231 | NP242 | No — one-piece passenger shaft |

**Notes:**
- 2WD XJs have no transfer case and no driven front axle.
- Selec-Trac (NP242 / NP228 / NP229) models never used the CAD — full-time 4WD requires the front axle to always be engaged.
- The NP242 was typically a higher-trim or optional feature. Not all 4WD XJs have it.
- Some early 1991 production XJs used leftover CAD assemblies as transition inventory was depleted.

**Status: needs verification** — The exact cutoff between CAD and non-CAD on NP231 models varies by source. 1991 is the most commonly cited last year, with 1992+ universally confirmed as non-CAD.

---

## Child leaves
- [front-axle-disconnect.md](front-axle-disconnect.md) — vacuum-operated Central Axle Disconnect (CAD) system: how it works, why it fails, and CAD delete options
- [locking-hubs.md](locking-hubs.md) — clarification on factory hub design (unit bearings, not locking hubs) and aftermarket locking hub conversion

## Cross-links
- Transfer case specs and internals: [`../transfer-case/overview.md`](../transfer-case/overview.md)
- Stock axle families and year matrix: [`../axles/overview.md`](../axles/overview.md)
- 2WD vs 4WD configuration filter: [`../../configurations/2wd-vs-4wd.md`](../../configurations/2wd-vs-4wd.md)
- Dana 30 front axle architecture: [`../axles/dana30-front.md`](../axles/dana30-front.md)

## Boundary links
- 4WD service and shifting procedures: `work/maintenance/transfer-case/`
- 4WD diagnostics: `diagnostics/transfer-case/` and `diagnostics/driveline/`
- Transfer case swap execution: `work/swaps/transfer-case/`

## Sources
Community-verified via NAXJA, JeepForum, CherokeeTalk, CherokeeForum; cross-referenced against Jeep four-wheel-drive systems (Wikipedia) and factory service manual shift pattern documentation.
