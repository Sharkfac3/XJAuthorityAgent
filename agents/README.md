# Agents Folder

Agent-facing behavior and routing lives here.

## Canonical policy in this branch
- `index.md` is the canonical router for an agent home.
- `README.md` is a lightweight human-facing mirror that must not add competing routing rules.
- Technical Jeep facts do not live in `agents/`.

## Current structure
- `assistant/` — general Jeep XJ technical assistant routing
- `book/` — book and presentation routing for human-facing deliverables
- legacy helper prompts remain at the top level during transition:
  - `writer.md`
  - `technical.md`
  - `wiring.md`
  - `tuning.md`
  - `reviewer.md`

## Routing rule
Agents should start from `AGENTS.md`, classify the task by question type, then load the owning repo domain:
- `vehicle/` for stock facts
- `work/` for procedures and project execution
- `diagnostics/` for fault isolation
- `sourcing/` for selection decisions
- `swap/` only when the task is specifically current ECU swap execution during migration
- `book/` for presentation guidance
- `docs/` and `skillbuilding/` for governance and repo-building work

## Transitional note
The top-level helper prompts are still in use for book and review workflows. They are compatibility helpers, not canonical technical sources.