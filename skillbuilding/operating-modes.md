# Operating Modes

Use this file to define the main modes of repo-building work in `skillbuilding/`.

## Purpose
The project now has multiple agents, skills, and framework files.
Operating modes provide a higher-level map of how those pieces are meant to behave during different kinds of work.

This file is useful for:
- designing new agents
- designing new skills
- deciding which framework files matter most for a task
- preventing workflows from mixing incompatible goals

## Core idea
Most repo-building work falls into a small number of repeatable modes.
A mode is a pattern of:
- goal
- inputs
- outputs
- common failure patterns
- likely next lifecycle transition

## Mode 1 — Discovery mode
Goal:
- identify likely weak areas before a full audit

Typical questions:
- what parts of the domain are likely under-covered?
- what critical unknowns should we inspect first?

Typical inputs:
- `skillbuilding/domain-map.md`
- `skillbuilding/critical-unknowns.md`
- `skillbuilding/gap-taxonomy.md`

Typical outputs:
- likely gap profiles
- candidate backlog items
- audit targets

Common failure patterns:
- treating likely gaps as confirmed
- skipping canonical destination routing
- creating too many vague ideas

Likely next stage:
- suspected → audited

## Mode 2 — Audit mode
Goal:
- inspect actual repo content and confirm, narrow, or dismiss suspected gaps

Typical questions:
- what is actually missing?
- what exists but is weak or misplaced?
- what is mature enough to trust?

Typical inputs:
- `AGENTS.md`
- task-specific canonical files
- `skillbuilding/gap-taxonomy.md`
- `skillbuilding/file-maturity.md`
- `skillbuilding/domain-map.md`

Typical outputs:
- gap report
- critical unknown review
- maturity assessment
- backlog candidates

Common failure patterns:
- vague findings without file paths
- confusing missing content with weak content
- ignoring dependency files

Likely next stage:
- audited → researched
- audited → deferred

## Mode 3 — Research-planning mode
Goal:
- turn a confirmed or likely gap into a practical validation plan

Typical questions:
- what exactly needs to be answered?
- what evidence is required?
- what decisions are blocked until this is known?

Typical inputs:
- `skillbuilding/evidence-standards.md`
- `skillbuilding/source-policy.md`
- `skillbuilding/templates/topic-brief.md`
- target canonical file(s)

Typical outputs:
- topic brief
- evidence plan
- narrowed research questions

Common failure patterns:
- asking broad unfalsifiable questions
- failing to define year/era scope
- not matching evidence strength to risk

Likely next stage:
- researched → normalized

## Mode 4 — Source-intake mode
Goal:
- transform raw material into structured, uncertainty-labeled findings

Typical questions:
- what is directly supported?
- what is inferred?
- what conflicts or caveats must stay visible?

Typical inputs:
- `skillbuilding/source-policy.md`
- `skillbuilding/evidence-standards.md`
- `skillbuilding/templates/source-intake.md`
- destination canonical files if known

Typical outputs:
- validated facts
- open questions
- recommended file placements

Common failure patterns:
- flattening conflicting claims
- losing provenance
- turning weak evidence into settled truth

Likely next stage:
- normalized → drafted

## Mode 5 — Canonical drafting support mode
Goal:
- prepare validated knowledge to be inserted into canonical files cleanly

Typical questions:
- what is the narrowest truthful destination?
- what caveats must survive the edit?
- what related files must be updated too?

Typical inputs:
- normalized findings
- target canonical files
- `docs/repo-taxonomy.md`
- `skillbuilding/file-maturity.md`

Typical outputs:
- edit plan
- destination map
- dependency checklist

Common failure patterns:
- writing too broadly
- hiding year-range scope
- placing swap procedures in vehicle files or vice versa

Likely next stage:
- drafted → hardened

## Mode 6 — Hardening mode
Goal:
- judge whether a file or package is mature enough for normal downstream use

Typical questions:
- is it trustworthy?
- is it complete enough for its intended use?
- what caveats must remain visible?

Typical inputs:
- `skillbuilding/file-maturity.md`
- `skillbuilding/critical-unknowns.md`
- target package files
- audience/writing guidance where relevant

Typical outputs:
- readiness verdict
- blocker list
- caveat list
- follow-up backlog items

Common failure patterns:
- equating technical correctness with readiness
- ignoring audience fit
- allowing missing warnings to slip through

Likely next stage:
- hardened → trusted
- hardened → backlog follow-up

## Mode 7 — Backlog mode
Goal:
- convert findings into an ordered work queue

Typical questions:
- what should be done next?
- what unlocks the most future value?
- what belongs in backlog now vs later?

Typical inputs:
- audit outputs
- research outputs
- hardening outputs
- `skillbuilding/prioritization-rubric.md`
- `skillbuilding/backlog.md`

Typical outputs:
- ranked backlog items
- dependency notes
- maturity targets
- definitions of done

Common failure patterns:
- vague backlog entries
- missing destination paths
- no distinction between confirmed and likely work

Likely next stage:
- any stage → scheduled work

## Mode 8 — Framework self-improvement mode
Goal:
- improve `skillbuilding/` itself when the scaffolding becomes inconsistent, redundant, or weakly connected

Typical questions:
- what framework friction keeps recurring?
- is this a policy, routing, artifact, template, agent, or skill problem?
- what is the lightest fix that improves the system?

Typical inputs:
- `skillbuilding/meta-improvement-loop.md`
- `skillbuilding/agent-design-rules.md`
- `skillbuilding/skill-design-rules.md`
- `skillbuilding/artifact-contracts.md`
- affected framework files

Typical outputs:
- framework problem statement
- recommended fix size
- exact file changes
- integration plan

Common failure patterns:
- adding new files when a small clarification would work
- creating orphan framework docs
- duplicating existing ideas with new names

Likely next stage:
- framework refinement and integration

## How to use operating modes
When designing a new agent or skill, ask:
1. Which operating mode is this mostly serving?
2. What artifact should come out of it?
3. What lifecycle transition should it support?
4. What framework files are essential for that mode?

## Relationship to other files
- use `skillbuilding/agent-design-rules.md` for role design
- use `skillbuilding/skill-design-rules.md` for workflow design
- use `skillbuilding/artifact-contracts.md` to standardize outputs by mode
- use `skillbuilding/work-item-lifecycle.md` for stage transitions
- use `skillbuilding/backlog.md` for turning outputs into active work
- use `skillbuilding/meta-improvement-loop.md` when the mode design itself needs revision
