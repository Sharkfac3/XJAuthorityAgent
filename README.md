# XJ Authority Agent

Jeep XJ technical knowledge system for agents and humans.

This repository covers the broader XJ platform:
- stock identification, configuration, and subsystem facts
- maintenance, repair, restoration, and setup work
- diagnostics and fault isolation
- upgrades and major swaps
- sourcing, interchange, donor, and connector decisions
- year, trim, package, drivetrain, and subsystem differences

ECU swaps remain an important branch, but they are no longer the repo's defining center. During migration, current ECU swap execution content remains canonical under `swap/`.

## Entry points
- `AGENTS.md` — primary routing file for agents
- `SKILL.md` — root skill entrypoint for pi workflows
- `.pi/skills/xj-swap-book/SKILL.md` — project-local pi discovery wrapper

## Top-level domains
- `vehicle/` — stock Jeep XJ facts and baselines
- `work/` — maintenance, repairs, restoration, upgrades, swaps, inspections, setup
- `diagnostics/` — symptom-first troubleshooting and fault isolation
- `sourcing/` — parts, donor, connector, and interchange decisions
- `swap/` — legacy-but-current ECU swap execution branch during migration
- `book/` — presentation rules and deliverable structure
- `agents/` — behavior and routing only
- `docs/` — governance, taxonomy, and migration notes only
- `skillbuilding/` — repo-building workflows, audits, intake, and hardening
- `humans/` — temporary process-artifact prompt archive from the retooling sequence; not a canonical technical root

## Notes
- Classify the question type before loading content.
- Prefer domain routers and narrow leaf files over broad repo sweeps.
- Keep canonical technical truth in the content tree, not in `agents/`, `docs/`, or `skillbuilding/`.
