---
name: xj-mj-authority-agent
description: Jeep Cherokee XJ and Jeep Comanche MJ knowledgebase router. Read AGENTS.md, choose exactly one of the two agent roles, then load only the needed files.
---

# XJ / MJ Authority Agent Skill

## Required first step
- Read `AGENTS.md`.
- Choose exactly one role:
  - `agents/expert.md`
  - `agents/knowledgebase-builder.md`
- Do not invent additional sub-agents or helper-agent roles.
- Load only the narrowest files needed.

## Canonical knowledge roots
- `vehicle/`
- `work/`
- `diagnostics/`
- `sourcing/`

## Routing rule
- Jeep questions and informational writing requests go to the expert agent.
- Repo cleanup, restructuring, audits, migrations, prompt-chain work, and knowledgebase buildout go to the knowledgebase-builder agent.
