# XJ Authority Agent

Primary router for this repository.

This project now has **two agent roles only**:
- `agents/expert.md`
- `agents/knowledgebase-builder.md`

## Repo identity
This repo is a Jeep Cherokee XJ knowledgebase.

It is meant to support one expert agent that can answer Jeep questions and write informational documents, and one separate builder agent that expands and hardens the knowledgebase.

## Canonical knowledge roots
- `vehicle/` — stock XJ facts, year differences, subsystem baselines
- `work/` — maintenance, repairs, upgrades, swaps, inspections, setup
- `diagnostics/` — symptom-first troubleshooting and fault isolation
- `sourcing/` — parts, donors, connectors, kits, interchange decisions

## Support roots
- `agents/` — role definitions and routing behavior only
- `humans/` — prompt chain for human-run cleanup and buildout work

## Non-negotiable rules
- Keep Jeep technical truth in the canonical knowledge roots.
- Do not store Jeep facts in `agents/` or `humans/`.
- Do not recreate a separate governance knowledgebase.
- Prefer deep, narrow files over broad summary files.
- Cross-link instead of duplicating facts.
- Treat `work/swaps/ecu/` as the canonical ECU swap execution branch.

## Choose the agent first
### Use the expert agent when the task is:
- answering a Jeep Cherokee question
- comparing stock hardware, upgrades, donors, or swap choices
- explaining maintenance, repair, troubleshooting, or setup work
- writing an informational document from repo facts
- revising or expanding reader-facing technical content

Start with:
- `agents/expert.md`

### Use the knowledgebase-builder agent when the task is:
- restructuring the repo
- removing drift or stale files
- deciding where content should live
- creating or normalizing routers and indexes
- planning or executing knowledgebase expansion
- creating prompt sequences under `humans/`
- auditing gaps, duplication, or stale architecture

Start with:
- `agents/knowledgebase-builder.md`

## Expert routing rules
When operating as the expert agent, classify the question before loading content:

1. Stock fact or factory configuration question → `vehicle/`
2. How-to / maintenance / repair / upgrade / swap / inspection / setup question → `work/`
3. Symptom or fault-isolation question → `diagnostics/`
4. Part / donor / connector / kit choice question → `sourcing/`
5. Current ECU swap execution question → `work/swaps/ecu/`
6. Informational writing request → the owning technical domain

Then narrow by year, era, engine, transmission, drivetrain, ABS, axle family, donor family, or ECU platform when the answer depends on them.

## Builder routing rules
When operating as the knowledgebase-builder agent:
- start with the current repo shape
- keep canonical truth in the knowledge roots
- keep behavioral instructions in `agents/`
- keep human process prompts in `humans/`
- delete or relocate stale meta files that compete with the canonical tree
- create durable paths, not temporary buckets
- optimize for future expert-agent retrieval and writing

## Session guardrail
The canonical repo root is the directory containing this file.
If working inside a nested worktree under `.claude/worktrees/`, edit the repo root copy instead.
Never edit a path containing `.claude/worktrees/`.
