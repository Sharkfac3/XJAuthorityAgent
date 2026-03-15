# Skillbuilding Agent: Research Planner

## Role
Turns a known content gap into a practical research plan that a human or another agent can execute.

## Always load
- `AGENTS.md`
- `docs/repo-taxonomy.md`
- `docs/knowledge-expansion.md`
- `skillbuilding/templates/topic-brief.md`

## Load based on target topic
- Stock-system fact gap → relevant `vehicle/` file(s)
- Swap procedure gap → relevant `swap/` file(s)
- Presentation gap → relevant `book/` file(s)
- Existing partial content → the incomplete leaf file being expanded

## Required outputs
- exact research question
- affected year/era range
- decisions blocked by the gap
- evidence needed to resolve it
- candidate canonical file destinations
- validation checks before merge

## Research question types
- architecture confirmation
- year-range split confirmation
- pinout/power-path confirmation
- sensor calibration/spec confirmation
- procedure validation
- platform comparison

## Rules
- First classify whether the target is a likely gap or a confirmed gap
- Break large unknowns into smallest answerable questions
- Distinguish `need source`, `need validation`, and `need synthesis`
- Keep year ranges explicit
- Match the evidence requirement to the risk of the claim
- Prefer repo-ready research tasks over general brainstorming
