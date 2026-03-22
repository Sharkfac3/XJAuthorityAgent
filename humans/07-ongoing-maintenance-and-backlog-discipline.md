You are working inside the XJ Authority Agent repository.

Assume the reframe, taxonomy, scaffold, migration plan, governance, research-intake system, retooling cleanup, router hardening, agent scaffolding alignment, legacy split wave, branch seeding, and validation pass have already been completed.

## Mission
Run a recurring maintenance pass that prevents structural drift, keeps agent scaffolding aligned with the live repo, and converts new gaps or ambiguities into disciplined next work instead of ad hoc repo growth.

## Why this prompt exists
This prompt is for the long-term health of the project.
Use it periodically after normal repo growth to keep the knowledge system scalable, navigable, and faithful to the adopted architecture.

## Context you must respect
- The broader Jeep XJ architecture is already adopted.
- This is not a redesign prompt.
- Prefer small corrective edits, targeted cleanup, and backlog-ready follow-up over broad churn.
- Leave the repo in a usable state after this run.
- Never edit any path containing `.claude/worktrees/`.

## Required reading order
1. `SKILL.md`
2. `AGENTS.md`
3. `docs/project-reframe.md`
4. `docs/repo-taxonomy.md`
5. `docs/routing-principles.md`
6. `docs/content-governance.md`
7. `docs/file-creation-rules.md`
8. `docs/next-actions.md`
9. `docs/retooling-review.md`
10. `docs/retooling-gap-report.md`
11. inspect the current live repo structure and only the files needed to verify drift or weak spots

## Recurring audit questions
- Do the root and branch entrypoints still agree about what this repo is?
- Do `AGENTS.md`, `agents/`, and local routers still point to the same canonical destinations?
- Has new content been placed in the correct domain?
- Have any new mixed-purpose files appeared?
- Are README files, `index.md` files, and local overviews still aligned?
- Is `swap/` staying transitional rather than reclaiming the center of the repo?
- Have any generic placeholder or copied router patterns reappeared?
- Which stubs are now mature enough to harden into real branch packages?
- Which transitional bridge files are ready to be retired or reduced?

## Your job
1. Inspect the current repo for fresh drift, stale transitional patterns, and navigation regressions.
2. Make small corrective edits where the fix is clear and low-risk.
3. Identify anything that should become a backlog item, hardening task, or next migration step instead of being improvised immediately.
4. Keep the agent scaffolding ready to use after the run.

## Things to fix directly when found
Fix directly when the change is small, clear, and low-risk, such as:
- inconsistent wording in entrypoints or routers
- obvious README/index divergence
- newly introduced generic placeholder router text
- minor path-specific drift in `agents/` or `book/` routing
- stale transition wording after a destination branch is already established

## Things to convert into disciplined next work instead of solving ad hoc
Do not improvise large work when you find:
- major mixed-purpose files that need a real split plan
- broad new topic families that need intake and placement work
- evidence-sensitive technical expansions
- cross-domain changes that need migration planning
- larger branch packages that should be seeded and hardened deliberately

For those, create or update the appropriate planning artifact under `docs/` or `skillbuilding/` as needed.

## Recommended outputs
Depending on what you find, produce some combination of:
- small direct repo fixes
- a refreshed status note under `docs/`
- updates to `docs/next-actions.md` if priorities have changed materially
- a narrow gap or hardening note if a branch has become the next best target

## Constraints
- Be path-specific.
- Distinguish confirmed current drift from future risks.
- Prefer preserving repo clarity over maximizing changes in one run.
- Do not let maintenance work turn into another broad retooling project.

## Definition of done
- The repo is at least as coherent after the pass as before it.
- Agent scaffolding still works cleanly from live entrypoints.
- New drift is either corrected or converted into explicit next work.
- Remaining open items are bounded and deliberate, not hidden structural decay.

## Final response requirements
Summarize:
- what drift you checked for
- what you fixed directly
- what you intentionally left for backlog or later migration
- whether the repo remains ready for ordinary agent use after the pass