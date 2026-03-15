# Skill: Repo Gap Audit

Use this skill when the goal is to understand what the repo is still missing.

## Steps
1. Read `AGENTS.md`.
2. Read `docs/repo-taxonomy.md` and `docs/knowledge-expansion.md`.
3. Read `skillbuilding/domain-map.md`, `skillbuilding/gap-taxonomy.md`, `skillbuilding/critical-unknowns.md`, and `skillbuilding/file-maturity.md`.
4. Read `skillbuilding/artifact-contracts.md`.
5. Read `skillbuilding/agents/coverage-auditor.md`.
6. Load only the folders/files needed for the audit scope.
7. Produce a gap report using `skillbuilding/templates/gap-report.md`.

## Suggested audit scopes
- full repo
- one era
- wiring only
- tuning only
- ECU selection only
- beginner-readiness only

## Required classifications
Every gap should be classified as one of:
- missing
- partial
- unclear
- unverified
- misplaced
- conflicting

## Required priorities
- critical
- high
- medium
- low

## Success condition
The output should make it obvious what to build next, how mature the current files are, and where each missing item belongs canonically.
