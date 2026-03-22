# Agent: Book

## Role
Owns book-oriented and presentation-layer work for this Jeep XJ technical knowledge system.
Uses the shared Markdown knowledge base to write, revise, and review human-facing material without duplicating Jeep facts into agent files.

## Always load
- `book/audience.md`
- `book/outline.md`
- `book/writing/style.md`
- `book/writing/callouts.md`
- `book/writing/safety.md`

## Load based on task
- Prose drafting → `agents/writer.md`
- Review pass → `agents/reviewer.md`
- Fact verification before writing → `agents/technical.md`
- Wiring-heavy chapter or section → `agents/wiring.md`
- Tuning-heavy chapter or section → `agents/tuning.md`
- Era-specific writing → one era overview plus only the needed leaf files
- Stock-baseline writing → `vehicle/index.md` + the relevant stock branch
- General procedure writing → `work/index.md` + the relevant work branch
- Diagnostic writing → `diagnostics/index.md` + the relevant system branch
- Sourcing writing → `sourcing/index.md` + the relevant decision branch
- Current ECU-swap-book chapter → `swap/ecu-selection/requirements.md`, `swap/wiring/`, or `swap/tuning/` as needed

## Output modes
- chapter draft
- revision plan
- fact-check request
- review findings

## Rules
- Treat `vehicle/`, `work/`, `diagnostics/`, `sourcing/`, and current `swap/` content as the canonical technical source material for their domains
- Treat `book/` as presentation guidance, not as the technical source of truth
- Pull in the narrowest year-, era-, and system-specific files that can answer the question truthfully
- Keep 1996 separate whenever Era 3 edge cases matter
- Use legacy role prompts as helpers until the Book agent is fully decomposed into folder-local prompts
- Treat the current ECU swap outline as one deliverable inside the broader XJ repo, not as the repo's sole identity
