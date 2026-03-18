# Domain Map

Use this file as the high-level map of the **Jeep XJ ECU swap knowledge surface** the repo is trying to cover.

## Purpose
The project already has gap taxonomy, evidence rules, source policy, lifecycle, and file maturity standards.
What this file adds is a map of the actual domain those tools operate on.

This file answers:
- what major knowledge areas exist in an XJ ECU swap project
- how those areas relate to the swap workflow
- which areas are stock-system facts vs swap procedures vs presentation concerns
- where answers should usually live canonically

## Important boundary
This file is a coverage map, not canonical Jeep fact storage.
It should describe domains, decisions, and destinations — not duplicate detailed technical content from `vehicle/`, `swap/`, or `book/`.

## Primary organizing principle
The main project axis is the swap workflow:
1. identify what is in the Jeep now
2. decide on a swap strategy
3. wire it correctly
4. configure it for first start
5. tune and validate it
6. keep it reliable and understandable for the reader

Era splits support the workflow.
They are not the end goal by themselves.

## Domain layers

### Layer 1 — Stock Jeep identification
This layer answers: **what system is already in the vehicle?**

Key domains:
- engine baseline
- ECU family by era
- ignition architecture by era/year
- stock sensor set
- stock injector baseline
- stock power and relay behavior
- transmission type and constraints
- year-specific exceptions

Typical canonical destinations:
- `vehicle/engine.md`
- `vehicle/eraX/overview.md`
- `vehicle/eraX/trigger.md`
- `vehicle/eraX/injectors.md`
- `vehicle/eraX/power-relay.md`
- `vehicle/eraX/wiring.md`
- `vehicle/eraX/sensors/*.md`
- `vehicle/trans/*.md`
- dedicated year-exception files

Typical user decisions supported:
- Which stock ECU family do I have?
- Which ignition setup is in my Jeep?
- Which year/era caveats apply before I plan the swap?

## Layer 2 — Swap strategy selection
This layer answers: **what aftermarket ECU approach makes sense for this Jeep and this owner?**

Key domains:
- ECU platform requirements
- platform comparison for XJ use
- idle control strategy
- wideband and closed-loop prerequisites
- required supporting hardware
- tradeoffs in complexity, cost, and supportability

Typical canonical destinations:
- `swap/ecu-selection/requirements.md`
- platform files under `swap/ecu-selection/` (e.g. `speeduino.md`, `rusefi.md`)
- variant files under `swap/ecu-selection/` (e.g. `speeduino-ocelot.md`) — load alongside the platform file when a specific board is chosen
- `swap/ecu-selection/iac-strategy.md`
- `swap/ecu-selection/wideband.md`

Typical user decisions supported:
- Which platform best fits this XJ?
- What hardware is mandatory vs optional?
- What compromises am I accepting with this platform?

## Layer 3 — Wiring and physical integration
This layer answers: **how does the aftermarket ECU physically and electrically fit into the Jeep?**

Key domains:
- harness reuse vs replacement strategy
- grounding strategy
- power distribution and relay replication
- connector families and pinouts
- sensor wiring integration
- ignition wiring integration
- transmission-related retained circuits
- serviceability and trail-repair considerations

Typical canonical destinations:
- `swap/wiring/harness.md`
- `swap/wiring/grounds.md`
- `swap/wiring/connectors/`
- `swap/wiring/aw4-tps.md`
- era `wiring.md`
- era `power-relay.md`

Typical user decisions supported:
- What stock wiring can stay?
- What must be replicated exactly?
- Which connectors can I reuse or replace?
- What extra wiring is needed for AW4 or ignition changes?

## Layer 4 — ECU configuration for first start
This layer answers: **what settings and checks are needed before and during first crank?**

Key domains:
- trigger setup
- ignition sync setup
- injector constants and base fueling
- sensor calibration and validation
- idle strategy setup
- pre-start checklist
- software-side vs vehicle-side verification

Typical canonical destinations:
- `swap/tuning/first-start.md`
- `swap/tuning/ignition.md`
- `swap/tuning/idle-tuning.md`
- era `trigger.md`
- era `injectors.md`
- era sensor leaf files

Typical user decisions supported:
- Is my configuration safe enough to crank?
- Are my trigger and timing assumptions correct?
- Are the sensors and injectors configured plausibly?

## Layer 5 — Tuning and validation
This layer answers: **how do I move from running to reliable and well-behaved?**

Key domains:
- VE table development
- AFR target strategy
- open-loop vs closed-loop behavior
- ignition advance refinement
- WOT safety and tuning limits
- drivability refinement
- trail-use tuning priorities
- transmission behavior under tuning changes

Typical canonical destinations:
- `swap/tuning/ve-table.md`
- `swap/tuning/afr-targets.md`
- `swap/tuning/closed-loop.md`
- `swap/tuning/wot-tuning.md`
- `swap/tuning/trail-tuning.md`
- `vehicle/trans/aw4.md` when interaction matters

Typical user decisions supported:
- What should I tune first?
- What is safe enough for the street or trail?
- How do tuning choices affect drivability and transmission behavior?

## Layer 6 — Troubleshooting and ongoing validation
This layer answers: **what do I do when it does not work as expected?**

Key domains:
- no-start diagnosis
- sync-loss diagnosis
- sensor plausibility checks
- idle instability diagnosis
- fuel/timing sanity checks
- post-change validation routines
- recurring failure modes

Typical canonical destinations:
- existing `swap/tuning/` docs where applicable
- possible future troubleshooting docs under `swap/`
- supporting era and sensor files under `vehicle/`

Typical user decisions supported:
- Why will it not start?
- Which system is lying to me?
- Is this a wiring issue, config issue, or hardware issue?

## Layer 7 — Reliability, safety, and reader usability
This layer answers: **how do we make the information safe, trustworthy, and usable by the intended audience?**

Key domains:
- safety warnings before risky steps
- reliability implications of design choices
- beginner-appropriate explanations
- acronym expansion and terminology control
- why-before-how writing pattern
- automatic vs manual callouts
- year/era caveat visibility

Typical canonical destinations:
- `book/audience.md`
- `book/writing/style.md`
- `book/writing/callouts.md`
- `book/writing/safety.md`
- affected `swap/` and `vehicle/` files

Typical user decisions supported:
- Do I understand this well enough to proceed?
- Which choices improve reliability instead of just functionality?
- What warning applies before I do this step?

## Cross-cutting XJ-specific problem areas
These domains span multiple workflow layers and deserve special attention.

### 1. Era and year-range management
Examples:
- Renix vs SBEC vs JTEC differences
- 1996 transition behavior
- late-era ignition changes

Why it matters:
- wrong year assumptions corrupt otherwise-correct guidance

### 2. AW4 automatic transmission interaction
Examples:
- TPS coexistence
- retained TCU inputs
- tuning interactions

Why it matters:
- the engine can run while the vehicle still behaves badly

### 3. Trigger and ignition interpretation
Examples:
- decoder naming
- sync strategy
- distributor vs coil-rail implications

Why it matters:
- these are swap-critical and error-sensitive

### 4. Connector and harness reality
Examples:
- connector sourcing
- repin hazards
- aging harness condition
- serviceability after modification

Why it matters:
- theoretical guidance fails if the physical integration path is vague

### 5. Beginner comprehension of ECU concepts
Examples:
- calibration terminology
- sensor concepts
- table-based tuning ideas
- avoiding assumed ECU literacy

Why it matters:
- technically correct content can still fail the actual reader

## Domain-to-folder routing rules
Use these quick rules when mapping a topic.

- If it describes what the Jeep came with → `vehicle/`
- If it explains how to make the swap work → `swap/`
- If it controls presentation, safety language, or reader guidance → `book/`
- If it governs audits, planning, validation workflow, or maturity → `skillbuilding/`
- If it governs repo taxonomy or maintenance policy → `docs/`

## Domain map and gap work
Use this file together with:
- `skillbuilding/gap-taxonomy.md` to classify weakness type
- `skillbuilding/critical-unknowns.md` to focus on likely high-risk areas
- `skillbuilding/prioritization-rubric.md` to rank what to build next
- `skillbuilding/file-maturity.md` to judge whether a mapped area is mature enough

## Practical use
Use this file when:
- planning a full repo audit
- deciding whether a new file is justified
- checking whether a workflow stage lacks supporting docs
- converting vague ideas into structured backlog items
- deciding where a new topic belongs canonically

## Non-goals
This file should not:
- become an encyclopedia of Jeep facts
- replace `swap/index.md` as the workflow router
- duplicate leaf-file technical details
- justify creating files that do not help the actual swap workflow
