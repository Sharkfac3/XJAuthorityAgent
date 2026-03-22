# Routing Principles

This document defines how agents and maintainers should route questions, files, and future content through the repository.

It is the operational companion to `docs/repo-taxonomy.md`.

## Purpose

Routing should let an agent enter cold, classify the request quickly, and load only the narrowest truthful files.

The routing model must answer:
- what kind of question is being asked
- which domain owns the canonical answer
- whether the topic is stock or modified
- whether year, era, package, drivetrain, or donor differences materially change the answer
- which files should be loaded first and which should remain unloaded

---

# 1. Core routing rule

Route by **question type first**, not by whatever folder currently feels closest.

## Primary classification questions

1. Is the user asking about **what the XJ is or came with**?
   - Route to `vehicle/`
2. Is the user asking **how to do a job**?
   - Route to `work/`
3. Is the user asking **what is wrong and how to isolate it**?
   - Route to `diagnostics/`
4. Is the user asking **what part, donor, kit, or option to choose**?
   - Route to `sourcing/`
5. Is the user asking **how the answer should be presented**?
   - Route to `book/`
6. Is the user asking **how the repo should be structured or expanded**?
   - Route to `docs/` and `skillbuilding/`

## Secondary classification questions

After the domain is chosen, ask:
- Is this stock baseline or modified-state guidance?
- Which system owns the topic?
- Which compatibility splits matter?
- Is this a routing overview or a leaf answer?

---

# 2. Canonical domain ownership

## `vehicle/` owns
- stock platform facts
- year and era differences
- trim, package, and drivetrain baselines
- stock subsystem architecture
- factory component families
- baseline interchange facts

## `work/` owns
- maintenance procedures
- repair procedures
- restoration work
- upgrades
- swaps
- setup and post-work validation

## `diagnostics/` owns
- symptom-first troubleshooting
- test sequences
- verification and fault isolation logic
- pre-repair and post-repair confirmation paths

## `sourcing/` owns
- donor comparisons
- interchange choices
- kit and connector selection
- OEM vs aftermarket guidance
- option tradeoffs and acquisition advice

## `agents/` owns
- behavior and loading logic
- user-facing role instructions
- task routing guidance

## `docs/` owns
- taxonomy
- routing rules
- naming rules
- migration planning
- architecture governance

---

# 3. Routing sequence for agents

## Required entry sequence for restructuring work

1. Read `SKILL.md`
2. Read `AGENTS.md`
3. Read the relevant governance target, such as `docs/project-reframe.md`
4. Read only the current routing and taxonomy docs needed for the task
5. Read only the minimum canonical content needed to understand present layout

## Recommended entry sequence for ordinary technical questions

1. Read `SKILL.md`
2. Read `AGENTS.md`
3. Identify the question type
4. Load the domain router for that type
5. Load one narrow branch router if needed
6. Load only the necessary leaf files

## Load minimization rule

An agent should prefer:
- one router
- one system or work branch
- one to three leaf files

An agent should avoid:
- loading every era
- loading every file in a domain
- loading governance docs for ordinary technical questions

---

# 4. Stock vs modified routing

This distinction is mandatory.

## Route to stock baseline when the question is about:
- factory configuration
- original system behavior
- year or package differences in stock form
- what components were used from the factory

Primary home:
- `vehicle/`

## Route to modified-state guidance when the question is about:
- changing the vehicle from stock
- performance improvements
- donor-part adaptation
- installing non-stock assemblies
- tuning altered behavior

Primary homes:
- `work/`
- `diagnostics/` when fault isolation is required after the modification
- `sourcing/` when the decision is mainly about what to buy or pull

## Rule
Modified-state topics may cite stock baseline files, but they may not replace them as the canonical stock source.

---

# 5. Work-type routing

When a topic belongs in `work/`, route by work class before routing by system.

## Work classes
- `maintenance/` for service and refresh work
- `repairs/` for fixing failed or damaged stock components
- `restoration/` for stock-correct or preservation-oriented work
- `upgrades/` for improved non-stock outcomes that retain the same core system role
- `swaps/` for major donor or architecture changes
- `inspections/` for baseline checks and condition assessment
- `setup-and-calibration/` for adjustment and configuration tasks

## Examples
- thermostat replacement as routine refresh → `work/maintenance/cooling/`
- radiator replacement after failure → `work/repairs/cooling/`
- alternator output improvement → `work/upgrades/electrical/`
- LS engine conversion → `work/swaps/drivetrain/`
- idle calibration after ECU conversion → `work/setup-and-calibration/` or swap-specific subtree

---

# 6. Procedure vs troubleshooting vs sourcing routing

These are often adjacent but must remain distinct.

## If the user asks “how do I install or replace it?”
Route to:
- `work/`

## If the user asks “why is it doing this?”
Route to:
- `diagnostics/`

## If the user asks “which one should I use?”
Route to:
- `sourcing/`

## If the user asks “what did Jeep use from the factory?”
Route to:
- `vehicle/`

## Mixed-question rule

If a question mixes types, answer from the dominant task and pull supporting files from the other domains.

Example:
- “Which alternator upgrade should I buy, and how do I install it?”
  - primary: `sourcing/`
  - secondary: `work/upgrades/electrical/`

Example:
- “Why does my WJ brake swap pull right after installation?”
  - primary: `diagnostics/brakes/`
  - secondary: `work/upgrades/brakes/wj-brake-upgrade/`

---

# 7. Compatibility routing

Compatibility should be loaded only when it changes the answer materially.

## Common compatibility dimensions
- year
- era
- engine family
- transmission type
- 2WD vs 4WD
- ABS vs non-ABS
- package or trim
- axle family
- donor family
- emissions architecture

## Compatibility rule

Load the compatibility dimension closest to the affected topic.
Do not load broad year documents if a narrower system-specific compatibility file already exists.

## Example
Question: “Will this SYE path work on my 231-equipped 1998 automatic XJ?”

Load order:
1. `work/upgrades/driveline/sye/overview.md`
2. local `compatibility.md` for the SYE branch
3. `vehicle/systems/transfer-case/` only if baseline transfer-case truth is needed
4. `vehicle/years/` only if the year materially changes the answer

---

# 8. Overview routing vs leaf routing

## Use an overview file when you need to:
- identify branch scope
- understand major variants
- choose between multiple leaves
- find the compatibility split before reading details

## Use a leaf file when you need to:
- answer one narrow technical question
- perform one bounded procedure
- isolate one symptom path
- inspect one compatibility constraint

## Rule
Do not answer from an overview when a leaf is the real source of truth.
Overviews route. Leaves decide.

---

# 9. Cross-domain routing rules

Some topics require more than one domain.
Use one domain as primary and the rest as support.

## Pattern
- primary domain = where the main question lives
- supporting domains = where baseline, troubleshooting, or sourcing context lives

## Common cross-domain patterns

### Stock fact + procedure
Example: cooling system refresh
- primary: `work/maintenance/cooling/`
- support: `vehicle/systems/cooling/`

### Procedure + sourcing
Example: alternator upgrade
- primary: `work/upgrades/electrical/`
- support: `sourcing/interchange/electrical/`

### Procedure + diagnostics
Example: poor results after a brake upgrade
- primary: `diagnostics/brakes/`
- support: `work/upgrades/brakes/`

### Stock fact + swap planning
Example: LS swap planning
- primary: `work/swaps/drivetrain/`
- support: `vehicle/configurations/`, `sourcing/donor-vehicles/`

### Stock fact + ECU conversion
Example: ECU swap wiring
- primary: `work/swaps/ecu/wiring/`
- support: `vehicle/years/<era>/wiring.md` during transition

---

# 10. Present-state transitional routing

The repo is not fully migrated yet.
Agents must route using the target model while respecting current canonical files.

## Current canonical roots
- `vehicle/`
- `swap/`
- `book/`
- `agents/`

## Transitional meaning
- current `swap/` is the active canonical branch for what will later become part of `work/swaps/ecu/`
- current era folders under `vehicle/era1`, `vehicle/era2`, and `vehicle/era3` are the active canonical year-based fact trees

## Transitional routing rule

If the target-state path does not exist yet, route to the current canonical branch that maps to it most closely.

### Mapping examples
- target `work/swaps/ecu/wiring/` → current `swap/wiring/`
- target `work/swaps/ecu/tuning/` → current `swap/tuning/`
- target `vehicle/years/era1/` → current `vehicle/era1/`
- target `vehicle/years/era3/1996-notes.md` → current `vehicle/era3/1996-notes.md`

## Guardrail
Do not invent new canonical destinations inside legacy folders if the topic clearly belongs to a future non-swap domain.
For new non-swap topics, prefer the target-state taxonomy in planning and governance.

---

# 11. Routing matrix

Use this matrix to classify new and existing questions.

| Question form | Primary domain | Typical branch |
|---|---|---|
| What did Jeep use? | `vehicle/` | `years/`, `systems/`, `packages/` |
| How do I service it? | `work/` | `maintenance/` |
| How do I fix it? | `work/` | `repairs/` |
| How do I restore it? | `work/` | `restoration/` |
| How do I improve it? | `work/` | `upgrades/` |
| How do I replace the architecture? | `work/` | `swaps/` |
| Why is it failing? | `diagnostics/` | system branch |
| Which part or donor should I use? | `sourcing/` | `interchange/`, `donor-vehicles/`, `oem-vs-aftermarket/` |
| How should this be written? | `book/` | writing branch |
| How should the repo evolve? | `docs/` / `skillbuilding/` | taxonomy or framework branch |

---

# 12. Routing examples

## Renix sensor baseline
- primary: `vehicle/`
- branch: era-based fact tree during transition
- current route: `vehicle/era1/overview.md` + relevant sensor leaf when it exists

## AW4 transmission behavior
- primary: `vehicle/`
- current route: `vehicle/trans/aw4.md`
- target route: `vehicle/systems/transmission/aw4/overview.md`

## Dana 30 axle swap options
- stock baseline: `vehicle/`
- donor choices: `sourcing/`
- swap procedure: `work/swaps/axles/`

## Chrysler 8.25 upgrade notes
- primary: `work/upgrades/axles/`
- support: `vehicle/systems/axles/chrysler-8.25/`

## WJ brake upgrade
- primary: `work/upgrades/brakes/`
- support: `sourcing/interchange/brakes/`, `vehicle/systems/brakes/`

## Cooling system refresh
- primary: `work/maintenance/cooling/`
- support: `vehicle/systems/cooling/`

## Alternator upgrade
- primary: `work/upgrades/electrical/`
- support: `sourcing/interchange/electrical/`, `vehicle/systems/charging-starting/`

## Fuel pump diagnostics
- primary: `diagnostics/fuel/`
- support: `vehicle/systems/fuel/`

## Headliner repair
- primary: `work/repairs/interior/`

## Door wiring issues
- primary: `diagnostics/body-electrical/`
- support: `vehicle/systems/electrical/body-wiring/`

## Suspension lift geometry
- primary: `work/upgrades/suspension/`
- support: `vehicle/systems/suspension/`

## Steering box swap
- primary: `work/swaps/steering/`
- support: `sourcing/interchange/steering/`

## LS swap planning
- primary: `work/swaps/drivetrain/`
- support: `sourcing/donor-vehicles/drivetrain/`, `vehicle/configurations/`

## ECU swap wiring
- primary target: `work/swaps/ecu/wiring/`
- current canonical route: `swap/wiring/`
- support: relevant era wiring files in `vehicle/`

## Transfer case SYE upgrade
- primary: `work/upgrades/driveline/`
- support: `vehicle/systems/transfer-case/`, `diagnostics/driveline/`

---

# 13. Rules for adding new routing indexes

Create a new local router only when:
- a folder has multiple durable child topics
- the child topics need compatibility guidance
- the branch would otherwise be ambiguous for new agents

A router should:
- define scope
- list child branches
- explain major splits
- point to the narrowest likely next files

A router should not:
- become a full technical treatise
- duplicate all leaf content
- hold orphaned facts that belong in leaves

---

# 14. Anti-patterns

Avoid these routing failures:

1. **Folder by convenience**
   - placing content in the nearest existing folder instead of the correct domain

2. **Procedure in fact files**
   - hiding install steps under `vehicle/`

3. **Troubleshooting in sourcing files**
   - turning a parts comparison into a symptom tree

4. **Agent prompt drift**
   - storing canonical facts in `agents/`

5. **Mega-overview drift**
   - using `index.md` or `overview.md` as the real long-form source

6. **Compatibility smear**
   - repeating year caveats in many files instead of attaching them near the relevant branch and linking to the canonical year baseline

7. **Legacy-root inertia**
   - forcing all future work into `swap/` because it already exists

---

# 15. Summary

The routing model is:
1. classify the question type
2. choose the owning domain
3. determine stock vs modified
4. route by system or work class
5. load compatibility only if it changes the answer
6. use overview files to choose branches
7. answer from leaf files whenever possible
8. use current canonical roots during transition, but design future placement according to the target taxonomy
