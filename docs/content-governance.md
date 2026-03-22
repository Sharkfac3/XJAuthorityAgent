# Content Governance

This document defines how canonical knowledge is owned, how duplication is prevented, and how uncertainty should be handled as the repo expands.

## Governance goals
- keep one canonical home for each truth
- separate facts from procedures, diagnostics, sourcing, and presentation
- preserve year-, era-, package-, and subsystem-specific accuracy
- let humans and agents find the same truth through aligned routers
- make uncertainty explicit instead of silently flattening it

## Canonical ownership model
### Technical content roots
- `vehicle/` — stock platform truth
- `work/` — procedures and project execution
- `diagnostics/` — symptom-first troubleshooting
- `sourcing/` — parts, donor, and interchange decisions
- `swap/` — current canonical ECU swap branch during migration

### Non-canonical support roots
- `agents/` — behavior and routing only
- `docs/` — governance and structure rules only
- `skillbuilding/` — audits, backlog, source intake, maturity workflows only
- `book/` — human-facing presentation guidance only

## Domain boundaries
### Stock facts vs procedures
If the file explains what exists on a stock XJ, it belongs in `vehicle/`.
If the file explains how to do a job, it belongs in `work/`.

### Procedure vs diagnostics
If the file explains what tests isolate a symptom, it belongs in `diagnostics/`.
If the file explains how to replace, adjust, restore, install, upgrade, or swap, it belongs in `work/`.

### Modification vs maintenance
Use `work/maintenance/` for service and refresh work.
Use `work/upgrades/` for improved non-stock outcomes.
Use `work/swaps/` when assembly identity, donor family, or control architecture changes materially.

### Sourcing vs reference
Use `sourcing/` when the primary question is which part, donor, connector, or kit to choose.
Use `vehicle/` when the primary question is what Jeep used or what stock parts fit as a factual baseline.

## Anti-duplication rules
### One truth, many pointers
A fact should have one canonical home.
Other files may:
- summarize briefly for routing
- link to the canonical file
- note local compatibility implications

Other files may not restate the full fact set as a competing source.

### No parallel fact stores
Do not place Jeep technical truth in:
- `agents/`
- `docs/`
- `skillbuilding/`
- `book/`

### Avoid mixed-purpose files
Do not combine these into one file unless the topic is genuinely tiny:
- stock platform facts
- procedures
- diagnostics
- sourcing comparisons
- governance rules

## When to extend an existing branch
Extend an existing branch when:
- the topic fits the branch's existing domain and system boundary
- the new material uses the same compatibility dimensions
- a new leaf can answer one bounded question inside that branch
- the branch router already points naturally to the new content

Examples:
- add a new brake-upgrade leaf under `work/upgrades/brakes/...`
- add a new no-start leaf under `diagnostics/ignition/...`
- add a year-specific brake baseline leaf under `vehicle/systems/brakes/...` or `vehicle/years/...`

## When to create a new branch
Create a new branch when:
- the topic introduces a durable new work class, subsystem, component family, or donor family
- the topic needs multiple child leaves such as overview, compatibility, procedure, and validation
- the current branch would become mixed-purpose or misleading if expanded further
- repeated compatibility caveats show that a dedicated subtree is cleaner

Do not create a new branch just because a topic is long.
Create one when the branch label itself is durable and reusable.

## Deep-tree rule
Prefer adding depth over adding new top-level roots.

Good:
- `work/upgrades/brakes/wj-brake-upgrade/`
- `diagnostics/fuel/fuel-pump/`
- `vehicle/systems/axles/dana-30/`

Avoid:
- new root-level buckets for every new topic
- vague catch-all folders like `misc/`, `general/`, `other/`, or `notes/`

## Handling uncertainty and confidence
Uncertainty must be visible.
Do not silently write broad claims when the repo evidence is narrow or conflicting.

### Use explicit labels in prose
Use labels such as:
- `confirmed`
- `likely`
- `unverified`
- `needs source`
- `year-range uncertain`
- `package-specific uncertainty`
- `transition-year caution`

### Year-range ambiguity rule
If a statement may change by year, era, package, drivetrain, emissions family, ABS, transmission, or axle family:
- state the ambiguity explicitly
- narrow the scope in the path or file title when possible
- prefer a dedicated compatibility or year-specific leaf over repeating caveats everywhere

### Confidence rule
When evidence quality differs across claims:
- keep high-confidence facts separate from provisional notes
- mark provisional claims directly
- point to the missing verification area instead of smoothing over it

## Transition governance
The repo is in migration.
Use the target taxonomy for new placement decisions, but respect current canonical branches.

### Current transitional rules
- ECU swap execution content remains canonical under `swap/`
- current `vehicle/era1/`, `vehicle/era2/`, `vehicle/era3/`, and `vehicle/trans/` remain canonical until migration
- do not force new non-swap content into `swap/`
- do not rewrite present canonical content just to imitate the future tree unless migration is part of the task

## Human-facing and agent-facing alignment
Navigation should stay aligned across:
- top-level routers
- local `index.md` and `overview.md` files
- `AGENTS.md`
- governance docs
- human-facing folder summaries

### Alignment rule
If a human README, an index, and `AGENTS.md` point to different canonical homes for the same topic, fix the routing layer.
Do not allow hidden agent-only placement logic.

## Review checklist for governance-sensitive edits
Before finalizing a change, confirm:
1. Does the file live in the correct top-level domain?
2. Is stock truth separated from procedure and diagnostics?
3. Is modification guidance separated from maintenance when needed?
4. Is there one canonical home for the main truth?
5. Are support files linking instead of duplicating?
6. Are year and compatibility limits explicit?
7. Are uncertainty and confidence marked where needed?
8. Does the path match the current taxonomy and naming rules?
9. Would both a human and an agent find the same file first?

## Quick governance examples
- Stock identification question → canonical home in `vehicle/`
- Maintenance procedure request → canonical home in `work/maintenance/`
- Diagnostic workflow request → canonical home in `diagnostics/`
- Axle swap planning question → procedure in `work/swaps/axles/`, sourcing in `sourcing/interchange/axles/`, baseline facts in `vehicle/systems/axles/`
- Brake upgrade question → procedure in `work/upgrades/brakes/`, not in stock brake reference
- ECU swap wiring question → current canonical home in `swap/wiring/`
- Body/interior repair question → `work/repairs/` or `work/restoration/`, not `vehicle/`
- Repo-building/restructure task → `docs/` and `skillbuilding/`, not content roots
