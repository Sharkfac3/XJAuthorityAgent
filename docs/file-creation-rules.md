# File Creation Rules

Use this document when adding, splitting, or relocating content.

## Purpose
Define a repeatable placement method so new files land in the right branch, stay narrow, and do not create duplicate truth.

## Creation sequence
1. Classify the task type.
2. Choose the owning top-level domain.
3. Decide stock baseline vs modified-state.
4. Decide system or work class.
5. Decide whether to extend an existing branch or create a new one.
6. Decide whether the topic needs a folder or a single leaf.
7. Name the path using `docs/naming-conventions.md`.
8. Add cross-links instead of copying facts from other domains.
9. Mark uncertainty, year limits, and confidence explicitly.

## Step 1: classify the task type
- stock fact → `vehicle/`
- procedure or project execution → `work/`
- diagnostic logic → `diagnostics/`
- sourcing or interchange decision → `sourcing/`
- presentation rule → `book/`
- repo-governance or migration rule → `docs/`
- repo-building workflow or audit artifact → `skillbuilding/`

## Step 2: choose the correct top-level branch
### Use `vehicle/` for
- stock configurations
- year and package differences
- subsystem baselines
- factual stock interchange limits

### Use `work/` for
- maintenance
- repairs
- restoration
- upgrades
- swaps
- inspections
- setup and calibration

### Use `diagnostics/` for
- symptom-based fault isolation
- test paths
- verification logic

### Use `sourcing/` for
- part-family comparisons
- donor guidance
- connectors
- kits
- OEM vs aftermarket decisions

## Step 3: separate stock from modified
### Stock baseline
Home: `vehicle/`

### Modified-state content
Home depends on task:
- install or change work → `work/`
- fault isolation after modification → `diagnostics/`
- donor or kit choice → `sourcing/`

Rule: modified content may reference stock baseline files, but should not absorb them.

## Step 4: choose the system or work class
### Work classes
- `maintenance/`
- `repairs/`
- `restoration/`
- `upgrades/`
- `swaps/`
- `inspections/`
- `setup-and-calibration/`

### Common system branches
- `engine/`
- `fuel/`
- `ignition/`
- `cooling/`
- `electrical/`
- `charging-starting/`
- `transmission/`
- `transfer-case/`
- `axles/`
- `suspension/`
- `steering/`
- `brakes/`
- `body/`
- `interior/`
- `body-electrical/`
- `driveline/`

## Step 5: extend existing branch vs create new branch
### Extend an existing branch when
- the topic matches the branch's current job and scope
- the branch already owns that system or project family
- one new leaf can answer the new question cleanly
- the new content would not confuse the branch identity

### Create a new branch when
- the topic introduces a durable component family or project family
- multiple leaf types will be needed
- repeated caveats show the topic needs local compatibility handling
- the existing branch would become mixed-purpose or too broad

## Folder vs leaf rule
### Create a single leaf when
- one file can answer one bounded question cleanly
- no local compatibility, parts, or procedure stack is needed

Examples:
- `diagnostics/cooling/overheating-at-idle.md`
- `vehicle/packages/up-country/suspension.md`

### Create a folder when
- the topic needs multiple durable children such as:
  - `overview.md`
  - `compatibility.md`
  - `required-parts.md`
  - `procedure.md`
  - `post-install-checks.md`

Examples:
- `work/upgrades/brakes/wj-brake-upgrade/`
- `vehicle/systems/axles/dana-30/`
- `diagnostics/fuel/fuel-pump/`

## Required placement tests
Before creating a file, answer:
1. What is the dominant question type?
2. Is this stock or modified?
3. Is this maintenance, repair, upgrade, swap, restoration, inspection, or setup?
4. Which system owns it?
5. Which compatibility dimensions materially change the answer?
6. Is there already a canonical branch that should own this?
7. Can the topic stay a leaf, or does it need a subtree?

## Compatibility placement rule
Create compatibility leaves only when compatibility materially changes the answer.

Common compatibility dimensions:
- year or era
- engine family
- transmission type
- 2WD vs 4WD
- ABS vs non-ABS
- package or trim
- axle family
- donor family

Prefer:
- local `compatibility.md` inside the affected topic folder
- year-specific leaf files when the split is real and repeated

Avoid:
- smearing the same caveat across many unrelated files

## Uncertainty and confidence rule
Every new file should make scope limits visible.

If any claim is uncertain, mark it directly with labels such as:
- `confirmed`
- `likely`
- `unverified`
- `needs source`
- `year-range uncertain`
- `transition-year caution`

If uncertainty is central to the topic, prefer a dedicated note or compatibility file over burying it in one sentence.

## Cross-linking rule
When a file needs supporting truth from another domain:
- link to the canonical source
- summarize only what is needed for local context
- do not copy the whole fact set into the new file

Examples:
- a brake upgrade procedure can point to stock brake baselines in `vehicle/`
- an axle swap folder can point to donor choices in `sourcing/`
- a diagnostic leaf can point to the relevant repair procedure in `work/`

## Router rules
### Use `index.md` for
- domain routers
- major workflow routers
- agent entrypoints

### Use `overview.md` for
- local branch routers inside technical content trees

### Router constraint
Routers should classify and point.
They should not become hidden mega-docs.

## Transitional placement rules
During migration:
- keep current ECU swap execution content under `swap/` unless migration is part of the task
- respect current canonical `vehicle/era1/`, `vehicle/era2/`, `vehicle/era3/`, and `vehicle/trans/` content
- place new non-swap content according to the target taxonomy, not under `swap/`

## Quick routing examples for file creation
### Stock identification question
Example topic: factory brake family by year
- create under `vehicle/`
- likely path: `vehicle/years/...` or `vehicle/systems/brakes/...`

### Maintenance procedure request
Example topic: cooling system refresh
- create under `work/maintenance/cooling/`

### Diagnostic workflow request
Example topic: crank-no-start
- create under `diagnostics/ignition/` or other owning diagnostic branch

### Axle swap planning question
Example topic: Dana 44 into XJ
- procedure folder under `work/swaps/axles/`
- donor/selection support under `sourcing/interchange/axles/`
- stock axle baseline stays in `vehicle/systems/axles/`

### Brake upgrade question
Example topic: WJ brake upgrade
- folder under `work/upgrades/brakes/wj-brake-upgrade/`
- supporting part-choice guidance under `sourcing/interchange/brakes/`

### ECU swap wiring question
Example topic: aftermarket ECU harness integration
- current canonical home under `swap/wiring/`
- supporting stock-era facts under `vehicle/`

### Body/interior repair question
Example topic: headliner repair
- create under `work/repairs/interior/` or `work/restoration/interior/` depending on job intent

### Repo-building/restructure task
Example topic: deciding where future steering coverage belongs
- create governance rules in `docs/`
- create audit or backlog artifacts in `skillbuilding/`

## Names to avoid
Do not create:
- `misc/`
- `general/`
- `other/`
- `notes/` as a catch-all
- `temp/`
- `new/`
- `final/`

Use explicit, durable names instead.

## Final checklist before writing a new file
- correct domain?
- correct stock vs modified classification?
- correct work class or system?
- branch extended or created for a durable reason?
- path named clearly?
- canonical facts linked, not duplicated?
- uncertainty and year limits marked?
- router and human navigation still aligned?
