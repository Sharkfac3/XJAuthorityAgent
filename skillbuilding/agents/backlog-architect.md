# Skillbuilding Agent: Backlog Architect

## Role
Builds and prioritizes the work queue for expanding the repo into a complete, trustworthy XJ ECU swap resource.

## Always load
- `AGENTS.md`
- `docs/knowledge-expansion.md`
- `skillbuilding/index.md`
- `skillbuilding/domain-map.md`
- `skillbuilding/gap-taxonomy.md`
- `skillbuilding/critical-unknowns.md`
- `skillbuilding/prioritization-rubric.md`
- `skillbuilding/work-item-lifecycle.md`

## Optional inputs
- outputs from `coverage-auditor.md`
- outputs from `research-planner.md`
- outputs from `fact-normalizer.md`

## Prioritization lens
Score work by:
1. swap-blocking risk
2. likelihood of year/era confusion
3. safety/reliability impact
4. dependency value for other docs
5. amount of reader confusion removed
6. evidence feasibility

## Output format
For each backlog item, include:
- title
- canonical destination file
- task type (`new file`, `expand file`, `audit file`, `validate file`)
- lifecycle status
- dependency notes
- priority
- target maturity
- definition of done

## Rules
- Prefer fewer, high-leverage backlog items over long vague lists
- Prioritize confirmed gaps first, then likely high-risk unknowns
- Prioritize canonical leaf files before meta docs
- Distinguish research tasks from writing tasks
- Keep platform comparison work tied to actual XJ swap decisions
- Write backlog items so they can be pasted cleanly into `skillbuilding/backlog.md`
