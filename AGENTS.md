# XJ ECU Swap Book

Cross-agent routing index for this repo.

## Start here
- Use this file as the primary entrypoint.
- Load only the files needed for the current task.
- Prefer canonical content under `agents/`, `vehicle/`, `swap/`, and `book/`.
- Use `skillbuilding/` only for repo-building workflows, audits, and expansion planning.
- Ignore deleted or archived redirect stubs.

## Session context — file editing
- The canonical repo root is the directory containing this file.
- Claude Code sessions may run inside a git worktree nested under `.claude/worktrees/`.
- Always edit files at the repo root (e.g. `vehicle/era2/trigger.md`), never the worktree copy under `.claude/worktrees/`.
- If you are unsure which copy you are editing, check that the file path does NOT contain `.claude/worktrees/`.

## Repo map
- `agents/` — role prompts
- `vehicle/` — Jeep/XJ facts by era, engine, transmission
- `swap/` — ECU choice, wiring, connectors, tuning
- `book/` — audience, outline, writing standards
- `docs/` — taxonomy and audit notes for repo maintenance
- `skillbuilding/` — meta-framework for audits, backlog building, research planning, and repo hardening
- `.pi/skills/xj-swap-book/` — pi-only wrapper, not source content
- `.pi/skills/skillbuilding-framework/` — pi-only wrapper for repo-building workflows

## Load by task
- Swap workflow routing: `swap/index.md`
- Writing: `book/audience.md` + `book/writing/style.md` + `book/writing/callouts.md`
- Safety copy: `book/writing/safety.md`
- Outline work: `book/outline.md`
- Era 1 / Renix: `vehicle/era1/overview.md` + needed leaf file
- Era 2 / OBD-I: `vehicle/era2/overview.md` + needed leaf file
- Era 3 / OBD-II: `vehicle/era3/overview.md` + needed leaf file
- 1996 specifics: `vehicle/era3/1996-notes.md`
- Engine baseline: `vehicle/engine.md`
- AW4 auto: `vehicle/trans/aw4.md`
- Manual trans: `vehicle/trans/manual.md`
- ECU selection: `swap/ecu-selection/requirements.md` + platform file
- Wiring: `swap/wiring/grounds.md` + `swap/wiring/harness.md` + era wiring file
- Connectors: `swap/wiring/connectors/index.md`
- Tuning: `swap/tuning/<topic>.md`
- Role behavior: `agents/<role>.md`
- Repo-building/meta tasks: `skillbuilding/index.md`

## Era quick reference
- Era 1: 1988–1990, Renix
- Era 2: 1991–1995, Chrysler SBEC
- Era 3: 1996–2001, Chrysler JTEC

Use eras as the compatibility lens for the swap, not as the main goal of the repo.

## Token discipline
- Do not load multiple era overviews unless the task compares eras.
- Do not load every tuning or ECU file up front.
- Treat `AGENTS.md` as the router and leaf docs as the facts.
- Use `vehicle/` for technical truth, `swap/` for procedures, `book/` for presentation, `agents/` for role behavior.
- Load `docs/repo-taxonomy.md` or `docs/content-audit.md` only when restructuring or auditing the repo.
