# Transfer Case Overview

## Purpose
Stock XJ transfer case families, specifications, and year/package differences.

## Scope
Factory transfer case configurations for the 1984–2001 Jeep Cherokee XJ. This branch covers the transfer case hardware itself — engagement behavior and front axle disconnect are documented under [`../4wd/overview.md`](../4wd/overview.md).

## What belongs here
- stock transfer case architecture and specifications
- factory component-family differences
- year, era, package, or drivetrain splits that materially affect this system
- links to narrower factual leaves as this branch grows

## What does not belong here
- 4WD engagement logic, mode positions, or front axle disconnect → [`../4wd/overview.md`](../4wd/overview.md)
- service or installation procedures → `work/`
- symptom-first diagnostics paths → `diagnostics/`
- donor-part buying advice → `sourcing/`

---

## Transfer case families

### Era 1 — 1984–1986: NP207 / NP228 / NP229

| Spec | NP207 | NP228 / NP229 |
|------|-------|---------------|
| Brand name | Command-Trac | Selec-Trac |
| Type | Part-time only | Part-time + full-time |
| Low range ratio | 2.61:1 | 2.61:1 |
| High range ratio | 1.00:1 | 1.00:1 |
| Drive | Chain-driven | Chain-driven |
| Case material | Aluminum | Aluminum |
| Input spline (manual trans) | 21-spline | 21-spline |
| Input spline (auto trans) | 23-spline | 23-spline |
| Center differential | None | Yes (full-time mode) |

The NP207 is widely considered the weakest XJ transfer case — smaller chain and lighter internals than the NP231 that replaced it.

### Era 2 — 1987–2001: NP231 / NP242

| Spec | NP231 | NP242 |
|------|-------|-------|
| Brand name | Command-Trac | Selec-Trac |
| Type | Part-time only | Part-time + full-time |
| Low range ratio | 2.72:1 | 2.72:1 |
| High range ratio | 1.00:1 | 1.00:1 |
| Drive | Chain-driven | Chain-driven |
| Case material | Aluminum | Aluminum |
| Input spline | 21-spline (early) / 23-spline | 21-spline (early) / 23-spline |
| Center differential | None | Open center diff (approx. 48/52 front/rear in full-time mode) |
| Approximate weight | Lighter | ~20 lb heavier, hangs ~1" lower |
| Aftermarket support | Extensive (SYE, 4:1 kit, slip yoke eliminator) | More limited |

Both use a slip-yoke rear output in stock form. The slip yoke is a common vibration source on lifted XJs — a slip yoke eliminator (SYE) kit with a custom driveshaft is the standard fix, and is much more widely available for the NP231.

## Year / package matrix

| Year range | Command-Trac (part-time) | Selec-Trac (full-time) |
|------------|--------------------------|------------------------|
| 1984–1986 | NP207 | NP228 / NP229 |
| 1987–2001 | NP231 | NP242 |

2WD XJs have no transfer case.

## Child leaves
- [shifting-procedure.md](shifting-procedure.md) — redirect to shifting procedures in `work/`

## Expected child branches
- `np231.md` and `np242.md` when detailed internal specs or rebuild context warrants separation

## Cross-links
- 4WD engagement system (mode positions, front axle disconnect): [`../4wd/overview.md`](../4wd/overview.md)
- Stock axle families: [`../axles/overview.md`](../axles/overview.md)
- 2WD vs 4WD configuration: [`../../configurations/2wd-vs-4wd.md`](../../configurations/2wd-vs-4wd.md)

## Boundary links
- Transfer case swap execution: `work/swaps/transfer-case/`
- Transfer case diagnostics: `diagnostics/transfer-case/`

## Sources
Community-verified via NAXJA, JeepForum, CherokeeTalk; cross-referenced against Jeep four-wheel-drive systems (Wikipedia) and New Process Gear transfer case identification references.
