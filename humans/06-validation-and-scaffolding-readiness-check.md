You are working inside the XJ Authority Agent repository.

Assume the reframe, taxonomy, scaffold, migration plan, governance, research-intake system, retooling audit, front-door identity cleanup, router hardening, agent scaffolding alignment, first legacy split wave, and first high-value branch seeding have already been completed.

## Mission
Run a final post-cleanup validation pass that checks whether the repo is now easier for agents to navigate, safer to scale, and ready for ordinary use without tripping over retooling drift.

## Context you must respect
- This is a validation-and-polish pass, not a fresh redesign.
- Prefer small corrective edits over new structural churn.
- Leave the repo in a usable state after this run.
- Never edit any path containing `.claude/worktrees/`.

## Required reading order
1. `SKILL.md`
2. `AGENTS.md`
3. `docs/retooling-review.md`
4. `docs/retooling-gap-report.md`
5. `docs/next-actions.md`
6. inspect the updated `agents/`, `book/`, `vehicle/`, `work/`, `diagnostics/`, `sourcing/`, and `swap/` routers
7. read only the canonical leaves needed to verify any remaining weak spots

## Validation questions you must answer
- Can a new agent orient itself quickly from the live repo, not just the governance docs?
- Do front-door files, branch routers, and agent scaffolding now agree about repo identity?
- Is `swap/` clearly transitional in live navigation?
- Are the most obvious template-router and mixed-purpose-file problems now reduced?
- Do the first seeded branches prove broader Jeep XJ usefulness?
- What confirmed weaknesses still remain?

## Your job
1. Audit the live navigation surface.
2. Make any small corrective edits needed to remove last-mile drift.
3. Update or create final validation artifacts if the current docs now need a refreshed status note.

## Suggested deliverables
At minimum, produce or refresh:
- a short status note under `docs/` if needed
- any final router or entrypoint fixes required for readiness

If the earlier audit files remain accurate, do not rewrite them wholesale. Add only what is needed to reflect the new state.

## Constraints
- Be critical, but do not reopen settled architecture questions.
- Distinguish confirmed remaining issues from future risks.
- Prefer path-specific findings over broad impressions.

## Definition of done
- The live repo is coherent enough that a new agent can use it without relying on hidden project history.
- The agent scaffolding is ready to use after this run.
- Remaining issues are explicit, bounded, and suitable for normal backlog handling rather than emergency cleanup.
- Summarize what you validated, what you corrected, and what still remains open.