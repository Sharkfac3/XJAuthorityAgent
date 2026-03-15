# Knowledge Expansion Strategy

This project should expand around swap-critical unknowns, not around model years as an end in themselves.

## Guiding principle
The era split stays.
It is familiar to XJ owners and necessary because Jeep changed hardware, wiring, and diagnostics across 1988–2001.

But the repo should grow along the swap workflow:
1. identify what is in the Jeep now
2. decide what aftermarket ECU strategy fits
3. wire it correctly
4. configure it to start
5. tune it to run well and stay reliable

## Expansion priorities

### 1. Fill swap blockers first
Add detail wherever a missing fact would stop a real swap in the garage.

Examples:
- missing trigger details
- missing sensor calibration data
- connector replacement uncertainty
- relay/power architecture ambiguity
- AW4 interaction edge cases
- 1996 transition-year exceptions

### 2. Keep era facts as support layers
Era files should answer:
- what stock hardware is present
- what changed from other eras
- what exceptions can break a generic swap plan

They should not become a disconnected encyclopedia.

### 3. Add year-specific exception files only when they unblock real decisions
Do not create a file for every year by default.
Do create a dedicated note file when one year or sub-range materially changes swap planning.

Current example:
- `vehicle/era3/1996-notes.md`

Potential future examples:
- 1991 early/late connector or sensor split, if confirmed
- 2000–2001 coil-rail integration details beyond current ignition notes

## Canonical places to add missing details

### Missing stock-system facts
Add to:
- `vehicle/eraX/overview.md` for high-level architecture or caveats
- `vehicle/eraX/<leaf>.md` for detailed era-specific facts
- `vehicle/trans/*.md` for transmission behavior

### Missing swap procedures or implementation strategy
Add to:
- `swap/ecu-selection/`
- `swap/wiring/`
- `swap/tuning/`
- `swap/index.md` if the new content changes workflow routing

### Missing connector details
Add to:
- `swap/wiring/connectors/<family>/overview.md`
- `swap/wiring/connectors/<family>/<leaf>.md`

### Missing cross-cutting repo guidance
Add to:
- `docs/`

## Practical rule for future additions
Before creating a file, ask:
1. Is this fact about the stock Jeep, or about the swap?
2. Is it true for all eras, one era, or only a special-case year/range?
3. Will putting it here help a person or agent complete the swap with less ambiguity?

If the answer to #3 is no, the file probably does not need to exist.
