# Topic Intake Rules

This document defines how a new Jeep XJ topic enters the repo expansion system.

Use it before creating canonical files, backlog items, or research packages.

It should be used with:
- `docs/repo-taxonomy.md`
- `docs/content-governance.md`
- `docs/research-pipeline.md`
- `docs/backlog-seeding-guide.md`
- `skillbuilding/source-policy.md`

## Purpose
Topic intake exists to stop structural drift at the front door.
A topic should be classified before it is researched deeply and before a new file is created.

The intake process must answer:
1. what is being asked
2. why it matters
3. where it belongs in the taxonomy
4. what uncertainty is already known
5. whether the topic is narrow enough to write as one file

---

# 1. Intake triggers

A topic should enter intake when it appears through any of these channels:
- repeated user questions
- a missing branch noticed during normal work
- an audit finding
- a migration planning need
- a broad file that clearly needs splitting
- a source packet that introduces a durable new subject
- a high-risk uncertainty that blocks reliable writing

Do not skip intake just because the answer feels obvious.

---

# 2. Intake questions

Every proposed topic must answer these questions in order.

## A. What kind of question is this?
Choose the dominant type:
- stock platform fact
- work procedure
- diagnostics or fault isolation
- sourcing/interchange decision
- governance/meta

## B. What top-level domain owns the canonical answer?
Choose one primary home:
- `vehicle/`
- `work/`
- `diagnostics/`
- `sourcing/`
- `docs/`
- transitional `swap/` for ECU swap execution topics

## C. Is this stock baseline or modified-state guidance?
- stock baseline
- maintenance or repair of stock hardware
- restoration
- upgrade
- swap
- inspection
- setup/calibration

## D. Which system owns the topic?
Examples:
- engine
- fuel
- cooling
- charging-starting
- transmission
- transfer-case
- driveline
- axles
- steering
- suspension
- brakes
- body
- interior
- hvac
- body-electrical

## E. Which compatibility dimensions change the answer?
Check all that apply:
- era
- year
- engine family
- transmission type
- 2WD vs 4WD
- ABS vs non-ABS
- package/trim
- axle family
- donor family
- emissions family
- market/export variation

## F. Is the topic narrow enough for one file?
A single leaf is appropriate when one bounded question can be answered clearly.
A branch is needed when the topic requires multiple durable children such as:
- `overview.md`
- `compatibility.md`
- `procedure.md`
- `required-parts.md`
- `validation.md`
- symptom-specific diagnostic leaves

---

# 3. Placement rules during intake

## Put the topic in `vehicle/` when
The question is mainly:
- what the XJ had
- how the stock system is arranged
- what changed by year, era, package, or drivetrain
- what factory component families exist

## Put the topic in `work/` when
The question is mainly:
- how to perform a job
- how to maintain, repair, restore, upgrade, swap, inspect, or set up

## Put the topic in `diagnostics/` when
The question is mainly:
- what symptom points to what failure path
- what tests isolate the fault
- how to confirm the root cause

## Put the topic in `sourcing/` when
The question is mainly:
- which donor, part family, connector, or kit to choose
- what interchange choices are practical
- whether OEM or aftermarket is better for the job

## Put the topic in `docs/` when
The question is about:
- taxonomy
- repo growth
- naming
- pipeline rules
- migration

## Put the topic in transitional `swap/` when
The question is specifically ECU swap execution and the future `work/swaps/ecu/` destination does not exist yet.

---

# 4. Intake artifact contract

Every intake should produce a small, structured topic card.

## Required fields
- proposed title
- dominant question
- why this topic exists now
- primary domain
- stock vs modified classification
- work class if applicable
- owning system
- compatibility dimensions
- likely canonical destination
- likely supporting domains
- known evidence state
- known uncertainties
- recommended next step

## Recommended next-step values
- seed backlog item
- create research brief
- split existing broad file
- create stub router only
- defer until dependency exists
- reject because topic duplicates an existing canonical branch

---

# 5. Intake acceptance rules

Accept a topic into the pipeline when:
- it answers a real user or repo need
- it has a clear dominant question type
- it has a plausible canonical home
- it is not just a duplicate wording of an existing topic
- its scope can be made narrow and durable

Reject or merge the intake when:
- the topic already exists canonically
- it is only a synonym for an existing branch
- it is too vague to classify
- it mixes many question types without a dominant one
- it depends on unresolved broader classification decisions

---

# 6. Broad-topic handling

Broad topics should not enter the backlog as one giant writing request.
They must be split during intake.

## Broad-topic split method
For a broad topic:
1. identify the dominant domains involved
2. separate stock facts from procedures, diagnostics, and sourcing
3. separate work classes inside `work/`
4. separate durable systems or component families
5. identify real compatibility splits
6. convert the broad topic into a branch seed plus smaller backlog items

## Example: "cooling system"
Do not create one huge file.
Instead classify into possible branches such as:
- `vehicle/systems/cooling/`
- `work/maintenance/cooling/`
- `work/repairs/cooling/`
- `work/upgrades/cooling/`
- `diagnostics/cooling/`
- `sourcing/interchange/cooling/` when needed

## Example: "axles"
Do not mix all axle facts and jobs into one path.
Split into:
- stock baseline families under `vehicle/systems/axles/`
- maintenance/repair topics under `work/`
- swap topics under `work/swaps/axles/`
- donor/interchange guidance under `sourcing/interchange/axles/`

---

# 7. Uncertainty handling at intake time

Intake is allowed to carry uncertainty, but it must label it.

## Required uncertainty fields
- current confidence level
- missing evidence areas
- likely year-range ambiguity
- conflicting source hints if already known
- whether the topic should be blocked until source work begins

## Approved intake labels
- `confirmed gap`
- `likely gap`
- `needs source`
- `year-range uncertain`
- `transition-year caution`
- `conflicting reports`

## Rule
Do not write intake notes as settled truth.
Intake is a routing and planning layer, not canonical fact storage.

---

# 8. Human and agent usability rules

The intake system must work for both humans and agents.

## For humans
Intake should make it obvious:
- what the topic is
- why it matters
- what branch should own it
- what work remains before writing canon

## For agents
Intake should make it easy to infer:
- which router to load first
- which compatibility dimensions matter
- whether a branch or leaf should be created
- which supporting domains need cross-links

## Rule
Do not require repo-history knowledge to understand an intake card.

---

# 9. Anti-drift intake rules

Do not accept a topic proposal that would:
- store Jeep facts in `agents/`, `docs/`, or `skillbuilding/`
- force non-swap content into `swap/`
- create vague folders such as `misc/`, `general/`, or `other/`
- merge stock truth, procedures, diagnostics, and sourcing into one file without a tiny-topic justification
- create a broad mega-doc when a branch is clearly needed

---

# 10. Intake outputs by topic type

## Stock fact topic
Typical next step:
- route to `vehicle/`
- determine year/system/package placement
- create backlog item for baseline reference and compatibility split

## Maintenance or repair topic
Typical next step:
- route to `work/maintenance/` or `work/repairs/`
- define stock baseline dependencies in `vehicle/`
- seed a procedure package if the job is multi-step

## Diagnostic topic
Typical next step:
- route to `diagnostics/`
- define symptom-first leaf names
- identify supporting baseline and repair links

## Sourcing topic
Typical next step:
- route to `sourcing/`
- define decision criteria and donor/fitment splits
- cross-link to stock baseline files rather than restating them

## Repo-governance topic
Typical next step:
- route to `docs/` or `skillbuilding/`
- keep it out of canonical Jeep fact trees

---

# 11. Minimal intake template

```text
Title:
Dominant question:
Why now:
Primary domain:
Stock vs modified:
Work class:
Owning system:
Compatibility dimensions:
Likely canonical destination:
Supporting domains:
Known evidence state:
Known uncertainties:
Recommended next step:
```

---

# 12. Summary

A new topic should enter through a small, explicit intake process.
That process classifies the topic, bounds its scope, preserves uncertainty, and points it toward the correct canonical destination before research or writing begins.
