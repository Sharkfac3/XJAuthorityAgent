# Structure Map

## Purpose
Provide a human-readable map of the next-generation repository scaffold.

## Scope
This document explains where future Jeep XJ content should live during the transition from the ECU-swap-centered layout to the broader platform knowledge architecture.

## What belongs here
- top-level structure summary
- routing-oriented branch descriptions
- transition notes for legacy roots that remain canonical
- quick placement guidance for new content

## What does not belong here
- canonical Jeep technical facts
- full migration checklists for every file
- detailed agent behavior that belongs in `AGENTS.md`
- project backlog management that belongs in `skillbuilding/`

## Child branches
- [`project-reframe.md`](project-reframe.md) — target-state mission and architectural framing
- [`repo-taxonomy.md`](repo-taxonomy.md) — governing placement taxonomy
- [`routing-principles.md`](routing-principles.md) — routing model for agents and maintainers
- [`naming-conventions.md`](naming-conventions.md) — durable naming rules

## Top-level map
```text
agents/         agent behavior and routing only
book/           presentation-layer guidance only
diagnostics/    symptom-first troubleshooting scaffold
sourcing/       parts, donor, connector, and interchange decision scaffold
docs/           governance, taxonomy, migration, and structure docs
skillbuilding/  repo-building workflows and audits
vehicle/        canonical stock XJ fact scaffold plus legacy era content
work/           maintenance, repairs, restoration, upgrades, swaps, inspections, setup
swap/           legacy-but-still-canonical ECU swap branch during migration
humans/         temporary process-artifact prompt archive, not a canonical content root
```

## How to read the scaffold
1. Classify the request by question type first.
2. Enter the owning top-level domain.
3. Use the local `index.md` or `overview.md` to narrow by system, work class, or decision type.
4. Follow child branches to the narrowest truthful file.
5. If a target-state branch is still empty, use the documented transition path to legacy canonical content.

## Major branch intent
### `vehicle/`
Home for stock platform truth. The new scaffold adds `vehicle/years/`, `vehicle/systems/`, `vehicle/packages/`, `vehicle/configurations/`, and `vehicle/interchange-baselines/` while preserving current `vehicle/era1/`, `vehicle/era2/`, `vehicle/era3/`, and `vehicle/trans/` material.

### `work/`
Home for action-oriented content. The scaffold splits jobs first by work class, then by system or project type so maintenance, repairs, upgrades, and swaps do not collapse into one bucket.

### `diagnostics/`
Home for symptom-first troubleshooting. This is separate from stock facts and procedures so fault isolation can grow without polluting reference or work branches.

### `sourcing/`
Home for decision support around parts, donors, connectors, kits, and practical interchange. This keeps buying logic out of stock reference and procedure files.

## Transition notes
- `swap/` remains canonical for current ECU swap execution content.
- Existing `vehicle/era1/`, `vehicle/era2/`, and `vehicle/era3/` files remain canonical until migration into `vehicle/years/` and `vehicle/systems/` is planned.
- This scaffold is intentionally heavy on routers and intentionally light on facts.
- New stubs mark expected child branches without inventing technical details.

## Quick placement guide
- Stock fact about what Jeep used: start in `vehicle/`
- How to perform a job: start in `work/`
- Why something is failing: start in `diagnostics/`
- Which donor, part, or kit to choose: start in `sourcing/`
- How an answer should be written: start in `book/`
- How the repo should evolve: start in `docs/` or `skillbuilding/`
