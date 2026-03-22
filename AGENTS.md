# XJ Authority Agent

Primary entrypoint for agents entering this repository.

Read this file after `SKILL.md`. Then classify the task, load one domain router, and load only the narrowest truthful leaves.

## Repo identity
This repo is a **Jeep XJ technical knowledge system**.

ECU swaps remain important, but they are now one branch inside a larger structure that must support:
- stock platform identification and configuration facts
- maintenance, repair, restoration, and setup work
- diagnostics and fault isolation
- upgrades and major swaps
- sourcing, interchange, and donor decisions
- year, trim, package, drivetrain, and subsystem differences

## Non-negotiable rules
- Keep canonical truth in the content tree, not in `agents/`.
- Use `agents/` for behavior and routing only.
- Use `docs/` for governance and structure rules only.
- Use `skillbuilding/` for repo-building workflows only.
- Treat `swap/` as the current canonical ECU swap branch during migration.
- Prefer deep, narrow files over broad summary files.
- Cross-link to canonical files instead of duplicating facts.

## Session context — edit the repo root copy
The canonical repo root is the directory containing this file.

If your session is running in a nested worktree under `.claude/worktrees/`, always edit the file at the repo root, not the worktree copy.

Guardrail:
- never edit a path that contains `.claude/worktrees/`

## Start here for governance and routing
For repo-entry guidance and file placement rules, load these in order when doing repo-structure, governance, or file-creation work:
1. `docs/project-reframe.md`
2. `docs/repo-taxonomy.md`
3. `docs/routing-principles.md`
4. `docs/naming-conventions.md`
5. `docs/structure-map.md`
6. `docs/agent-orientation.md`
7. `docs/content-governance.md`
8. `docs/file-creation-rules.md`

## Top-level domain map
- `vehicle/` — stock Jeep XJ facts and baselines
- `work/` — maintenance, repairs, restoration, upgrades, swaps, inspections, setup
- `diagnostics/` — symptom-first troubleshooting and fault isolation
- `sourcing/` — parts, donor, connector, and interchange decisions
- `swap/` — legacy-but-current ECU swap execution content during migration
- `book/` — presentation rules for human-facing output
- `agents/` — agent behavior and routing only
- `docs/` — governance, taxonomy, naming, and migration rules
- `skillbuilding/` — repo-building audits, backlog, research intake, and hardening
- `humans/` — temporary process-artifact prompt archive; not a canonical content domain

## Classify the task first
Ask these questions in order:
1. Is the user asking **what the XJ has, had, or came with**? → `vehicle/`
2. Is the user asking **how to do a job**? → `work/`
3. Is the user asking **what is wrong and how to isolate it**? → `diagnostics/`
4. Is the user asking **which part, donor, connector, or kit to choose**? → `sourcing/`
5. Is the user asking **how the answer should be written or presented**? → `book/`
6. Is the user asking **how the repo should evolve, be audited, or be restructured**? → `docs/` and `skillbuilding/`

Then ask:
- Is this **stock baseline** or **modified-state** guidance?
- Is this **maintenance**, **repair**, **upgrade**, **swap**, **restoration**, **inspection**, or **setup**?
- Which system owns the topic?
- Do year, era, package, drivetrain, ABS, transmission, axle family, or donor family change the answer?

## Domain ownership rules
### `vehicle/` — stock facts
Use for:
- factory configurations
- year and era differences
- package and drivetrain baselines
- stock subsystem architecture
- stock interchange baselines

Do not use for:
- procedures
- troubleshooting trees
- buying advice

### `work/` — procedures and project execution
Use for:
- maintenance
- repairs
- restoration
- upgrades
- swaps
- inspections
- setup and calibration

Do not use for:
- pure stock fact storage
- symptom-first diagnosis
- donor/parts comparisons as the primary topic

### `diagnostics/` — fault isolation
Use for:
- symptoms
- tests
- decision trees
- verification paths

### `sourcing/` — selection decisions
Use for:
- donor choices
- part-family comparisons
- OEM vs aftermarket decisions
- connector and kit selection

### `agents/` — behavior only
Never use `agents/` as a Jeep fact store.

## Load by task
### Stock fact question
- Start with `vehicle/index.md`
- Then one of:
  - `vehicle/years/index.md`
  - `vehicle/systems/index.md`
  - `vehicle/packages/index.md`
  - `vehicle/configurations/index.md`
  - `vehicle/interchange-baselines/index.md`
- During transition, use current canonical branches such as `vehicle/era1/`, `vehicle/era2/`, `vehicle/era3/`, and `vehicle/trans/`

### Work procedure question
- Start with `work/index.md`
- Then the work-class index:
  - `work/maintenance/index.md`
  - `work/repairs/index.md`
  - `work/restoration/index.md`
  - `work/upgrades/index.md`
  - `work/swaps/index.md`
  - `work/inspections/index.md`
  - `work/setup-and-calibration/index.md`
- Then load the narrowest system or project branch

### Diagnostic question
- Start with `diagnostics/index.md`
- Then the relevant system branch such as:
  - `diagnostics/engine/index.md`
  - `diagnostics/fuel/index.md`
  - `diagnostics/ignition/index.md`
  - `diagnostics/cooling/index.md`
  - `diagnostics/charging-and-starting/index.md`
  - `diagnostics/transmission/index.md`
  - `diagnostics/transfer-case/index.md`
  - `diagnostics/driveline/index.md`
  - `diagnostics/steering-and-suspension/index.md`
  - `diagnostics/brakes/index.md`
  - `diagnostics/body-electrical/index.md`
  - `diagnostics/body-and-interior/index.md`

### Sourcing question
- Start with `sourcing/index.md`
- Then the relevant decision branch such as:
  - `sourcing/interchange/index.md`
  - `sourcing/donor-vehicles/index.md`
  - `sourcing/oem-vs-aftermarket/index.md`
  - `sourcing/connectors/index.md`
  - `sourcing/swap-kits/index.md`
  - `sourcing/wear-items/index.md`

### ECU swap work during transition
- Start with `swap/index.md`
- Use current canonical files under `swap/` for ECU selection, wiring, tuning, and related execution
- Treat `swap/...` as the active equivalent of future `work/swaps/ecu/...`

### Writing and presentation
- `book/audience.md`
- `book/writing/style.md`
- `book/writing/callouts.md`
- `book/writing/safety.md`
- `book/outline.md`

### Repo-building and restructure work
- `docs/project-reframe.md`
- `docs/repo-taxonomy.md`
- `docs/routing-principles.md`
- `docs/naming-conventions.md`
- `docs/structure-map.md`
- `docs/agent-orientation.md`
- `docs/content-governance.md`
- `docs/file-creation-rules.md`
- `skillbuilding/index.md`

## Quick routing examples
- Stock identification question: “What axle did a 1998 4.0/AW4 XJ usually get?” → `vehicle/`
- Maintenance procedure request: “How do I refresh the cooling system?” → `work/maintenance/`
- Diagnostic workflow request: “Why does it crank but not start?” → `diagnostics/`
- Axle swap planning question: “How should I plan a Dana 44 axle swap?” → `work/swaps/axles/` + `sourcing/interchange/axles/` + stock baseline in `vehicle/systems/axles/`
- Brake upgrade question: “How do I do a WJ brake upgrade?” → `work/upgrades/brakes/` + supporting `sourcing/` and `vehicle/`
- ECU swap wiring question: “How do I wire an aftermarket ECU into this XJ?” → current `swap/wiring/` + supporting era facts in `vehicle/`
- Body/interior repair question: “How do I repair a sagging headliner or broken interior trim?” → `work/repairs/interior/` or `work/restoration/interior/`
- Repo-building/restructure task: “Where should new axle coverage live?” → `docs/` + `skillbuilding/`

## Transitional mappings
Use the target architecture for routing, but respect current canonical branches during migration.

- future `work/swaps/ecu/...` → current `swap/...`
- future `vehicle/years/era1/...` → current `vehicle/era1/...`
- future `vehicle/years/era2/...` → current `vehicle/era2/...`
- future `vehicle/years/era3/...` → current `vehicle/era3/...`
- future stock transmission system branch → current `vehicle/trans/...`

## Token discipline
- Load one domain router before many leaves.
- Prefer one system/work branch and only the necessary leaves.
- Do not load multiple era overviews unless comparing eras.
- Treat `index.md` and `overview.md` as routers, not hidden mega-docs.
- Use governance docs only for governance, migration, naming, or placement work.

## Anti-drift rules
- Do not store Jeep technical facts in `agents/`.
- Do not create parallel fact stores in `docs/`, `skillbuilding/`, or `book/`.
- Do not force non-swap work into `swap/` just because it already exists.
- Do not mix stock facts, procedures, diagnostics, and sourcing in one file unless the topic is truly tiny.
- Do not create vague folders like `misc/`, `general/`, `other/`, or `notes/`.
- Do not overwrite current canonical ECU swap content during scaffold work unless the task explicitly requires migration.
