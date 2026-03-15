# Content Audit

This audit is meant to reduce accidental overlap without removing useful Jeep/XJ context.

## Summary
The current content is mostly well separated by purpose:
- `vehicle/` = stock Jeep/XJ facts needed to understand compatibility
- `swap/` = procedures and swap constraints
- `book/` = presentation guidance
- `agents/` = loading behavior

Most overlap appears intentional and useful for routing. Very little should be deleted.

## Intentional overlap to keep

### Era overview files
Files:
- `vehicle/era1/overview.md`
- `vehicle/era2/overview.md`
- `vehicle/era3/overview.md`

Why keep overlap:
- They provide a small identity summary for the era
- They link to leaf files so agents do not need to load an entire era folder
- They are the right place for high-level caveats like connector splits and 1996 transition notes

Constraint:
- Keep detailed specs in leaf files, not in overviews

### Routing overlap
Files:
- `AGENTS.md`
- `SKILL.md`
- `agents/*.md`
- `book/outline.md`

Why keep overlap:
- This overlap is routing metadata, not technical duplication
- It reduces token waste by helping agents load only the correct files

Constraint:
- These files should point to facts, not become fact stores themselves

### AW4 information split
Files:
- `vehicle/trans/aw4.md`
- `swap/wiring/aw4-tps.md`

Why keep overlap:
- `vehicle/trans/aw4.md` captures transmission behavior and system constraints
- `swap/wiring/aw4-tps.md` captures the swap procedure and wiring strategy

Constraint:
- Voltage expectations may appear in both, but stock behavior belongs in `vehicle/trans/aw4.md`
- swap implementation details belong in `swap/wiring/aw4-tps.md`

## Overlap risks to watch

### Sensor structure is complete but easy to bloat
Files under:
- `vehicle/era1/sensors/`
- `vehicle/era2/sensors/`
- `vehicle/era3/sensors/`

Risk:
- repeating large generic sensor explanations in every era file

Recommended rule:
- keep each sensor file focused on era-specific spec, connector, calibration, and caveats
- if a generic explanation becomes necessary later, place it in a clearly named shared reference file and keep era deltas in the era file

### Connector content can drift from stock-era wiring files
Files under:
- `swap/wiring/connectors/`
- `vehicle/era*/wiring.md`

Risk:
- same connector detail being stated in multiple places with different wording

Recommended rule:
- stock harness architecture belongs in `vehicle/era*/wiring.md`
- connector family and physical connector identification belong in `swap/wiring/connectors/`
- era wiring files may reference connector family names, but should avoid full connector specs unless necessary

## Known factual tension found during audit

### Ignition wording across cross-era and era-specific files
Files:
- `vehicle/engine.md`
- `vehicle/era2/overview.md`
- `vehicle/era3/overview.md`

Issue:
- `vehicle/engine.md` says the ECU does not fire the coil directly in any era and points to era-specific architecture
- era 2 and era 3 overview wording can be read as if the PCM directly drives the coil via the ASD relay

Interpretation:
- the ASD relay supplies ignition power; it is not itself the ignition driver
- this is a wording-consistency issue, not a signal to remove context

Action:
- normalize wording so era overviews describe control architecture without oversimplifying ignition drive behavior

## Recommendation
Do not do broad deduplication.

Instead:
1. keep routing overlap
2. keep era overview summaries
3. keep year-specific exception files
4. only remove duplication when a detailed spec exists in more than one canonical technical file
