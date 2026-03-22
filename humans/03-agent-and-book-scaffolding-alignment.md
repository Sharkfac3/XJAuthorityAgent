You are working inside the XJ Authority Agent repository.

Assume the reframe, taxonomy, scaffold, migration plan, governance, research-intake system, retooling audit, front-door identity cleanup, and router hardening have already been completed.

## Mission
Bring agent-facing scaffolding into alignment with the new domain-first repo model while keeping the agents usable after the run.

## Context you must respect
- `AGENTS.md` is the primary repo entrypoint and should stay authoritative.
- `agents/` is for behavior and routing only.
- `book/` is for presentation guidance only.
- ECU swap work remains important, but it is no longer the default routing assumption for all tasks.
- Leave the repo in a usable state after this run.
- Never edit any path containing `.claude/worktrees/`.

## Required reading order
1. `SKILL.md`
2. `AGENTS.md`
3. `docs/retooling-review.md`
4. `docs/retooling-gap-report.md`
5. `docs/next-actions.md`
6. `docs/agent-orientation.md`
7. `docs/content-governance.md`
8. `docs/migration-plan.md`
9. inspect the current files under `agents/` and the key files under `book/`

## Primary files to inspect and likely edit
- `agents/README.md`
- `agents/assistant/index.md`
- `agents/book/index.md`
- `agents/assistant/README.md`
- `agents/book/README.md`
- `book/outline.md`
- any helper prompt file whose instructions now clearly contradict the retooling

## Your job
Make agent scaffolding reflect the current repo architecture.

Specifically:
- remove swap-first assumptions from assistant routing
- make question-type classification come before branch loading
- keep ECU swap execution routing available and explicit when relevant
- make Book-agent loading rules aware of the broader repo, even if the current deliverable focus remains ECU-swap-heavy
- reduce or document any README/index duplication inside `agents/`
- keep helper prompts usable if they are still intentionally transitional

## Constraints
- Do not move technical facts into `agents/`.
- Do not break existing helper-prompt references without replacing them cleanly.
- Do not broaden the Book agent into a vague generic writer; keep it path-specific and repo-aware.
- If you make a policy choice about `README.md` vs `index.md` inside `agents/`, apply it consistently at least within this branch.

## Deliverables
- aligned `agents/` scaffolding
- any necessary book-layer routing cleanup that directly affects agent usability
- a concise note on remaining transitional helper-prompt patterns still in use

## Definition of done
- A new agent following `agents/assistant/index.md` no longer behaves as if every task is an ECU swap task.
- The Book agent can operate inside the broader repo without losing its current project utility.
- The `agents/` scaffolding is ready to use immediately after this run.
- Summarize what changed, what remains transitional, and what should be handled in a later migration wave.