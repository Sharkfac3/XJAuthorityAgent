# Post-Cleanup Validation

## Status
Validated after the front-door cleanup, router hardening, agent scaffolding alignment, first legacy split wave, and first branch seeding.

**Readiness verdict:** ready for ordinary repo use, with bounded follow-up backlog items.

The live repo now orients a new agent from the active entrypoints rather than requiring hidden migration history. Repo identity, branch routers, and agent scaffolding now broadly agree that this is a **Jeep XJ technical knowledge system** with `swap/` retained as the **legacy-but-current ECU swap execution branch during migration**.

## What was validated

### 1. New-agent orientation is now workable from live files
Confirmed path chain:
- `SKILL.md`
- `AGENTS.md`
- top-level `README.md`
- domain routers under `vehicle/`, `work/`, `diagnostics/`, `sourcing/`, and `swap/`
- agent homes under `agents/assistant/` and `agents/book/`

These files now agree on:
- question-type-first routing
- domain ownership by `vehicle/`, `work/`, `diagnostics/`, `sourcing/`, and `book/`
- `swap/` as a scoped migration branch rather than whole-repo identity

### 2. Front-door identity is aligned enough for ordinary use
Confirmed aligned front doors:
- `README.md`
- `AGENTS.md`
- `agents/assistant/index.md`
- `agents/book/index.md`
- `book/outline.md`
- `vehicle/README.md`
- `swap/README.md`
- `swap/index.md`

These no longer present the repo as swap-only.

### 3. `swap/` is visibly transitional in live navigation
Confirmed bridges:
- `work/index.md` points ECU swap users toward `work/swaps/ecu/` as the target-state branch
- `work/swaps/ecu/index.md` sends live execution work into `swap/`
- `swap/index.md` explicitly scopes itself to current ECU swap execution during migration

### 4. Template-router drift is reduced, not eliminated
Representative routers now contain branch-true guidance instead of generic placeholders:
- `work/maintenance/cooling/index.md`
- `work/maintenance/charging-starting/index.md`
- `diagnostics/cooling/index.md`
- `diagnostics/charging-and-starting/index.md`
- `diagnostics/brakes/index.md`
- `sourcing/connectors/index.md`

### 5. Broader XJ usefulness is now demonstrated in live content
The repo is no longer proving itself only through ECU content.
Visible seed branches now include:
- `vehicle/systems/cooling/overview.md`
- `vehicle/systems/brakes/overview.md`
- `vehicle/systems/charging-starting/overview.md`
- `vehicle/systems/fuel/overview.md`
- `work/maintenance/cooling/cooling-system-refresh/`
- `work/maintenance/charging-starting/cable-and-ground-service/`
- `diagnostics/cooling/overheating-at-idle.md`
- `diagnostics/charging-and-starting/low-charging-voltage.md`
- `diagnostics/fuel/no-prime.md`
- `sourcing/connectors/pigtail-vs-rehousing.md`
- `sourcing/interchange/axles/`
- `sourcing/interchange/brakes/`

## Small corrective edits made in this validation pass
- Updated `humans/README.md` to explicitly mark `humans/` as a **temporary process-artifact prompt archive** rather than a canonical technical domain.
- Added this file as the final status note and operational validation record.

## Current operating conventions
- `AGENTS.md` remains the primary live routing contract.
- `index.md` is the canonical router inside branch homes.
- `README.md` files are lightweight mirrors and must not carry competing routing rules.
- `swap/` remains valid for live ECU execution work, but should not be used as the default entrypoint for non-swap topics.
- `humans/` is temporary process-artifact storage only; do not expand it into a durable content root.

## Confirmed remaining weaknesses

### Bounded, non-emergency issues
1. **Mixed-purpose legacy files still remain in active use**
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

2. **Many branch routers are still scaffold-light rather than content-rich**
   The routing surface is now coherent, but many branches still advertise expected child packages more than they deliver finished leaves.

3. **`work/swaps/ecu/` is a bridge, not yet the live execution home**
   This is acceptable for now because the bridge is explicit, but migration is not complete.

4. **`book/outline.md` is correctly scoped, but root `book/` still has only one visible project deliverable**
   This is no longer an identity problem; it is a future breadth question.

## Bottom line
The repo no longer appears trapped in retooling drift.
A new agent can orient from the live repo, classify the task, and reach the correct domain without relying on undocumented project history.

Remaining issues are now explicit and suitable for normal backlog handling rather than emergency cleanup.
