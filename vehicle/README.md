# Vehicle Folder

Canonical stock Jeep XJ platform facts.

Use this folder when the question is what the XJ came with, how a stock system is arranged, or what changed by year, era, package, configuration, or subsystem.

This is not a swap-support-only branch. It is the stock baseline for the broader repository, including maintenance, diagnostics, upgrades, sourcing, and ECU swap work.

## Load strategy
- Start with `vehicle/index.md` for stock-fact routing
- Then load the narrowest year, era, system, package, or configuration branch needed for the question
- During transition, use legacy canonical branches like `era1/`, `era2/`, `era3/`, and `trans/` where the newer target branches are not filled out yet

## Current branch map
- `index.md` — stock-fact router
- `years/` — time-based routing for model-year and era differences
- `systems/` — subsystem-based stock facts
- `packages/` — package-defined stock differences
- `configurations/` — stock configuration matrices
- `interchange-baselines/` — factual stock interchange limits
- `era1/`, `era2/`, `era3/` — legacy-but-current canonical era branches during migration
- `trans/` — legacy-but-current transmission fact branch during migration
- `engine.md` — legacy cross-era engine baseline during migration

## Important rule
If a fact changes by year, era, package, drivetrain, or subsystem family, do not flatten it into a universal statement.
Use the narrowest truthful file.
