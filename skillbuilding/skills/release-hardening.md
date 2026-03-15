# Skill: Release Hardening

Use this skill when deciding whether a section is mature enough to treat as trusted guidance.

## Steps
1. Read `AGENTS.md`.
2. Read `skillbuilding/file-maturity.md`.
3. Read `skillbuilding/agents/release-hardener.md`.
4. Read the target files and only their necessary dependencies.
5. Evaluate the package for accuracy, completeness, clarity, and visible caveats.
6. Return a readiness verdict and a short blocker list.

## Readiness definitions
- `not ready` — too incomplete, too ambiguous, or too risky to trust
- `usable with caveats` — mostly helpful but caveats must stay visible
- `ready` — mature enough for normal downstream use

## Blocker examples
- year range is unclear
- critical connector details are missing
- tuning guidance lacks safety context
- 1996 caveat is absent where required
- output depends on unstated assumptions
