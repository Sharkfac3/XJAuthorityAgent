# Book Folder

## Purpose
Route informational writing and presentation rules for reader-facing output.

Use `book/` when the task is to draft, revise, or structure a document.
Always load `book/` **with** the owning technical branch; do not treat `book/` as the source of Jeep facts.

## First-hop loading path for writing
- Audience guidance → [`audience.md`](audience.md)
- Writing style → [`writing/style.md`](writing/style.md)
- Callouts and formatting conventions → [`writing/callouts.md`](writing/callouts.md)
- Safety language → [`writing/safety.md`](writing/safety.md)
- Deliverable structure only when needed → [`outline.md`](outline.md)

## Technical source pairings
- Stock facts writing → [`../vehicle/index.md`](../vehicle/index.md)
- Procedures and job execution writing → [`../work/index.md`](../work/index.md)
- Diagnostics writing → [`../diagnostics/index.md`](../diagnostics/index.md)
- Sourcing writing → [`../sourcing/index.md`](../sourcing/index.md)
- ECU swap execution writing → [`../work/swaps/ecu/index.md`](../work/swaps/ecu/index.md)

## Important rule
Do not treat `book/` as canonical technical source material.
Use `vehicle/`, `work/`, `diagnostics/`, `sourcing/`, and `work/swaps/ecu/` for technical truth in their respective domains.

## Scope note
The current `book/outline.md` is an ECU swap deliverable inside the broader Jeep XJ knowledgebase.
It does not define the repo’s overall mission.
