# Meta Improvement Loop

Use this file to improve `skillbuilding/` itself.

## Purpose
Most of the framework focuses on improving canonical repo content.
This file focuses on improving the framework that improves the content.

In other words:
this is the process for building better stuff that builds better stuff.

## When to use this loop
Use this loop when:
- `skillbuilding/` feels repetitive or inconsistent
- agents produce outputs that do not compose well
- skills overlap or leave gaps between stages
- templates are too weak, too vague, or too fragmented
- the framework adds friction instead of removing it

## Core principle
Do not add new framework files just because a new idea appears.
Improve the framework only when the change increases one or more of these:
- consistency
- composability
- routing clarity
- output quality
- lifecycle coverage
- reduced duplication

## Meta improvement stages

### 1. Detect friction
Ask:
- where are agents or skills producing inconsistent outputs?
- where are users forced to improvise structure?
- where does the framework duplicate itself?
- where does a lifecycle transition have weak support?

Output:
- a clearly stated framework problem

### 2. Classify the framework problem
Common classes:
- missing policy
- missing artifact contract
- weak routing
- overlapping agent roles
- overlapping skill workflows
- missing lifecycle bridge
- missing design rule
- template weakness

Output:
- problem class
- affected files
- impact on the rest of the framework

### 3. Choose the lightest fix
Possible fixes, from lightest to heaviest:
1. clarify an existing file
2. extend a template
3. tighten an agent or skill prompt
4. add a cross-reference
5. create one new framework file
6. restructure multiple files only if necessary

Rule:
Prefer the smallest change that improves the system.

### 4. Define the contract
Before adding or changing framework structure, define:
- what problem it solves
- what inputs it expects
- what outputs it standardizes
- what existing files it connects to
- what future duplication it should prevent

### 5. Integrate the change
After the change exists:
- wire it into `skillbuilding/index.md`
- add references in any affected README/router file
- connect it to the relevant agents, skills, or templates
- avoid orphan framework files

### 6. Evaluate the result
Ask:
- did this reduce ambiguity?
- did this create a cleaner lifecycle transition?
- did this replace ad hoc output patterns with a standard?
- did this accidentally duplicate an existing framework file?

## Meta anti-patterns
Avoid:
- creating framework files that only rename existing ideas
- building separate files for tiny variations of the same pattern
- adding policy without wiring it into agents/skills
- adding templates no workflow actually uses
- solving a human discipline problem with unnecessary folder growth

## Good meta changes
Good framework changes usually do one of these:
- standardize a recurring output
- improve transitions between stages
- reduce ambiguity between agent roles
- reduce ambiguity between skills
- reduce duplication across docs
- improve routing into canonical destinations

## Relationship to other files
- use `skillbuilding/agent-design-rules.md` for agent-level fixes
- use `skillbuilding/skill-design-rules.md` for skill-level fixes
- use `skillbuilding/artifact-contracts.md` for output standardization
- use `skillbuilding/operating-modes.md` to identify weak workflow modes
- use `skillbuilding/work-item-lifecycle.md` to identify weak stage transitions
