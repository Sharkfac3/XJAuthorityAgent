# XJ / MJ Authority Agent

This repository is a Jeep Cherokee XJ and Jeep Comanche MJ knowledgebase with exactly two agent roles:

- `agents/expert.md` — the foremost expert on both platforms; answers questions and writes informational documents from the knowledgebase
- `agents/knowledgebase-builder.md` — the builder that restructures, cleans up, expands, audits, and hardens the knowledgebase across both vehicles

## Fast start
1. Read `AGENTS.md`.
2. Choose exactly one role.
3. Load that role file from `agents/`.
4. Load only the narrowest knowledge files needed.

If the task is a Jeep question or an informational writing request, use the expert agent.
If the task is repo cleanup, routing, migration, prompt-chain work, or knowledgebase buildout, use the knowledgebase-builder agent.

## Canonical knowledge roots
- `vehicle/` — stock XJ and MJ facts, baselines, and per-platform variations
- `work/` — maintenance, repairs, upgrades, swaps, inspections, setup
- `diagnostics/` — troubleshooting and fault isolation
- `sourcing/` — donor, parts, connector, and kit decisions

## Support roots
- `agents/` — role behavior and routing only
- `humans/` — human-run prompt chain for cleanup, restructuring, and buildout work

## Rules
- Keep Jeep technical truth in the canonical knowledge roots.
- Keep agent behavior in `agents/` only.
- Keep human process prompts in `humans/` only.
- Do not rebuild a separate governance knowledgebase.
- Do not create additional agent roles in this repo.
- Prefer narrow, reusable Markdown files over broad catch-all summaries.
- Distinguish XJ-specific and MJ-specific content clearly where the platforms diverge.
