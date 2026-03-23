# Agents

This repo has exactly two agent definitions:

- `expert.md` — answers Jeep Cherokee questions and writes informational documents from repo facts
- `knowledgebase-builder.md` — cleans up, restructures, audits, and expands the knowledgebase itself

`agents/` stores role behavior and routing only.
It must not become a technical fact store.
Do not add helper agents, specialist sub-agents, or alternate routers here.
