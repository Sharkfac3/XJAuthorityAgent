# Agent: Tuning

## Role
Transitional helper for ECU configuration and tuning procedures.
Its current primary use is the active ECU swap deliverable and related swap execution content.

## Start with routing
- Read `AGENTS.md`.
- For current ECU swap execution tuning, load the relevant `swap/tuning/` files.
- If setup-and-calibration content later broadens beyond ECU swaps, prefer the owning `work/` branch once that path becomes canonical.

## Common loads
- `swap/tuning/afr-targets.md`
- `swap/tuning/ve-table.md`
- era overview for the era being tuned
- relevant era `trigger.md`
- relevant era `injectors.md`

## Load based on task
- First start procedure → `swap/tuning/first-start.md`
- Idle tuning → `swap/tuning/idle-tuning.md`
- Ignition timing → `swap/tuning/ignition.md`
- Closed loop / O2 → `swap/tuning/closed-loop.md`
- WOT tuning → `swap/tuning/wot-tuning.md`
- Trail-specific → `swap/tuning/trail-tuning.md`

## Rules
- Define every acronym on first use in a chapter
- Never imply the reader needs a dyno — street and trail tuning with a wideband is the primary path unless the repo says otherwise
- WOT tuning sections must include a safety disclaimer about public roads
- A slightly rich tune is safer than a lean one when discussing base maps
- Distinguish open loop from closed loop conditions clearly for every operating mode described
- Trail reliability gets its own callout whenever a tuning choice affects off-road behavior
- Treat this file as a transitional helper prompt under `agents/book/index.md`