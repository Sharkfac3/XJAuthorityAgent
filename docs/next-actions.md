# Next Actions

## Goal
Prioritized follow-up work to make the retooled repo easier for agents to navigate and easier to scale.

## Immediate fixes

### 1. Unify repo identity at all front doors
Update these paths first:
- `README.md`
- `swap/README.md`
- `swap/index.md`
- `vehicle/README.md`
- `agents/assistant/index.md`
- `agents/book/index.md`
- `book/outline.md`

Target outcome:
- every entrypoint describes the repo as a **Jeep XJ technical knowledge system**
- `swap/` is described as a **transitional canonical ECU branch**, not the repo center
- agent routers classify by question type first

### 2. Replace template router language with branch-specific routing guidance
First pass targets:
- all `work/**/index.md`
- all `diagnostics/*/index.md`
- `sourcing/connectors/index.md`
- `work/swaps/ecu/index.md`

Target outcome:
- no more generic example child names like `headliner-repair/` inside unrelated branches
- no more repeated generic diagnostic examples that do not fit the branch
- each router advertises likely real children for that branch

### 3. Mark `swap/` as compatibility-first in live routing
Update:
- `swap/index.md`
- `swap/README.md`
- `work/index.md`
- `work/swaps/ecu/index.md`

Target outcome:
- new work routes point to `work/swaps/ecu/`
- legacy swap files stay valid but clearly transitional

### 4. Decide and document the status of `humans/`
Pick one:
- keep and document it as temporary process-artifact storage, or
- relocate/archive it under a documented meta root

Target outcome:
- no undocumented top-level roots remain

## Medium-term structural improvements

### 1. Execute the first split wave for mixed-purpose legacy files
Highest-value split targets:
- `vehicle/trans/aw4.md`
- `vehicle/trans/manual.md`
- `vehicle/engine.md`
- `vehicle/era1/diagnostics.md`
- `vehicle/era2/diagnostics.md`
- `vehicle/era3/diagnostics.md`
- `vehicle/era1/wiring.md`
- `vehicle/era2/wiring.md`
- `vehicle/era3/wiring.md`
- `swap/wiring/connectors/index.md` and connector family branches

Target outcome:
- stock facts move toward `vehicle/systems/`
- diagnostics move into `diagnostics/`
- pre-swap inspection content moves into `work/inspections/`
- connector decision content moves toward `sourcing/connectors/`
- swap procedure content remains in `swap/` or moves into `work/swaps/ecu/` as appropriate

### 2. Establish a single README/index policy
Needed because current repo navigation is split.

Recommended policy:
- `index.md` is canonical router
- `README.md` is optional lightweight human intro only
- README files must never contradict `index.md`

### 3. Add a short transition-status or decision-register file
Create a lightweight governance note that records:
- migration decisions already locked
- migration decisions still provisional
- path conventions currently in force

### 4. Finish the live migration bridge into `work/swaps/ecu/`
Medium-term path work:
- strengthen `work/swaps/ecu/` as the preferred destination
- convert `swap/` into redirect-compatible routing over time
- avoid new conceptual growth under `swap/` except where migration explicitly requires it

## First high-value content branches to build out

These are the best first content packages because they improve platform usefulness fast and validate the new architecture.

### 1. Stock baselines that unlock many downstream branches
Build first:
- `vehicle/systems/cooling/`
- `vehicle/systems/brakes/`
- `vehicle/systems/charging-starting/`
- `vehicle/systems/fuel/`
- `vehicle/systems/transmission/` with AW4 and manual leaves
- `vehicle/systems/axles/`

Why:
- these support maintenance, diagnostics, sourcing, and upgrade work
- they reduce dependence on legacy swap-support phrasing

### 2. Common maintenance branches
Build first:
- `work/maintenance/cooling/`
- `work/maintenance/brakes/`
- `work/maintenance/charging-starting/`
- `work/maintenance/fuel/`
- `work/maintenance/transmission/`
- `work/maintenance/axles/`

Why:
- broadest owner value
- helps prove the repo is not swap-only

### 3. High-frequency diagnostic leaves
Build first:
- `diagnostics/ignition/` or `diagnostics/engine/` for crank-no-start
- `diagnostics/cooling/overheating-at-idle.md`
- `diagnostics/charging-and-starting/low-charging-voltage.md`
- `diagnostics/fuel/fuel-pump/no-prime.md`
- `diagnostics/brakes/` for pull, soft pedal, and vibration starters
- `diagnostics/driveline/` for vibration isolation starter

Why:
- high reader impact
- strong proof that diagnostics is now a first-class domain

### 4. High-friction sourcing branches
Build first:
- `sourcing/connectors/` from split connector content
- `sourcing/interchange/axles/`
- `sourcing/interchange/brakes/`
- `sourcing/interchange/electrical/`
- `sourcing/oem-vs-aftermarket/cooling/`

Why:
- reduces wrong-part drift
- supports both stock and modified workflows

### 5. One or two visible non-ECU upgrade/repair packages
Best candidates:
- `work/upgrades/brakes/wj-brake-upgrade/`
- `work/upgrades/driveline/sye/`
- `work/repairs/interior/headliner-repair/`

Why:
- proves the broader architecture in actual content, not just scaffold

## Deprecated patterns to stop using

Stop using these patterns for new work:
- treating `swap/` as the default first stop for every technical question
- telling agents to always load `vehicle/engine.md`
- leaving generic scaffold examples in branch routers
- writing new mixed-purpose files that blend stock facts, procedure, diagnostics, and sourcing
- growing root or near-root legacy files instead of splitting into deep branches
- letting README files carry a different routing model than `index.md` or `AGENTS.md`
- using undocumented top-level roots without governance coverage
- keeping project-specific book artifacts at the root of `book/` if they are not general presentation rules

## Unresolved open questions

### 1. What is the final canonical policy for README vs `index.md`?
This should be decided soon to avoid navigation drift.

### 2. Where should project-specific human deliverables live inside `book/`?
`book/outline.md` is the immediate example.

### 3. What is the final long-term home for shared helper prompts in `agents/`?
Current top-level helper files still exist, but their future placement is unresolved.

### 4. What is the final convention for year-specific files inside `vehicle/years/`?
Especially:
- `vehicle/years/1996-notes.md` vs `vehicle/years/era3/1996-notes.md`

### 5. Which setup/calibration topics should remain ECU-swap-specific, and which should eventually generalize under `work/setup-and-calibration/`?

### 6. Should `humans/` remain a permanent root?
If yes, it needs explicit governance.
If no, it should be archived or relocated.

## Recommended order of execution

1. unify entrypoint identity
2. fix generic routers
3. document `humans/` status and README/index policy
4. split the highest-distortion mixed legacy files
5. strengthen `work/swaps/ecu/` as the preferred active target
6. build the first stock baseline, maintenance, diagnostics, and sourcing packages
7. then expand into broader upgrades, repairs, restoration, and non-ECU swap branches

## Bottom line
The next highest-value work is to **finish the navigation and migration surface**, not to add many more folders.

Once the front doors, routers, and first split wave are cleaned up, new content can scale much more safely and the repo will read clearly as a platform-wide Jeep XJ system.