# Artifact Contracts

Use this file to standardize the outputs produced by `skillbuilding/` agents and skills.

## Purpose
The framework already defines:
- what kinds of repo-building work exist
- how evidence should be judged
- how maturity should be classified
- how work should move through lifecycle stages

What this file adds is **output consistency**.
It defines the expected shape and intent of the core artifacts so agents and skills can compose cleanly.

This is scaffolding for scaffolding:
it makes future prompts easier to build, easier to compare, and easier to route into the next step.

## Core rule
If a repo-building workflow produces an artifact that already exists in this framework, reuse that artifact shape instead of inventing a new one.

## Artifact list

### 1. Gap report
Primary use:
- audit mode

Template:
- `skillbuilding/templates/gap-report.md`

Must answer:
- what was audited
- what is missing, weak, unclear, unverified, misplaced, or conflicting
- why it matters to the swap
- where the answer belongs canonically
- what should happen next

Should feed into:
- `skillbuilding/backlog.md`
- `skillbuilding/templates/critical-unknown-review.md`
- research planning

### 2. Topic brief
Primary use:
- research-planning mode

Template:
- `skillbuilding/templates/topic-brief.md`

Must answer:
- what question is being resolved
- what scope/year range applies
- what decisions are blocked
- what evidence is needed
- what order the work should follow

Should feed into:
- source intake
- backlog items
- canonical drafting support

### 3. Source intake packet
Primary use:
- source-intake mode

Template:
- `skillbuilding/templates/source-intake.md`

Must answer:
- what the source is
- which claims it supports
- what confidence or status applies to each claim
- what conflicts and caveats exist
- where each claim should go canonically

Should feed into:
- normalized findings
- canonical drafting support
- research follow-up

### 4. Critical unknown review
Primary use:
- audit mode
- hardening mode

Template:
- `skillbuilding/templates/critical-unknown-review.md`

Must answer:
- whether a critical unknown is still only likely or now confirmed
- what appears covered vs weak
- what confidence level exists
- what the next action should be

Should feed into:
- backlog reprioritization
- release hardening follow-up

### 5. Backlog item
Primary use:
- backlog mode

Template:
- `skillbuilding/templates/backlog-item.md`

Canonical destination:
- `skillbuilding/backlog.md`

Must answer:
- what work should be done
- what lifecycle status it is in
- where it belongs canonically
- what dependency chain exists
- what maturity target and definition of done apply

Should feed into:
- future audit, research, drafting, or hardening work

### 6. Hardening verdict
Primary use:
- hardening mode

Template:
- `skillbuilding/templates/hardening-verdict.md`

Current shape:
- readiness verdict
- blockers
- caveats to preserve
- next actions required

Must answer:
- is this file/package trusted enough for normal use?
- what still blocks trust?
- what caveats must survive even if usable?

Should feed into:
- `skillbuilding/backlog.md`
- file/package maturity updates

## Output normalization rules
All artifacts should:
- use canonical repo paths where relevant
- distinguish likely vs confirmed
- preserve year/era scope explicitly
- preserve uncertainty labels when needed
- avoid embedding unsupported Jeep facts as settled truth

## When a new artifact type is justified
Create a new artifact only if:
1. an existing artifact cannot represent the output cleanly
2. the workflow recurs enough to justify a new standard
3. the artifact has a distinct role in the lifecycle
4. it improves composability instead of fragmenting it

If these are not true, extend an existing artifact or template instead.

## Relationship to other files
- use `skillbuilding/agent-design-rules.md` to make agent outputs map cleanly into artifacts
- use `skillbuilding/skill-design-rules.md` to align workflows with artifact creation
- use `skillbuilding/operating-modes.md` to understand which artifact belongs to which mode
- use `skillbuilding/work-item-lifecycle.md` to route one artifact into the next stage
