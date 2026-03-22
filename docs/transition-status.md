# Transition Status

## Purpose
Record the current live conventions that are already settled enough to use during ordinary repo work.

Use this file when you need a short operational answer to "what is locked right now?" without re-reading the full migration stack.

## Status summary
The broader Jeep XJ architecture is live.
The repo is usable for ordinary agent work.
Migration is still in progress, but several navigation and governance decisions are now locked enough to treat as current convention.

## Locked current conventions

### 1. Repo identity
The repo is a **Jeep XJ technical knowledge system**.
It is not a swap-only repo.

Primary live entrypoints that should agree with this:
- `README.md`
- `SKILL.md`
- `AGENTS.md`
- domain `index.md` files

### 2. Domain ownership
Use these current top-level roots as the live routing model:
- `vehicle/` — stock Jeep XJ facts
- `work/` — procedures and project execution
- `diagnostics/` — symptom-first fault isolation
- `sourcing/` — donor, part, connector, and interchange decisions
- `swap/` — current ECU swap execution branch during migration
- `book/` — presentation guidance
- `agents/` — behavior and routing only
- `docs/` — governance and migration rules only
- `skillbuilding/` — repo-building workflows only

### 3. `swap/` status
`swap/` remains canonical for live ECU swap execution work.
It is **not** the repo center and should not be the default starting point for non-ECU questions.

Preferred live bridge:
- target-state routing starts in `work/swaps/ecu/`
- live execution still resolves into `swap/`

### 4. README vs `index.md`
Current operating policy:
- `index.md` is the canonical router inside a branch
- `README.md` is optional and lightweight
- `README.md` must not carry competing routing rules

### 5. `humans/` status
`humans/` is a **temporary process-artifact prompt archive** from the retooling sequence.
It is not a canonical technical content root and should not receive new Jeep facts or long-term routing logic.

## Still transitional but actively valid

### Legacy canonical branches still in use
- `vehicle/era1/`
- `vehicle/era2/`
- `vehicle/era3/`
- `vehicle/trans/`
- `vehicle/engine.md`
- current ECU swap execution content under `swap/`

These remain valid until a deliberate split or migration replaces them.
Do not force-move them ad hoc.

## Open decisions still pending
These are real backlog items, not live-routing blockers.

### 1. First mixed-purpose split wave
Highest-value remaining split targets:
- `vehicle/engine.md`
- `vehicle/trans/aw4.md`
- `vehicle/trans/manual.md`
- `vehicle/era1/diagnostics.md`
- `vehicle/era2/diagnostics.md`
- `vehicle/era3/diagnostics.md`
- `vehicle/era1/wiring.md`
- `vehicle/era2/wiring.md`
- `vehicle/era3/wiring.md`
- `swap/wiring/connectors/index.md`

### 2. Final long-term home for shared helper prompts
Current helper prompts remain under `agents/` during transition.
Their long-term placement and packaging are still open.

### 3. Final long-term book deliverable layout
`book/outline.md` is the current active deliverable.
Broader conventions for multiple human-facing deliverables remain open.

### 4. Final year-specific file convention under `vehicle/years/`
Especially unresolved:
- `vehicle/years/1996-notes.md`
- `vehicle/years/era3/1996-notes.md`

### 5. Final scope boundary for ECU-specific setup and calibration
Some content will likely remain ECU-swap-specific.
Some may eventually generalize under `work/setup-and-calibration/`.
That split is not finished yet.

## Use rule
If a task needs a current operational convention, follow this file.
If a task needs architectural reasoning or migration planning, go back to:
- `docs/project-reframe.md`
- `docs/repo-taxonomy.md`
- `docs/routing-principles.md`
- `docs/content-governance.md`
- `docs/file-creation-rules.md`
