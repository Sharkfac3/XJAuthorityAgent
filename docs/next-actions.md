# Next Actions

## Goal
Track the next bounded structural work now that the broad reframe, scaffold, and front-door cleanup are already in place.

This file should prefer:
- small navigation and governance hardening
- disciplined split plans for mixed legacy files
- backlog-ready branch packages over ad hoc expansion

## Recently completed and now considered stable
These no longer need to sit at the top of the queue:
- front-door repo identity alignment
- initial `swap/` transitional framing in live routing
- first pass of agent scaffolding alignment
- README vs `index.md` operating policy
- documenting `humans/` as temporary process-artifact storage

Current convention reference:
- `docs/transition-status.md`
- `docs/post-cleanup-validation.md`

## Highest-priority next work

### 1. Execute the first remaining mixed-purpose split wave
Focus on the highest-distortion legacy canon that still teaches the old structure by example:
- `vehicle/engine.md`
- `vehicle/trans/aw4.md`
- `vehicle/trans/manual.md`
- `vehicle/era1/diagnostics.md`
- `vehicle/era2/diagnostics.md`
- `vehicle/era3/diagnostics.md`
- `vehicle/era1/wiring.md`
- `vehicle/era2/wiring.md`
- `vehicle/era3/wiring.md`
- `swap/wiring/connectors/index.md` and related connector-family branches

Target outcome:
- stock facts migrate toward `vehicle/systems/`
- diagnostic logic migrates toward `diagnostics/`
- inspection/pre-swap workflow lands under `work/inspections/`
- sourcing-style connector choice content lands under `sourcing/connectors/`
- `swap/` keeps only the execution logic that still truly belongs there

### 2. Continue router hardening where scaffold language still dominates
Remaining weak spots are mostly not wrong, but still too generic to be strong local routers.

Primary sweep targets:
- scaffold-light `work/**/index.md` files
- scaffold-light `diagnostics/*/index.md` files
- scaffold-light `sourcing/**/index.md` files that still advertise expected branches more than real branch shape

Target outcome:
- each router advertises branch-true child packages or symptom families
- generic compatibility boilerplate is reduced where it adds little signal
- local routers become trustworthy enough to guide cold-start agents without broad repo reads

### 3. Strengthen the live bridge into `work/swaps/ecu/`
Current bridging works, but it is still mostly a routing shell.

Next work:
- tighten cross-links between `work/swaps/ecu/` and the active `swap/` tree
- move or mirror only the routing/value-add material that clarifies the target branch
- avoid conceptual growth under `swap/` unless the change is explicitly part of ECU execution canon

Target outcome:
- `work/swaps/ecu/` becomes the obvious place to start
- `swap/` behaves more like a compatibility-preserving execution branch

## Best next branch packages to harden
These branches are mature enough to justify deliberate hardening instead of more raw scaffolding.

### Stock baseline branches
- `vehicle/systems/transmission/` with AW4 and manual leaves
- `vehicle/systems/axles/`
- expansion around existing `vehicle/systems/cooling/`, `brakes/`, `charging-starting/`, and `fuel/`

### Diagnostics branches
- `diagnostics/brakes/` starter leaves for soft pedal, pull, and vibration
- `diagnostics/driveline/` starter vibration-isolation leaves
- `diagnostics/ignition/` or `diagnostics/engine/` crank-no-start starter leaves

### Sourcing branches
- `sourcing/connectors/` beyond the first pigtail decision leaf
- `sourcing/interchange/electrical/`
- `sourcing/interchange/axles/`
- `sourcing/interchange/brakes/`

### Work branches
- `work/maintenance/brakes/`
- `work/maintenance/fuel/`
- `work/maintenance/transmission/`
- one visible non-ECU upgrade or repair package such as:
  - `work/upgrades/brakes/wj-brake-upgrade/`
  - `work/upgrades/driveline/sye/`
  - `work/repairs/interior/headliner-repair/`

## Items to keep in backlog, not improvise during routine maintenance
- final long-term home for shared helper prompts under `agents/`
- broader multi-deliverable structure inside `book/`
- final `vehicle/years/` convention for year-specific files like 1996 notes
- final split between ECU-specific and general `work/setup-and-calibration/` content
- any broad evidence-sensitive content expansion that needs research intake first

## Deprecated patterns to continue blocking
Do not reintroduce these during ordinary growth:
- treating `swap/` as the default start for any technical question
- adding new mixed-purpose legacy files near the root of a domain
- letting README files drift away from branch `index.md` routers
- using `humans/` as a durable content root
- copying technical truth into `agents/`, `docs/`, `book/`, or `skillbuilding/`
- broadening scaffold routers with filler examples that are not branch-true

## Recommended execution order
1. split the highest-distortion mixed legacy files
2. harden the weakest remaining routers
3. strengthen `work/swaps/ecu/` as the preferred live bridge
4. harden the next small branch packages in stock baselines, diagnostics, sourcing, and work
5. only then expand into broader coverage families

## Bottom line
The repo does not need another redesign pass.
It needs continued hardening of the live migration surface, especially where old mixed files and scaffold-light routers still encourage drift.
