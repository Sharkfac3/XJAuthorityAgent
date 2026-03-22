# Project Reframe

## Target-state summary

This repository should become a long-term, agent-friendly Jeep XJ technical knowledge system, not only an ECU-swap knowledge base.

The Jeep XJ remains the platform anchor. ECU swaps remain an important domain, but they should sit as one branch inside a larger architecture that can support the full vehicle lifecycle:
- stock vehicle understanding
- maintenance and repair
- diagnostics and fault isolation
- restoration and preservation
- upgrades and modifications
- major system swaps
- parts interchange and sourcing
- model-year, package, and subsystem differences

The target state is a deeply structured Markdown knowledge base that:
- preserves canonical facts in predictable places
- separates facts from procedures, sourcing advice, troubleshooting, and presentation rules
- supports both stock and modified paths
- scales by adding deeper folders instead of overloading broad top-level files
- helps agents orient quickly with minimal session context

## Scope statement

This reframe covers the repository mission, information architecture, domain boundaries, routing model, and naming rules.

It does **not** perform the restructure itself. It does **not** move content yet. It does **not** flatten existing ECU-swap content into a new shape prematurely.

The immediate goal is to define a target architecture that can guide future migration without breaking the current repo during transition.

## New mission

Build a canonical Jeep XJ technical knowledge system for agents and humans that explains:
- what the XJ is, by year, era, package, and subsystem
- how to diagnose, maintain, repair, restore, modify, and swap major systems on the platform
- how stock configurations and modified configurations affect decisions
- how to route users and agents quickly to the narrowest truthful file

In short:

> Preserve Jeep XJ platform knowledge in a deep, agent-routable structure where ECU swaps are one major work domain rather than the defining center of the repo.

## Guiding principles

### 1. Keep the Jeep XJ as the platform anchor
The repo should stay centered on the XJ itself, not on one type of project.

### 2. Separate facts from actions
A fact about how a 1996 XJ is built is different from:
- a procedure for replacing a part
- a troubleshooting path for a symptom
- a sourcing recommendation
- a writing rule for presenting the answer

These must live in different domains.

### 3. Favor deep trees over crowded summary files
When a topic grows, split downward into narrower folders and leaf files. Do not keep expanding giant top-level indexes or catch-all documents.

### 4. Store knowledge in canonical content trees, not agent prompts
`agents/` should route and instruct. It should not become a shadow fact store.

### 5. Preserve year, era, package, and subsystem truth
Do not flatten meaningful differences for convenience. Narrow truth beats short files.

### 6. Support both stock and modified paths
The repo should explain stock baselines and modified outcomes without forcing one worldview.

### 7. Optimize for agent entry with low context cost
Agents should be able to enter cold, load one router, inspect the task domain, and then load only the needed leaves.

### 8. Keep canonical knowledge separate from governance/meta files
Technical knowledge belongs in knowledge domains. Taxonomy rules, audits, and migration planning belong in `docs/` and `skillbuilding/`.

### 9. Prefer expandable categories over vague buckets
Use durable categories such as `maintenance`, `diagnostics`, `swaps`, `upgrades`, `restoration`, and `sourcing` instead of catch-all names like `misc`, `notes`, or `general`.

### 10. Let compatibility live close to the affected topic
Compatibility should be attached to the system or task where it matters, with clear links back to year/era/package facts.

## Proposed top-level architecture

The current repo already has useful separation logic. The target state should expand that logic rather than discard it.

```text
agents/          Agent behavior, routing, loading guidance
book/            Presentation-layer rules for human-facing output
diagnostics/     Symptom-based and test-path troubleshooting knowledge
docs/            Repo governance, taxonomy, migration, audits
sourcing/        Buying, parts selection, interchange, availability guidance
skillbuilding/   Meta-framework for expansion, audits, backlog, research intake
vehicle/         Canonical Jeep XJ platform facts
work/            Task/procedure domains for maintenance, repair, upgrades, swaps, restoration
```

### Why this architecture
- `vehicle/` remains the platform fact root and preserves continuity with the current repo.
- `work/` becomes the main action domain for doing things to the XJ.
- `diagnostics/` becomes its own problem-oriented domain instead of being buried only inside era notes or procedures.
- `sourcing/` becomes a dedicated domain for what to buy, reuse, avoid, or interchange.
- `book/`, `agents/`, `docs/`, and `skillbuilding/` retain their existing non-fact roles.

## Domain definitions

## 1. `vehicle/` — vehicle facts

Purpose: canonical facts about the Jeep XJ platform itself.

Use for:
- model-year and era differences
- engine, transmission, axle, brake, suspension, steering, cooling, fuel, electrical, body, and interior facts
- stock package differences
- factory configuration baselines
- known year-range hardware changes
- stock system architecture
- compatibility facts that describe what exists on the vehicle

Do not use for:
- step-by-step procedures
- symptom trees
- buying advice
- writing rules
- agent operating instructions

Target shape example:

```text
vehicle/
  overview.md
  years/
    era1/
    era2/
    era3/
    1996-notes.md
  systems/
    engine/
    fuel/
    ignition/
    cooling/
    electrical/
    transmission/
    transfer-case/
    axles/
    suspension/
    steering/
    brakes/
    body/
    interior/
  packages/
  interchange-baselines/
```

Note: existing era-based material can remain valuable, but the future shape should allow both year-based and system-based access paths.

## 2. `work/` — procedures and project execution

Purpose: explain how to perform jobs on or to the XJ.

Use for:
- maintenance procedures
- repair procedures
- restoration work
- upgrades
- swaps
- installation workflows
- adjustment and setup procedures
- validation steps after work

Do not use for:
- platform facts with no action context
- symptom-first diagnosis trees
- buying-only guidance

Target shape example:

```text
work/
  maintenance/
  repairs/
  restoration/
  upgrades/
    suspension/
    brakes/
    steering/
    cooling/
    electrical/
  swaps/
    ecu/
    drivetrain/
    axle/
  inspections/
  setup-and-calibration/
```

## 3. `diagnostics/` — troubleshooting and fault isolation

Purpose: help users identify problems from symptoms, tests, and observations.

Use for:
- no-start diagnosis
- overheating diagnosis
- charging-system faults
- brake pull/vibration diagnosis
- driveline vibration diagnosis
- sensor plausibility checks
- symptom trees, decision trees, and test sequences

Do not use for:
- generic system facts
- full replacement procedures unless linked as next-step actions
- buying recommendations except as a small supporting note

Target shape example:

```text
diagnostics/
  engine/
  fuel/
  ignition/
  cooling/
  charging-and-starting/
  transmission/
  driveline/
  steering-and-suspension/
  brakes/
  body-electrical/
```

## 4. `sourcing/` — buying, parts, interchange, and selection guidance

Purpose: support decisions about what parts, donors, kits, brands, connectors, or assemblies to acquire.

Use for:
- parts interchange guidance
- donor compatibility notes
- aftermarket option comparisons
- replacement-part selection criteria
- risk notes on unknown-quality parts
- sourcing constraints by year or subsystem

Do not use for:
- canonical stock facts unless needed as a referenced baseline
- complete installation procedures
- general writing standards

Target shape example:

```text
sourcing/
  interchange/
  oem-vs-aftermarket/
  donor-vehicles/
  connectors/
  swap-kits/
  wear-items/
```

## 5. `book/` — presentation rules

Purpose: define how human-facing output should be structured and written.

Use for:
- audience definition
- style rules
- callout conventions
- safety language
- chapter or deliverable structure

Do not use for:
- technical facts
- troubleshooting logic
- procedures
- agent routing logic

## 6. `agents/` — behavior and routing

Purpose: tell agents how to orient, what to load, and how to behave.

Use for:
- entrypoint indexes
- role definitions
- task routing rules
- load-by-task instructions
- review behavior

Do not use for:
- new technical fact storage
- duplicate procedures
- hidden canonical knowledge

## 7. `docs/` and `skillbuilding/` — governance and expansion system

Purpose:
- `docs/` holds taxonomy, migration planning, architecture rules, and audits.
- `skillbuilding/` holds meta workflows for hardening the repo, identifying gaps, normalizing research, and planning expansion.

These are not primary Jeep fact domains.

## Major content domains the repo should cover

The future system should be able to cover at least these major branches:

### Platform and configuration
- year/era differences
- trim, package, drivetrain, and emissions differences
- stock subsystem architecture
- factory hardware changes over time

### Maintenance
- fluids, filters, tune-up items
- scheduled service
- wear-item replacement
- baseline inspections

### Repairs
- cooling repairs
- electrical repairs
- fuel and ignition repairs
- brake repairs
- drivetrain repairs
- body/interior repairs

### Diagnostics
- symptom-based troubleshooting
- test workflows
- fault isolation
- pre-repair verification and post-repair validation

### Upgrades
- suspension upgrades
- brake upgrades
- steering upgrades
- electrical system improvements
- cooling upgrades
- lighting upgrades

### Swaps
- ECU swaps
- drivetrain swaps
- axle swaps
- transfer-case changes
- charging/fuel/ignition architecture conversions

### Restoration
- stock restoration paths
- trim/body/interior restoration
- wiring restoration
- factory-correct decisions vs practical service choices

### Sourcing and interchange
- donor parts
- interchangeable components
- OEM vs aftermarket considerations
- connector and harness sourcing
- package-specific or year-specific fitment traps

## Quick orientation model for agents

Agents entering cold should be able to orient in a repeatable sequence.

### Recommended entry sequence
1. Read `SKILL.md`
2. Read `AGENTS.md`
3. Inspect top-level structure
4. Determine the question type:
   - platform fact
   - work procedure
   - diagnosis
   - sourcing decision
   - writing/presentation
   - repo governance/meta
5. Load only the domain router and leaf files needed for that task

### Fast classification questions
An agent should ask:
- Is the user asking what the XJ has? → `vehicle/`
- Is the user asking how to do a job? → `work/`
- Is the user asking what is wrong and how to isolate it? → `diagnostics/`
- Is the user asking what part, donor, or kit to buy/use? → `sourcing/`
- Is the user asking how to present the answer? → `book/`
- Is the user asking how the repo should evolve? → `docs/` and `skillbuilding/`

### Routing rule
Agent files should stay small and act as routers. They should point to canonical domains rather than restating facts.

## What should remain from the current structure

The current repo already contains several strong patterns worth preserving.

### Keep
- `AGENTS.md` as the primary cross-agent entrypoint
- `SKILL.md` as the pi-facing root entrypoint
- the distinction between canonical knowledge and governance/meta files
- the rule that narrow, truthful leaf files beat broad summaries
- `vehicle/` as the canonical fact root, at least through migration
- `book/` as presentation-only guidance
- `agents/` as behavior/routing only
- `docs/` for taxonomy and migration planning
- `skillbuilding/` for expansion planning and repo-hardening workflows
- the current emphasis on year/era truth and token discipline

## What should change

### Change in project identity
The repo should stop presenting itself primarily as an ECU-swap book project and start presenting itself as a Jeep XJ technical knowledge system.

### Change in primary workflow axis
`swap/` should no longer define the whole repo. It should become one branch inside a broader work architecture.

### Change in domain breadth
The repo should grow to include:
- maintenance
- repairs
- diagnostics
- upgrades
- restoration
- sourcing/interchange
- broader platform systems beyond engine control

### Change in navigation model
Future routing should begin by classifying the request type, not by assuming every path leads to ECU swap execution.

### Change in folder strategy
As the repo expands, new domains should be added as deep trees with local indexes instead of making `vehicle/` and `swap/` absorb all new content.

## Naming principles for scalable folder and file design

### 1. Use nouns for domains, verbs sparingly for procedures
Good folder names:
- `cooling/`
- `brakes/`
- `diagnostics/`
- `maintenance/`
- `swaps/`

Good leaf names:
- `overview.md`
- `bleeding.md`
- `fan-control.md`
- `no-start.md`
- `donor-compatibility.md`

### 2. Avoid vague buckets
Avoid names like:
- `misc/`
- `general.md`
- `notes.md`
- `stuff.md`
- `other.md`

### 3. Put scope in the path, not only in prose
Prefer:
- `vehicle/systems/cooling/fan-types.md`
- `diagnostics/cooling/overheating-at-idle.md`
- `work/upgrades/brakes/wj-knuckle-swap/overview.md`

Instead of broad files that mix all three.

### 4. Keep indexes small and routing-focused
`index.md` and `overview.md` files should summarize, classify, and link. They should not become hidden mega-docs.

### 5. Encode stable distinctions in folder names
Examples:
- `stock/` vs `modified/` where needed
- `era1/`, `era2/`, `era3/`
- `front/` vs `rear/`
- `manual/` vs `automatic/`

### 6. Use year- or package-specific files when the difference is real
Prefer a dedicated file over repeated caveats across many files.

### 7. Keep file names descriptive and durable
Choose names that will still make sense after the tree grows deeper.

## Migration implications

This reframe implies a staged migration rather than a sudden rewrite.

### Near-term
- keep the current structure intact
- add this reframe document as the target-state reference
- continue using current ECU-swap content as canonical where it already exists
- avoid adding major new non-swap content into `swap/` just because it is the closest existing folder

### Mid-term
- create new top-level domains for `work/`, `diagnostics/`, and `sourcing/`
- add small routing indexes for those domains
- begin placing new non-swap content into those new domains
- update `AGENTS.md` to classify tasks by domain type before loading content

### Longer-term
- migrate ECU-swap execution content from `swap/` into `work/swaps/ecu/`
- leave temporary redirect/index files as needed during transition
- expand `vehicle/` from mostly era-centric swap support into a fuller platform fact tree
- align all agents to the broader domain model

### Current `swap/` implication
`swap/` should be treated as a legacy-but-still-canonical branch during migration. It remains useful now, but it should eventually resolve into a narrower place in the architecture instead of continuing to define the repo's whole identity.

## Risks to avoid

### 1. Turning agent files into fact stores
If agents start carrying technical truth in prompt files, the repo will drift and duplicate.

### 2. Flattening everything into giant summary docs
This makes growth harder, weakens routing, and increases token waste.

### 3. Keeping all future work under `swap/`
That would preserve the current distortion and make non-swap content feel secondary or awkward.

### 4. Mixing sourcing, diagnosis, and procedures into the same files
These are related but distinct jobs. Combining them creates ambiguity and poor reuse.

### 5. Losing year/package specificity
The XJ platform has meaningful splits. Broad statements should not erase those differences.

### 6. Letting `docs/` become the real knowledge base
Governance docs should describe the structure, not replace canonical technical content.

### 7. Creating too many shallow top-level categories too early
A few durable top-level roots with deep expansion underneath are better than a cluttered root.

### 8. Renaming everything before the routing model is stable
The conceptual model should be established first. File moves should follow clear migration rules.

## How ECU swap content fits in the broader system

ECU swap content remains important, but it becomes one major branch rather than the trunk.

### Example 1: stock sensor fact vs swap wiring step
- Stock CPS signal behavior belongs in `vehicle/`
- How to adapt that signal to an aftermarket ECU belongs in `work/swaps/ecu/` or the current `swap/` branch during migration

### Example 2: overheating after an ECU swap
- stock cooling system design facts belong in `vehicle/systems/cooling/`
- generic overheating diagnosis belongs in `diagnostics/cooling/`
- swap-specific fan-control integration belongs in `work/swaps/ecu/`
- fan relay or controller sourcing advice belongs in `sourcing/`

### Example 3: AW4 interaction with an ECU project
- AW4 stock behavior belongs in `vehicle/`
- diagnosing odd shift behavior belongs in `diagnostics/transmission/`
- TPS interface strategy for an ECU conversion belongs in `work/swaps/ecu/`
- choosing a compatible sensor or adapter belongs in `sourcing/`

### Example 4: a full drivetrain build path
A future drivetrain project might need:
- engine and trans baseline facts from `vehicle/`
- donor and fitment decisions from `sourcing/`
- swap procedure documents from `work/swaps/drivetrain/`
- startup or drivability troubleshooting from `diagnostics/`
- presentation rules from `book/`

That is the model the broader repo should enable.

## Practical target-state summary

The future repository should read as:
- a Jeep XJ platform knowledge base first
- a multi-domain technical work system second
- a collection of agent entrypoints and writing rules in support of that knowledge

The strongest parts of the current repo to preserve are:
- disciplined routing
- narrow canonical files
- clear fact/procedure separation
- year-aware structure

The main change is architectural scope:
- from an ECU-swap-centered knowledge base
- to a full Jeep XJ technical knowledge system where ECU swap content is one specialized branch inside a much larger tree
