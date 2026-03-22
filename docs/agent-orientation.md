# Agent Orientation

Use this document after `AGENTS.md` when you need a concise entry workflow for navigating, contributing to, or expanding the repo.

## Purpose
Give future agents a repeatable low-token startup path that keeps:
- routing fast
- domain ownership clear
- canonical truth in the content tree
- human-facing and agent-facing navigation aligned

## Required reading order for repo-governance work
1. `SKILL.md`
2. `AGENTS.md`
3. `docs/project-reframe.md`
4. `docs/repo-taxonomy.md`
5. `docs/routing-principles.md`
6. `docs/naming-conventions.md`
7. `docs/structure-map.md`
8. this file
9. `docs/content-governance.md`
10. `docs/file-creation-rules.md`
11. relevant files under `agents/` and `skillbuilding/` only as needed

## Cold-start workflow
1. Identify whether the task is technical content work or repo-governance work.
2. Classify the task type before loading content.
3. Load the owning top-level branch router first.
4. Load one narrow branch router if needed.
5. Load only the leaf files needed to answer or edit.
6. If creating content, place it in the canonical content tree, not in `agents/` or `docs/`.

## Task classification test
Ask these questions in order.

### 1. Is the task about stock platform truth?
Examples:
- what a factory XJ used
- year or package differences
- stock subsystem behavior

Load first: `vehicle/`

### 2. Is the task about doing a job?
Examples:
- maintenance
- replacement
- restoration
- upgrades
- swaps

Load first: `work/`

### 3. Is the task about isolating a fault?
Examples:
- no-start
- overheating
- voltage drop
- brake pull

Load first: `diagnostics/`

### 4. Is the task about choosing parts, donors, connectors, or kits?
Load first: `sourcing/`

### 5. Is the task about writing or presentation?
Load first: `book/`

### 6. Is the task about repo structure, migration, placement, or gap planning?
Load first: `docs/` and `skillbuilding/`

## Stock facts vs work procedures
Use this distinction every time.

### Stock fact
A file belongs in `vehicle/` when it answers:
- what Jeep built
- what changed by year, era, package, drivetrain, or subsystem
- how a stock system is arranged

### Work procedure
A file belongs in `work/` when it answers:
- how to service, replace, install, adjust, upgrade, restore, or swap something
- what sequence to follow
- what to verify before and after the job

## Maintenance vs repairs vs upgrades vs swaps vs diagnostics
### Maintenance
Routine service, refresh, wear-item replacement, inspection-driven upkeep.

Home: `work/maintenance/`

### Repairs
Fixing a failed, damaged, or degraded component or assembly.

Home: `work/repairs/`

### Upgrades
Improving a system while keeping the same basic role.

Home: `work/upgrades/`

Example: brake upgrade, alternator upgrade, suspension improvement.

### Swaps
Changing assembly identity, donor family, or control architecture.

Home: `work/swaps/`

Example: ECU swap, axle swap, drivetrain swap.

### Diagnostics
Finding the cause of a symptom through tests and decision logic.

Home: `diagnostics/`

Rule: diagnostics may point to a repair or upgrade path, but they do not own the procedure.

## Top-level branch to load first
- stock identification or factory configuration → `vehicle/`
- maintenance or repair procedure → `work/`
- troubleshooting workflow → `diagnostics/`
- parts or donor decision → `sourcing/`
- human-facing output or style → `book/`
- repo-building or restructure → `docs/` and `skillbuilding/`
- ECU swap execution during migration → `swap/`

## Load-by-task examples
### Stock identification question
Question: “What transfer case did a 1997 4WD automatic XJ use?”
- Load first: `vehicle/index.md`
- Then: `vehicle/configurations/index.md` or current canonical year/era files
- Then the narrowest transfer-case baseline file

### Maintenance procedure request
Question: “How do I service the cooling system?”
- Load first: `work/index.md`
- Then: `work/maintenance/index.md`
- Then the cooling branch

### Diagnostic workflow request
Question: “Why does it overheat at idle?”
- Load first: `diagnostics/index.md`
- Then: `diagnostics/cooling/index.md`
- Then the overheating leaf

### Axle swap planning question
Question: “How should I plan a rear axle swap?”
- Primary: `work/swaps/index.md`
- Support: `sourcing/interchange/index.md`
- Stock baseline support: `vehicle/systems/axles/` or current equivalent

### Brake upgrade question
Question: “How do I plan a WJ brake upgrade?”
- Primary: `work/upgrades/index.md`
- Support: `sourcing/interchange/brakes/`
- Stock baseline support: `vehicle/systems/brakes/`

### ECU swap wiring question
Question: “How do I wire an aftermarket ECU into this XJ?”
- Current canonical first load: `swap/index.md`
- Then: `swap/wiring/`
- Support: relevant `vehicle/` era wiring facts

### Body/interior repair question
Question: “How do I repair a sagging headliner?”
- Load first: `work/repairs/index.md`
- Then: interior/body branch

### Repo-building or restructure task
Question: “Where should I put new factory brake coverage?”
- Load first: `docs/repo-taxonomy.md`
- Then: `docs/routing-principles.md`
- Then: `docs/file-creation-rules.md`
- Use `skillbuilding/` only if doing gap analysis, backlog, or framework work

## Canonical truth rules
- `vehicle/`, `work/`, `diagnostics/`, `sourcing/`, and current `swap/` hold technical truth.
- `agents/` holds behavior only.
- `docs/` holds governance only.
- `skillbuilding/` holds repo-improvement workflows only.
- `book/` holds presentation rules only.

## When to read `agents/` or `skillbuilding/`
Read `agents/` only when you need role-specific behavior.
Read `skillbuilding/` only when the task is repo expansion, auditing, research intake, or backlog planning.

Do not read them as substitutes for canonical Jeep content.

## Token discipline
- Prefer one domain router, one branch router, and only the needed leaves.
- Do not sweep whole domains for ordinary tasks.
- Do not read multiple compatibility branches unless the task compares them.
- Do not load governance docs for ordinary technical Q&A.

## Alignment rule
If human-facing navigation and agent-facing routing diverge, fix the router and path structure so both point to the same canonical leaf.

The repo should not have one navigation system for humans and another hidden one for agents.
