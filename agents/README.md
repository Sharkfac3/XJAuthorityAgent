# Agents Folder

Agent homes, role prompts, and task-specific loading instructions.

## Structure
- `book/` — book and presentation-oriented agent home
- `assistant/` — general technical assistant agent home
- legacy role prompts remain at the top level during migration:
  - `writer.md`
  - `technical.md`
  - `wiring.md`
  - `tuning.md`
  - `reviewer.md`

## Intent
Each agent should expose a stable entrypoint such as `agents/<agent>/index.md` while routing to canonical content under the main repo domains:
- `vehicle/` for stock facts
- `work/` for procedures and project execution
- `diagnostics/` for fault isolation
- `sourcing/` for selection decisions
- `swap/` for current canonical ECU swap execution during migration
- `book/` for presentation rules
- `docs/` and `skillbuilding/` for governance and repo-building work

## Important rule
Agent files route to source content.
They should not become the source of new Jeep XJ facts.
