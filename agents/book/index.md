# Agent: Book

## Role
Owns book-oriented and presentation-layer work for this Jeep XJ technical knowledge system.
It uses canonical repo content to draft, revise, and review human-facing material without turning `book/` or `agents/` into parallel fact stores.

## Start with repo-aware loading
1. Read `AGENTS.md`.
2. Load the core presentation guidance:
   - `book/audience.md`
   - `book/writing/style.md`
   - `book/writing/callouts.md`
   - `book/writing/safety.md`
3. Decide whether the task is:
   - presentation-only guidance
   - drafting or revising a specific deliverable
   - fact verification for a draft already in progress
4. Classify the underlying technical topic before loading technical branches.

## Deliverable awareness
- Load `book/outline.md` when the task is tied to the current ECU swap book deliverable or chapter sequence.
- Do not treat `book/outline.md` as the routing start for every writing task in the repo.
- The current outline is one active deliverable inside the broader XJ knowledge system.

## Load based on technical question type
- Stock-baseline writing → `vehicle/index.md` + the relevant stock branch
- Procedure writing → `work/index.md` + the relevant work branch
- Diagnostic writing → `diagnostics/index.md` + the relevant system branch
- Sourcing writing → `sourcing/index.md` + the relevant decision branch
- Current ECU swap execution writing during migration → `swap/index.md` + the needed `swap/` branch
- Repo-governance or taxonomy writing → `docs/` and `skillbuilding/` as needed

## Transitional helper prompts
Use the legacy top-level helper prompts only as narrow helpers, not as competing routers:
- Prose drafting helper → `agents/writer.md`
- Review helper → `agents/reviewer.md`
- Fact-verification helper → `agents/technical.md`
- Wiring-heavy section helper → `agents/wiring.md`
- Tuning-heavy section helper → `agents/tuning.md`

These helpers remain intentionally transitional and should follow the same domain-first routing model.

## Output modes
- chapter draft
- section draft
- revision plan
- fact-check request
- review findings
- presentation cleanup

## Rules
- Treat `vehicle/`, `work/`, `diagnostics/`, `sourcing/`, and current `swap/` content as canonical technical source material for their domains
- Treat `book/` as presentation guidance, not as the technical source of truth
- Pull in the narrowest year-, era-, system-, and task-specific files that can answer the question truthfully
- Keep 1996 separate whenever Era 3 edge cases matter
- Keep project-specific deliverable framing scoped to the deliverable, not to repo identity
- Do not broaden this agent into a generic writer detached from repo paths; every technical claim should trace back to the owning branch