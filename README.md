# XJ ECU Swap Book

Knowledge-base repo for AI coding/writing agents building a Jeep XJ open-source ECU swap book.

## Goals
- Keep the repo centered on what is required to install an open-source ECU in a 1988–2001 Jeep XJ
- Preserve era-specific and year-specific differences that materially affect the swap
- Keep canonical facts in a small number of predictable folders
- Minimize default context/token usage
- Work cleanly with both pi and AGENTS.md-based coding agents

## Entry points
- `AGENTS.md` — primary cross-agent routing file for AGENTS-aware tools such as OpenCode-style agents
- `SKILL.md` — root skill file for pi-oriented workflows
- `.pi/skills/xj-swap-book/SKILL.md` — project-local pi discovery wrapper

## Canonical folders
- `agents/`
- `vehicle/` — stock Jeep/XJ facts and era-specific hardware context
- `swap/` — primary workflow for making the aftermarket ECU work in the Jeep
- `book/`
- `docs/` for repo-governance notes only

## Notes
- Root-level redirect stubs were removed to avoid ambiguity.
- Agents should load the router first, then only the leaf files required for the task.
