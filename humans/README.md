# Human-run Prompt Series

Run these prompts in order.

Goal: finish the post-retooling cleanup so the repo behaves like the broader Jeep XJ knowledge system it was redesigned to become.

These prompts are intentionally sequenced so that:
- each run is context-aware of the retooling already completed
- each run cleans up drift instead of re-opening taxonomy debates
- each run leaves the agent scaffolding in a usable state
- later runs build on earlier cleanup rather than duplicating it

## Required standing context for every prompt
Each prompt tells the agent to treat these as already completed:
- reframe
- taxonomy
- scaffold
- migration planning
- governance
- research-intake system
- retooling review and gap analysis

Each prompt also tells the agent to preserve a usable repo after the run.
That means:
- no half-migrated routers
- no broken entrypoints
- no orphaned scaffolding
- no edits under `.claude/worktrees/`

## Suggested order
1. `01-front-door-identity-and-entrypoint-alignment.md`
2. `02-router-hardening-and-template-cleanup.md`
3. `03-agent-and-book-scaffolding-alignment.md`
4. `04-first-legacy-split-wave.md`
5. `05-high-value-branch-seeding.md`
6. `06-validation-and-scaffolding-readiness-check.md`

## Expected result after the series
After all prompts are run, the repo should have:
- aligned front-door identity
- branch-specific routers instead of generic placeholders
- agent scaffolding that follows the new domain-first routing model
- the worst mixed-purpose legacy files split or clearly bridged
- initial high-value non-swap branch content to prove the broader architecture
- a final readiness check with remaining risks called out explicitly