# Skill Design Rules

Use this file when creating or revising workflow skills under `skillbuilding/skills/`.

## Purpose
A skill is not just a prompt.
It is a structured workflow that tells an agent how to move through a repo-building task.

This file defines how to build skills that are consistent, composable, and aligned with the rest of the skillbuilding framework.

## What a skill is
In this repo, a skill should provide:
- a repeatable sequence of steps
- clear inputs
- a defined output artifact or decision
- links to the framework files that govern the work

A skill is the workflow layer.
An agent is the role layer.

## Core distinction
- **agent** = who is doing the job and what rules they follow
- **skill** = how the job is executed step by step

Good skill design keeps those two layers separate.

## Required sections for every skill
Every skill should include:

### 1. Purpose statement
Say when the skill should be used.

### 2. Steps
Give an ordered sequence.
The steps should be concrete and reusable.

### 3. Expected outputs
Say what artifact, decision, or recommendation should come out of the workflow.

### 4. Success condition
State what “good completion” looks like.

## Core design rules

### Rule 1 — One workflow per skill
A skill should do one type of repo-building workflow well.
If it tries to cover multiple unrelated workflows, it should probably be split.

### Rule 2 — Skills should compose with agents
A skill should usually reference the matching skillbuilding agent for the role behavior.

### Rule 3 — Skills should load framework files before domain files
In most cases, a skill should read:
1. `AGENTS.md`
2. relevant skillbuilding framework files
3. the matching agent file
4. only then the canonical target files needed for the task

### Rule 4 — Skills should avoid duplicating policy
Do not restate large chunks of:
- gap taxonomy
- evidence standards
- source policy
- maturity model
- lifecycle rules

Reference those files instead.

### Rule 5 — Skills should define output shape implicitly or explicitly
The workflow should make it obvious whether the result is supposed to become:
- a gap report
- a topic brief
- a source intake packet
- a backlog item set
- a release-hardening verdict

### Rule 6 — Skills should be reusable across topics
A good skill should work for multiple topics in the domain.
It should not be overly tied to one very narrow Jeep fact unless that is truly necessary.

## Good skill structure pattern
A strong skill usually looks like:
1. read routing context
2. read framework/policy context
3. read role prompt
4. read task-specific canonical files
5. classify the problem
6. produce a structured output
7. route next actions

## Anti-patterns to avoid
- skills that are only vague reminders
- skills that restate the whole framework instead of using it
- skills that imply canonical truth without validation
- skills that skip output expectations
- skills that load broad repo content by default
- skills that mix writing/editing with auditing unless that combination is intentional and explicit

## When to create a new skill
Create a new skill when:
1. a workflow is repeated often
2. step order matters
3. the workflow uses a distinct output artifact
4. the workflow would otherwise be inconsistently performed by different agents

Do not create a new skill just because a new topic exists.
New topics usually need the same skills, not more skills.

## Preferred skill growth path
When a new recurring workflow appears:
1. identify the workflow boundary
2. identify the expected output artifact
3. identify required framework inputs
4. pair it with an existing or new agent only if needed
5. keep the steps minimal but sufficient

## Relationship to other files
- use `skillbuilding/agent-design-rules.md` for role prompt design
- use `skillbuilding/operating-modes.md` for common workflow modes
- use `skillbuilding/domain-map.md` to understand what content surface the skill may touch
- use `skillbuilding/work-item-lifecycle.md` to align workflow outcomes with project stage
