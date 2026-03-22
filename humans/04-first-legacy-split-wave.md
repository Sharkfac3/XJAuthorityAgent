You are working inside the XJ Authority Agent repository.

Assume the reframe, taxonomy, scaffold, migration plan, governance, research-intake system, retooling audit, front-door identity cleanup, router hardening, and agent scaffolding alignment have already been completed.

## Mission
Execute the first high-value split wave on mixed-purpose legacy content so the new taxonomy starts becoming true in live canonical files, not only in governance docs.

## Context you must respect
- This is a split-and-bridge pass, not a full-content rewrite.
- Preserve canonical truth.
- Use redirects, transition notes, and cross-links where needed.
- Prefer a few high-value splits done cleanly over many shallow edits.
- Leave the repo in a usable state after this run.
- Never edit any path containing `.claude/worktrees/`.

## Required reading order
1. `SKILL.md`
2. `AGENTS.md`
3. `docs/retooling-review.md`
4. `docs/retooling-gap-report.md`
5. `docs/next-actions.md`
6. `docs/migration-map.md`
7. `docs/migration-plan.md`
8. `docs/content-governance.md`
9. `docs/file-creation-rules.md`
10. read only the canonical files you plan to split

## Priority candidates
Choose a small, high-value set from this list:
- `vehicle/trans/aw4.md`
- `vehicle/trans/manual.md`
- `vehicle/engine.md`
- `vehicle/era1/diagnostics.md`
- `vehicle/era2/diagnostics.md`
- `vehicle/era3/diagnostics.md`
- `vehicle/era1/wiring.md`
- `vehicle/era2/wiring.md`
- `vehicle/era3/wiring.md`
- `swap/wiring/connectors/index.md` and the connector family branch structure

## Your job
For the files you choose:
- separate stock facts from procedures, diagnostics, or sourcing where the split is already clear
- create the narrowest truthful destination files
- leave compatibility notes or short transition pointers in legacy paths when needed
- avoid silently deleting valuable context
- improve routing clarity more than raw content volume

## Strong recommendations
- treat `vehicle/trans/aw4.md` as one of the best first split targets
- treat at least one era `diagnostics.md` file as a prototype split for diagnostics vs inspection flow
- if you touch connector content, move only the clearly sourcing-shaped material and leave procedure-specific notes where they still belong

## Constraints
- Do not attempt the entire migration in one pass.
- Do not create unresolved parallel canon.
- Do not move content if the destination branch is still too vague to own it cleanly.
- Keep year/era nuance intact.

## Deliverables
- a small set of completed split migrations
- any bridge or compatibility notes needed to preserve usability
- a short report in your final response listing:
  - source paths touched
  - new canonical destinations created or strengthened
  - what was intentionally left for later

## Definition of done
- At least one or two of the worst mixed-purpose legacy files are cleaner than before.
- The new taxonomy gains real live canonical support.
- The repo remains navigable and usable immediately after this run.
- Summarize remaining blockers for the next split wave.