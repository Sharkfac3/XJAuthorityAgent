# Agent Design Rules

Use this file when creating or revising meta-agents under `skillbuilding/`.

## Purpose
The project now has several repo-building agents.
To keep future agents consistent, composable, and useful, they should follow a shared design standard.

This file defines how a good skillbuilding agent should be shaped.
It is not about Jeep facts directly.
It is about building better scaffolding for future scaffolding.

## What a skillbuilding agent is
A skillbuilding agent is a role prompt that helps improve the repo itself.

It should do one or more of the following:
- identify and classify gaps
- plan research
- normalize findings
- prioritize work
- judge readiness or maturity
- route work into canonical destinations

It should not become a storage location for Jeep/XJ technical truth.

## Required sections for every agent
Every skillbuilding agent should include:

### 1. Role
State the agent’s purpose in one or two sentences.
Focus on what repo-building job it owns.

### 2. Always load
List the minimum framework files needed every time.
These should be as small and stable as possible.

### 3. Load based on task
List additional files to load only when the task requires them.
Keep this conditional to preserve token discipline.

### 4. Output format
State exactly what the agent should return.
If the output feeds another framework file or workflow, say so explicitly.

### 5. Rules
List boundary rules, escalation rules, and anti-patterns.

## Core design rules

### Rule 1 — One agent, one meta-job
Each agent should own a distinct project-building function.
Avoid agents that try to audit, research, write canonically, and harden all at once.

Good:
- coverage auditor
- research planner
- fact normalizer
- backlog architect
- release hardener

Weak:
- a single “master improvement agent” that does everything

### Rule 2 — Agents route, they do not canonize truth by themselves
An agent may identify where content should go.
It should not treat its own prompt file as a source of Jeep facts.

### Rule 3 — Agents must name canonical destinations
If the output recommends action, it should name the likely file path under:
- `vehicle/`
- `swap/`
- `book/`
- or, for meta-work, `skillbuilding/` or `docs/`

This prevents vague guidance.

### Rule 4 — Distinguish likely vs confirmed
Agents must clearly separate:
- planning hypotheses
- confirmed audit findings
- validated facts
- unresolved questions

This is one of the most important anti-drift rules in the project.

### Rule 5 — Agents must preserve scope
Agents should force explicit scope whenever relevant:
- stock Jeep vs swap procedure vs presentation guidance
- universal vs era-specific vs year-specific
- package-level vs single-file evaluation

### Rule 6 — Agents must define stop conditions
A good agent should know when not to continue.
Examples:
- evidence is too weak to promote a claim
- the topic must move to research planning
- the issue is really a canonical content task, not an agent task

### Rule 7 — Outputs should connect to existing framework artifacts
Whenever possible, agent outputs should map cleanly into:
- `backlog.md`
- `gap-report.md`
- `topic-brief.md`
- `source-intake.md`
- `critical-unknown-review.md`
- release-hardening decisions

## Required behavior patterns

### Pattern A — Input discipline
Agents should load only what they need.
They should not read large parts of the repo without a task reason.

### Pattern B — Traceable reasoning
Agents should make it visible why they reached a conclusion.
Not chain-of-thought detail, but explicit factors such as:
- missing dependency
- weak evidence
- year-range ambiguity
- poor destination fit

### Pattern C — Explicit uncertainty
Agents should preserve labels like:
- `likely`
- `confirmed`
- `provisional`
- `conflicting`
- `needs validation`

### Pattern D — Lifecycle awareness
Agents should know where a work item sits in:
- suspected
- audited
- researched
- normalized
- drafted
- hardened
- trusted

### Pattern E — Maturity awareness
If evaluating existing content, agents should consider whether the target is:
- stub
- partial
- usable with caveats
- trusted

## Anti-patterns to avoid
- vague outputs like “this area needs more detail”
- no canonical destination path
- flattening year-specific issues into general statements
- mixing likely gaps with confirmed gaps
- using weak sources as if they were settled
- creating agents that duplicate another agent’s job with slightly different wording
- embedding lots of Jeep facts into the agent prompt itself

## When to create a new agent
Create a new agent only if all are true:
1. the repo needs a repeatable meta-job not already covered
2. the job has a distinct output format or decision logic
3. the job cannot be handled cleanly by extending an existing agent
4. the new agent will reduce ambiguity or repetition in future work

If these are not true, improve an existing agent instead.

## Preferred agent growth path
When a new need appears:
1. identify the meta-job
2. check whether an existing agent can absorb it
3. if not, define the unique output artifact
4. define required framework files
5. define boundary rules
6. keep the new agent narrow

## Relationship to other files
- use `skillbuilding/skill-design-rules.md` for workflow design
- use `skillbuilding/artifact-contracts.md` to keep outputs standardized
- use `skillbuilding/operating-modes.md` for common repo-building modes
- use `skillbuilding/work-item-lifecycle.md` for stage awareness
- use `skillbuilding/file-maturity.md` when evaluating content trust
- use `skillbuilding/domain-map.md` to understand the domain surface being routed
- use `skillbuilding/meta-improvement-loop.md` when improving the framework itself
