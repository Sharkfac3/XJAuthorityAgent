# Repository Taxonomy

This document defines the target information architecture for the Jeep XJ knowledge repository.

It is the governing taxonomy for future growth and migration.
It does **not** create the full tree yet.
It defines where content belongs, how it should branch, and how agents should reason about placement.

## Purpose

The repo should answer five orientation questions quickly:

1. What is this repo about?
2. Where do stock Jeep XJ facts live?
3. Where do work procedures live?
4. Where do modification topics live?
5. How do year, era, trim, drivetrain, and donor differences get modeled without drift?

## Repo identity

This repo is a **Jeep XJ technical knowledge system**.

It is not only an ECU-swap repo.
ECU swaps remain important, but they are one work domain inside a broader architecture that must support:
- stock platform understanding
- maintenance and repair
- diagnostics and troubleshooting
- restoration and preservation
- upgrades and modifications
- major component swaps
- sourcing and interchange
- year, era, package, drivetrain, and subsystem differences

## Governing taxonomy principles

1. **Platform first.** The XJ is the anchor.
2. **Facts and actions stay separate.**
3. **Deep trees beat broad catch-all files.**
4. **Stock and modified states must both be routable.**
5. **Compatibility lives close to the affected topic.**
6. **Agent behavior is not canonical fact storage.**
7. **Governance docs describe the system; they do not replace it.**
8. **New topics must fit by rule, not by intuition.**

---

# 1. Top-level folder purpose

The target-state repo should use a small number of durable roots.

```text
agents/         Agent behavior, routing, loading instructions
book/           Presentation and writing rules
diagnostics/    Symptom-first troubleshooting and fault isolation
docs/           Repo governance, taxonomy, migration, architecture
sourcing/       Parts selection, donor interchange, buying guidance
skillbuilding/  Repo-building workflows, audits, backlog, research intake
vehicle/        Canonical Jeep XJ platform facts
work/           Job execution: maintenance, repair, restoration, upgrades, swaps
```

## `vehicle/`

Purpose: canonical facts about how Jeep XJs are built and how stock systems differ.

Use for:
- year and era differences
- package and drivetrain configuration facts
- subsystem architecture
- stock component families
- factory hardware changes
- baseline operating characteristics
- compatibility facts that describe what exists on the vehicle

Do not use for:
- procedures
- troubleshooting trees
- buying advice
- agent instructions

## `work/`

Purpose: explain how to perform jobs on or to the XJ.

Use for:
- maintenance
- repair
- restoration
- upgrades
- swaps
- installation workflows
- adjustment and setup
- post-work validation steps

Do not use for:
- pure platform facts
- symptom-first troubleshooting
- general sourcing-only comparisons

## `diagnostics/`

Purpose: isolate faults starting from symptoms, tests, or observed behavior.

Use for:
- no-start paths
- overheating diagnosis
- charging faults
- fuel pressure test logic
- door wiring fault isolation
- brake vibration or pull diagnosis
- driveline vibration isolation

Do not use for:
- long replacement procedures
- broad subsystem reference material
- buying guidance except minimal support notes

## `sourcing/`

Purpose: support parts, donor, kit, and interchange decisions.

Use for:
- donor-part interchange
- OEM vs aftermarket tradeoffs
- kit selection criteria
- replacement-part family comparisons
- connector sourcing
- donor axle and brake sourcing guidance

Do not use for:
- full install procedures
- canonical stock configuration facts beyond the minimum needed for fitment context
- diagnostics trees

## `agents/`

Purpose: routing and behavior only.

Use for:
- entrypoint instructions
- what to load for a task
- role-specific behavior
- review and output rules

Do not use for:
- storing Jeep technical facts
- duplicate troubleshooting logic
- duplicate procedures

## `book/`

Purpose: presentation-layer rules.

Use for:
- audience
- style
- chapter structure
- safety language
- callout conventions

Do not use for:
- technical truth
- work instructions
- platform facts

## `docs/`

Purpose: governance of the repo itself.

Use for:
- taxonomy
- routing principles
- naming rules
- migration plans
- audits

Do not use for:
- canonical Jeep knowledge

## `skillbuilding/`

Purpose: framework for improving the repo.

Use for:
- audits
- backlog planning
- research intake
- hardening workflows

Do not use for:
- final canonical Jeep fact storage

---

# 2. Second-level organizational logic

Each top-level domain should branch according to its own job.
Do not force one branch logic onto every root.

## `vehicle/` second-level logic: organize by platform truth

Primary second-level branches:

```text
vehicle/
  overview.md
  years/
  systems/
  packages/
  configurations/
  interchange-baselines/
```

### `vehicle/years/`
Use when the main question is time-based.

Examples:
- era identity
- 1996-only exceptions
- 2000–2001 ignition changes
- emissions-era differences

Suggested target pattern:

```text
vehicle/years/
  era1/
  era2/
  era3/
  1996-notes.md
```

### `vehicle/systems/`
Use when the main question is subsystem-based and may cut across years.

Examples:
- cooling architecture
- AW4 behavior
- Dana 30 baseline variants
- brake system families
- interior trim attachment differences

Suggested target pattern:

```text
vehicle/systems/
  engine/
  fuel/
  ignition/
  cooling/
  electrical/
  charging-starting/
  transmission/
  transfer-case/
  axles/
  suspension/
  steering/
  brakes/
  body/
  interior/
```

### `vehicle/packages/`
Use for package-defined stock differences.

Examples:
- towing package
- Up Country package
- police/export or market-specific notes if they become meaningful

### `vehicle/configurations/`
Use for stock configuration matrices that are not best expressed as a single subsystem or year page.

Examples:
- engine/trans combinations
- 2WD vs 4WD baselines
- ABS-equipped vs non-ABS baseline implications

### `vehicle/interchange-baselines/`
Use for factual interchange limits of stock parts.
This is not buying advice; it is factual fitment baseline.

Examples:
- which steering columns share mounting families
- which XJ years share front brake rotor patterns
- which axle families were factory paired to which engines or trims

## `work/` second-level logic: organize by job type first

Primary second-level branches:

```text
work/
  maintenance/
  repairs/
  restoration/
  upgrades/
  swaps/
  inspections/
  setup-and-calibration/
```

### Why job type comes before system here
A cooling refresh and a cooling upgrade are not the same class of work.
The distinction matters for routing, tool lists, and expected outcomes.

## `diagnostics/` second-level logic: organize by symptom domain or affected system

Primary second-level branches:

```text
diagnostics/
  engine/
  fuel/
  ignition/
  cooling/
  charging-and-starting/
  transmission/
  transfer-case/
  driveline/
  steering-and-suspension/
  brakes/
  body-electrical/
  body-and-interior/
```

## `sourcing/` second-level logic: organize by decision type

Primary second-level branches:

```text
sourcing/
  interchange/
  donor-vehicles/
  oem-vs-aftermarket/
  connectors/
  swap-kits/
  wear-items/
```

---

# 3. How to model deep trees

The repo should scale by branching downward, not by expanding broad summaries.

## Rule: branch by the next stable decision boundary

A tree should deepen when one of these becomes true:
- the topic has meaningful year splits
- the topic has front/rear or left/right splits
- the topic has stock vs modified divergence
- the topic has distinct work classes
- the topic has multiple component families
- the topic has enough detail that one file becomes a mixed-purpose document

## Recommended deep-tree sequence

When needed, branch in this order:
1. domain
2. work type or system
3. component family
4. variant or project type
5. compatibility split
6. procedure/reference/troubleshooting leaf

## Example: upgrade tree

```text
work/upgrades/brakes/wj-knuckle-swap/
  overview.md
  compatibility.md
  required-parts.md
  install-notes.md
  post-install-checks.md
```

## Example: stock fact tree

```text
vehicle/systems/axles/chrysler-8.25/
  overview.md
  spline-counts.md
  brakes.md
  year-changes.md
```

## Example: diagnostics tree

```text
diagnostics/fuel/fuel-pump/
  no-prime.md
  low-pressure.md
  intermittent-cutout.md
```

## Rule: do not branch unless the branch label is durable

Good branch labels:
- `aw4/`
- `dana-30/`
- `wj-brake-upgrade/`
- `era3/`
- `2wd/`
- `4wd/`

Bad branch labels:
- `misc/`
- `notes/`
- `random/`
- `other/`

---

# 4. Cross-cutting topics

Some XJ topics cut across years, trims, drivetrains, systems, and donor families.
These must be modeled explicitly so they do not create drift.

## Year and era differences

### Rule
Year and era truth belongs in `vehicle/` first.
Other domains may reference it, but they should not redefine it.

### Pattern
- put baseline difference in `vehicle/years/`
- attach local compatibility notes in the affected system or work topic
- create a year-specific file when the split is real and repeated often

Example:
- `vehicle/years/era3/overview.md`
- `vehicle/years/1996-notes.md`
- `work/swaps/ecu/compatibility/1996-jtec-caveats.md`

## Trims and packages

### Rule
If the difference is factory-defined and affects hardware, it belongs under `vehicle/packages/` or the affected stock system.

Examples:
- Up Country suspension baseline
- towing package cooling or axle differences
- ABS-equipped braking differences

## Drivetrains

### Rule
Use drivetrain splits when they change the truth materially.
Do not force drivetrain notes into every general file.

Examples:
- `vehicle/configurations/2wd-vs-4wd.md`
- `vehicle/systems/transfer-case/overview.md`
- `work/upgrades/driveline/sye/compatibility.md`

## Axle families

### Rule
Treat axle families as named component families under `vehicle/systems/axles/` for stock facts, then mirror them in `work/` or `sourcing/` only when the task changes.

Examples:
- stock baseline: `vehicle/systems/axles/dana-30/overview.md`
- procedure: `work/swaps/axles/dana-44-into-xj/overview.md`
- sourcing: `sourcing/interchange/axles/dana-30-donor-options.md`

## Donor-part interchange

### Rule
Separate factual fitment baseline from acquisition advice.

Use:
- `vehicle/interchange-baselines/` for factual stock compatibility
- `sourcing/interchange/` for what to pull, buy, avoid, or compare
- `work/.../compatibility.md` for project-specific fitment implications

## Modified-state dependencies

### Rule
If a topic exists only because the vehicle is no longer stock, it does not belong under stock `vehicle/` except as a brief baseline reference.

Examples:
- WJ brake upgrade → `work/upgrades/brakes/`
- LS swap planning → `work/swaps/drivetrain/`
- SYE upgrade → `work/upgrades/driveline/`

---

# 5. When a topic belongs under vehicle, system, workflow, reference, or troubleshooting

This is the core placement test.

## Put a topic under `vehicle/` when the question is:
- what the XJ came with
- how a stock system is arranged
- what changed by year, era, trim, or package
- what factory parts or architectures exist
- what a component does in stock form

Examples:
- AW4 operating behavior
- Renix sensor baseline
- stock cooling fan types
- Chrysler 8.25 stock variants

## Put a topic under `work/` when the question is:
- how to perform a job
- how to replace, service, install, upgrade, or swap something
- what sequence to follow
- what to verify before or after the work

Examples:
- cooling system refresh
- WJ brake upgrade install path
- ECU swap wiring procedure
- headliner replacement steps

## Put a topic under `diagnostics/` when the question is:
- what is wrong
- what tests isolate the fault
- what symptoms point to which branch
- how to verify or rule out a suspected failure

Examples:
- fuel pump no-prime diagnosis
- door wiring intermittent fault isolation
- charging system voltage drop diagnosis

## Put a topic under `sourcing/` when the question is:
- what donor or part to choose
- which kit or connector family to buy
- what parts interchange is practical
- what aftermarket or OEM option is preferable

Examples:
- Dana 30 donor axle options
- alternator upgrade donor choices
- ECU connector sourcing

## Put a topic under `docs/` when the question is:
- how the repo is organized
- where new content should go
- how migration should occur
- how names should be chosen

---

# 6. Stock baseline vs modified-state guidance

The repo must not blur stock truth with modified outcomes.

## Stock baseline
Store under `vehicle/`.
Use this to define what exists before work starts.

Examples:
- stock AW4 control behavior
- factory Dana 30 and Chrysler 8.25 variants
- stock charging system architecture

## Modified-state guidance
Store under `work/`, `diagnostics/`, or `sourcing/` depending on the question.

Examples:
- alternator upgrade wiring → `work/upgrades/electrical/`
- WJ brake conversion diagnosis after install → `diagnostics/brakes/`
- LS swap donor planning → `sourcing/donor-vehicles/` plus `work/swaps/drivetrain/`

## Rule
A modified topic may reference stock baseline facts, but it must not relocate them.

---

# 7. Component swaps vs direct upgrades

These are separate work classes and must not be mixed.

## Direct upgrade
Use when the XJ keeps the same core system role and receives a better or newer component.

Examples:
- alternator upgrade
- WJ brake upgrade
- steering box upgrade
- SYE upgrade
- cooling fan upgrade

Target path class:
- `work/upgrades/<system>/<topic>/`

## Component swap
Use when the XJ receives a materially different assembly, control system, or donor-family component.

Examples:
- ECU swap
- LS drivetrain swap
- axle family swap
- transfer-case swap

Target path class:
- `work/swaps/<system>/<topic>/`

## Rule of thumb
If the work changes platform architecture or donor-family identity, it is usually a swap.
If the work improves or replaces an existing architecture in-kind or near-kind, it is usually an upgrade.

---

# 8. Procedure docs vs reference docs vs troubleshooting docs

Every content type should advertise its job clearly.

## Procedure docs
Purpose: tell the reader what to do.

Usually live under:
- `work/`

Common leaf names:
- `procedure.md`
- `install.md`
- `bleeding.md`
- `adjustment.md`
- `post-install-checks.md`

## Reference docs
Purpose: describe what exists, how it is configured, or how variants differ.

Usually live under:
- `vehicle/`
- parts of `sourcing/`

Common leaf names:
- `overview.md`
- `compatibility.md`
- `year-changes.md`
- `specs.md`
- `variants.md`

## Troubleshooting docs
Purpose: isolate problems from symptoms and tests.

Usually live under:
- `diagnostics/`

Common leaf names:
- `no-start.md`
- `overheating-at-idle.md`
- `intermittent-loss.md`
- `poor-shift-quality.md`

## Rule
Do not merge all three document types into one file unless the topic is genuinely tiny.

---

# 9. Rules for overview files vs leaf files

## `overview.md`

Use `overview.md` when a folder needs a local router.

An overview should:
- define the scope of the folder
- summarize major branches or variants
- explain the main compatibility splits
- point to narrower leaf files
- stay short enough to support routing

An overview should **not**:
- become the hidden master document
- duplicate full procedures
- hold all troubleshooting steps for the entire branch

## Leaf files

Use leaf files when a topic can state one narrow truth or perform one narrow job.

A leaf file should:
- answer one bounded question well
- name its scope directly
- capture concrete year/variant limits
- avoid mixing stock facts, full procedures, and diagnostics when they are distinct concerns

## When to split an overview into leaves

Split when:
- a section needs repeated year caveats
- one section turns procedural and another stays referential
- one file covers multiple component families
- the file is serving as a router and a fact dump
- the user would reasonably ask for only one subsection

---

# 10. How to add a new topic without creating drift

Use this placement sequence every time.

## Step 1: classify the question type

Ask:
- Is this stock platform truth?
- Is this a procedure?
- Is this troubleshooting?
- Is this sourcing or interchange?
- Is this governance/meta?

## Step 2: classify stock vs modified

Ask:
- Is the topic about a stock XJ baseline?
- Is it about maintenance or repair of stock hardware?
- Is it about a modification, upgrade, or swap?

## Step 3: classify the dominant system

Examples:
- cooling
- fuel
- charging-starting
- steering
- brakes
- body-electrical
- interior

## Step 4: classify the compatibility split

Ask whether the content must branch by:
- era or year
- 2WD vs 4WD
- automatic vs manual
- ABS vs non-ABS
- package
- axle family
- donor family

## Step 5: decide whether the topic needs a folder or a leaf

Create a folder when the topic will likely contain:
- overview
- compatibility
- parts
- procedure
- validation
- troubleshooting follow-up

Create a single leaf when one file can remain narrow and durable.

## Step 6: place cross-links, not duplicate facts

If the topic needs year truth, link to `vehicle/years/...`.
If it needs stock subsystem truth, link to `vehicle/systems/...`.
If it needs donor or parts choice, link to `sourcing/...`.
If it needs failure isolation, link to `diagnostics/...`.

---

# 11. Routing examples

These examples define expected placement logic for realistic XJ topics.
They are examples of taxonomy and routing, not a command to build the full tree immediately.

## 1. Renix sensor baseline
Primary home:
- `vehicle/years/era1/sensors/`

Why:
- stock sensor truth tied to Renix era

Likely pattern:
- `vehicle/years/era1/sensors/overview.md`
- leaf per sensor where needed

## 2. AW4 transmission behavior
Primary home:
- `vehicle/systems/transmission/aw4/overview.md`

Why:
- stock behavior and constraints

Related routes:
- diagnostics: `diagnostics/transmission/`
- upgrade or controller changes: `work/upgrades/` or `work/swaps/`

## 3. Dana 30 axle swap options
Primary homes:
- stock baseline: `vehicle/systems/axles/dana-30/overview.md`
- donor and fitment choices: `sourcing/interchange/axles/dana-30-donor-options.md`
- actual swap execution: `work/swaps/axles/<topic>/`

## 4. Chrysler 8.25 upgrade notes
Primary homes:
- stock baseline: `vehicle/systems/axles/chrysler-8.25/overview.md`
- modification guidance: `work/upgrades/axles/chrysler-8.25/`

## 5. WJ brake upgrade
Primary home:
- `work/upgrades/brakes/wj-brake-upgrade/`

Supporting homes:
- stock brake baseline: `vehicle/systems/brakes/`
- donor/parts guidance: `sourcing/interchange/brakes/wj-brake-parts.md`

## 6. Cooling system refresh
Primary home:
- `work/maintenance/cooling/system-refresh/`

Why:
- maintenance job, not a platform fact and not a symptom tree

## 7. Alternator upgrade
Primary home:
- `work/upgrades/electrical/alternator-upgrade/`

Supporting homes:
- stock charging facts: `vehicle/systems/charging-starting/`
- donor choice: `sourcing/interchange/electrical/alternator-options.md`

## 8. Fuel pump diagnostics
Primary home:
- `diagnostics/fuel/fuel-pump/`

Likely leaves:
- `no-prime.md`
- `low-pressure.md`
- `intermittent-cutout.md`

## 9. Headliner repair
Primary home:
- `work/repairs/interior/headliner-repair/`

Why:
- repair procedure for body/interior system

## 10. Door wiring issues
Primary home:
- `diagnostics/body-electrical/door-wiring/`

Supporting home:
- stock body harness facts: `vehicle/systems/electrical/body-wiring/`

## 11. Suspension lift geometry
Primary homes:
- stock baseline geometry: `vehicle/systems/suspension/geometry.md`
- modified guidance: `work/upgrades/suspension/lifts/geometry-effects.md`

## 12. Steering box swap
Primary home:
- `work/swaps/steering/steering-box/`

Supporting homes:
- stock steering baseline: `vehicle/systems/steering/`
- donor choice: `sourcing/interchange/steering/steering-box-options.md`

## 13. LS swap planning
Primary homes:
- planning and execution: `work/swaps/drivetrain/ls-swap/`
- donor decision support: `sourcing/donor-vehicles/drivetrain/ls-family.md`

## 14. ECU swap wiring
Primary home:
- `work/swaps/ecu/wiring/`

Migration note:
- current canonical content still lives under `swap/wiring/` until migration

## 15. Transfer case SYE upgrade
Primary home:
- `work/upgrades/driveline/sye/`

Supporting homes:
- stock transfer-case baseline: `vehicle/systems/transfer-case/`
- driveline vibration follow-up: `diagnostics/driveline/`

## 16. No-start after crank sensor replacement
Primary home:
- `diagnostics/ignition/no-start-after-cps-work.md`

Supporting home:
- stock trigger baseline: `vehicle/years/<era>/trigger.md` during transition, later `vehicle/systems/ignition/`

## 17. Up Country package suspension baseline
Primary home:
- `vehicle/packages/up-country/suspension.md`

## 18. XJ rear axle donor interchange
Primary home:
- `sourcing/interchange/axles/rear-axle-donor-options.md`

Supporting home:
- `vehicle/systems/axles/`

---

# 12. Present-state transition rule

The repo is still in transition.
The target taxonomy governs future placement, but existing canonical branches remain valid until migrated.

## Current valid roots
- `vehicle/`
- `swap/`
- `book/`
- `agents/`

## Transition mapping
- current `swap/` content should be treated as the future `work/swaps/ecu/` branch during migration
- current era content in `vehicle/era1`, `vehicle/era2`, and `vehicle/era3` remains canonical until a future `vehicle/years/` and `vehicle/systems/` structure is created

## Migration guardrail
Do not force-move content conceptually until the destination branch rules are stable.
Use this document to guide future additions and eventual migration.

---

# 13. Anti-drift rules

1. Do not store Jeep facts in `agents/`.
2. Do not store repo rules in `vehicle/`, `work/`, or `diagnostics/`.
3. Do not use `misc`, `general`, `other`, or `notes` as category buckets.
4. Do not put troubleshooting inside procedure files unless the troubleshooting is trivial.
5. Do not put donor-part comparisons inside stock fact files except for minimal reference context.
6. Do not flatten year-specific truths to avoid making a new file.
7. Do not put modification guidance inside stock baseline files except as a short pointer to the correct work branch.
8. Do not add new broad top-level roots when a deep branch under an existing root is sufficient.

---

# 14. Summary

The durable architecture is:
- `vehicle/` for stock platform truth
- `work/` for jobs and project execution
- `diagnostics/` for symptom-first fault isolation
- `sourcing/` for parts, donor, and interchange decisions
- `agents/`, `book/`, `docs/`, and `skillbuilding/` for behavior, presentation, governance, and repo growth

New topics should be placed by rule:
1. classify the question type
2. classify stock vs modified
3. classify the system
4. classify the compatibility split
5. create a router only when a folder is truly needed
6. cross-link instead of duplicating facts
