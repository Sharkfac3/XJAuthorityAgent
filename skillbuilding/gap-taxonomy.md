# Gap Taxonomy

Use this file to classify **likely or confirmed knowledge gaps** in the XJ ECU swap project.

This taxonomy is for project-building work.
It does not claim a gap is real until an audit confirms it.

## Purpose
The repo needs a stable way to talk about missing information before and after audits.
This taxonomy gives agents and humans a shared checklist for:
- expected weak areas
- swap impact
- evidence standards
- likely canonical destinations

## Two states of a gap
- **likely gap** — a planning hypothesis based on domain expectations
- **confirmed gap** — a weakness verified by reviewing repo content

Do not treat likely gaps as proof that the repo is missing something.
Use them to drive audits and research.

## Gap status labels
- `likely`
- `confirmed`
- `resolved`
- `deferred`

## Gap type labels
- `missing` — no usable coverage exists
- `partial` — some coverage exists but not enough
- `unclear` — wording or scope is too ambiguous to trust
- `unverified` — claims exist but evidence is weak or absent
- `misplaced` — useful content exists in the wrong file/folder
- `conflicting` — multiple claims disagree materially

## Swap impact labels
- `swap-blocking` — the user cannot proceed safely or correctly
- `swap-risking` — the user may proceed but could misconfigure, miswire, damage parts, or waste time
- `trust-reducing` — not fatal, but weakens confidence in the repo
- `quality-of-life` — helpful improvement, low urgency

## Confidence labels for future findings
- `confirmed`
- `strongly supported`
- `plausible`
- `provisional`
- `conflicting`
- `unknown`

## Core likely gap categories

### 1. Stock-system identification gaps
Questions about what the Jeep has now.

Examples:
- ECU family identification
- ignition architecture identification
- year/era split confirmation
- special-case year detection

Likely canonical destinations:
- `vehicle/engine.md`
- `vehicle/eraX/overview.md`
- `vehicle/era3/1996-notes.md`

### 2. Year/era exception gaps
Questions where a broad era rule may have one or more exceptions.

Examples:
- 1996 transition behavior
- early/late connector or sensor changes
- ignition changes within an era

Likely canonical destinations:
- era note files under `vehicle/eraX/`
- dedicated year-range exception files when needed

### 3. Sensor and calibration gaps
Questions about sensor type, scaling, compatibility, and reuse.

Examples:
- MAP sensor scaling
- CLT/CTS and IAT calibration data
- TPS signal expectations
- O2 strategy differences
- idle valve compatibility

Likely canonical destinations:
- `vehicle/eraX/sensors/<sensor>.md`
- `swap/ecu-selection/` when compatibility affects ECU choice
- `swap/tuning/` when configuration procedure is the main issue

### 4. Trigger and ignition gaps
Questions about crank/cam patterns, decoder naming, sync strategy, and ignition hardware.

Examples:
- exact trigger pattern description
- crank-only vs crank/cam
- distributor vs coil rail implications
- platform-specific decoder naming

Likely canonical destinations:
- `vehicle/eraX/trigger.md`
- `vehicle/era3/ignition/*.md`
- `swap/tuning/ignition.md`

### 5. Injector and fueling data gaps
Questions about injector size, impedance, dead time, and fitment assumptions.

Examples:
- stock injector specs by era
- base fuel assumptions for first start
- dead time uncertainty

Likely canonical destinations:
- `vehicle/eraX/injectors.md`
- `swap/tuning/first-start.md`

### 6. Wiring architecture gaps
Questions about harness-level integration strategy.

Examples:
- what stock wiring can remain
- what must be rebuilt
- shielded signal handling
- branch planning and serviceability

Likely canonical destinations:
- `swap/wiring/harness.md`
- era `wiring.md` files

### 7. Connector and pinout gaps
Questions about connector family, pin count, keying, sourcing, and repinning.

Examples:
- missing pinouts
- unclear family identification
- unavailable OEM connectors and modern equivalents
- repin hazards

Likely canonical destinations:
- `swap/wiring/connectors/index.md`
- leaf files under `swap/wiring/connectors/`

### 8. Power, relay, and grounding gaps
Questions about power architecture that must be preserved or replicated.

Examples:
- relay behavior
- switched power architecture
- ECU/sensor/injector ground strategy
- starter/crank interaction assumptions

Likely canonical destinations:
- `vehicle/eraX/power-relay.md`
- `swap/wiring/grounds.md`
- `swap/wiring/harness.md`

### 9. Transmission integration gaps
Questions where transmission operation changes swap planning.

Examples:
- AW4 TPS coexistence
- TCU retained inputs
- automatic/manual split in procedures

Likely canonical destinations:
- `vehicle/trans/aw4.md`
- `vehicle/trans/manual.md`
- `swap/wiring/aw4-tps.md`

### 10. ECU platform comparison gaps
Questions about what aftermarket ECU fits the XJ use case.

Examples:
- trigger compatibility
- idle control support
- IO constraints
- logging/tuning practicality
- cost/support tradeoffs

Likely canonical destinations:
- `swap/ecu-selection/requirements.md`
- platform files under `swap/ecu-selection/`

### 11. First-start and base-config gaps
Questions that affect safe first crank and initial running.

Examples:
- pre-start verification steps
- required constants
- ignition sync checks
- fuel-pressure sanity checks

Likely canonical destinations:
- `swap/tuning/first-start.md`
- `swap/tuning/ignition.md`
- era `trigger.md` and `injectors.md`

### 12. Troubleshooting and validation gaps
Questions about how to diagnose failure after the swap begins.

Examples:
- no-start flow
- sync loss diagnosis
- sensor plausibility checks
- idle instability triage

Likely canonical destinations:
- `swap/tuning/` leaf docs
- possibly future troubleshooting files under `swap/`

### 13. Safety and reliability gaps
Questions where missing warnings or reliability context could cause harm or poor design choices.

Examples:
- live-circuit work warnings
- fuel-system safety
- public-road WOT cautions
- trail reliability implications

Likely canonical destinations:
- `book/writing/safety.md`
- relevant `swap/` procedure files

### 14. Beginner-explanation gaps
Questions where the technical facts may be present but still unusable for the target reader.

Examples:
- undefined acronyms
- unexplained terms
- missing “why before how” context
- skipped decision logic

Likely canonical destinations:
- `book/audience.md`
- `book/writing/style.md`
- specific `swap/` or `vehicle/` leaf files being clarified

## Category questions to ask
For any gap, ask:
1. Is this about the stock Jeep or the swap?
2. Is it universal, era-specific, or year-specific?
3. What wrong decision could happen if this stays unclear?
4. What evidence level should this topic require?
5. What is the narrowest truthful canonical destination?

## Use with other skillbuilding files
- likely high-value areas → `skillbuilding/critical-unknowns.md`
- evidence requirements → `skillbuilding/evidence-standards.md`
- individual gap profiling → `skillbuilding/templates/likely-gap-profile.md`
