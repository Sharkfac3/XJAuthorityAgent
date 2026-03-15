# Evidence Standards

Use this file to decide what level of support a claim needs before it should be trusted or merged into canonical repo content.

## Purpose
Not every claim in an ECU swap project needs the same proof strength.
A glossary definition needs less proof than a trigger decoder name or injector characterization value.

This file helps the project:
- label uncertainty honestly
- avoid overstating weak claims
- choose when a note is ready for merge
- decide when a claim needs stronger validation first

## Evidence source types
Ordered roughly from stronger to weaker for technical swap claims:

1. **OEM/service documentation**
   - factory service manual
   - official wiring diagrams
   - official parts references

2. **Direct inspection or measurement**
   - connector inspection
   - bench testing
   - electrical measurement
   - waveform capture

3. **Platform documentation**
   - official Speeduino/rusEFI documentation
   - firmware decoder docs
   - board-level IO references

4. **Known-good field validation**
   - tested on a running XJ
   - repeated successful implementation
   - documented comparison against observed behavior

5. **Vendor documentation**
   - sensor datasheet
   - injector vendor data
   - connector catalog/spec sheet

6. **Community synthesis**
   - respected forum thread summary
   - experienced builder notes
   - long-form how-to with evidence trail

7. **Writer or agent synthesis only**
   - interpretation without supporting evidence
   - inferred generalization from adjacent facts

## Confidence labels
- `confirmed` — directly supported by strong evidence and no unresolved conflict
- `strongly supported` — good support, minor uncertainty remains
- `plausible` — reasonable but incomplete support
- `provisional` — useful working assumption, not ready as settled fact
- `conflicting` — evidence materially disagrees
- `unknown` — no adequate evidence yet

## Minimum evidence by claim type

### High-risk technical claims
Examples:
- trigger pattern description
- decoder name
- critical pinout
- power/relay architecture
- injector dead time values used as authoritative
- AW4 retained input behavior

Recommended minimum:
- OEM/service documentation, or
- direct measurement/inspection plus corroboration, or
- documented field validation plus cross-checking

Weak on its own:
- forum consensus without primary support
- unsourced memory

### Medium-risk technical claims
Examples:
- sensor reuse guidance
- broad wiring strategy
- platform feature compatibility
- base calibration starting assumptions

Recommended minimum:
- at least one strong technical source plus one corroborating source, or
- tested field implementation with explicit caveats

### Low-risk explanatory claims
Examples:
- glossary-style explanation
- broad conceptual summaries
- audience-appropriate analogy

Recommended minimum:
- accurate synthesis grounded in canonical technical docs

## Merge guidance

### Safe to merge as canonical fact when:
- year/era range is explicit
- evidence meets the topic risk level
- destination file is the narrowest truthful home
- caveats are preserved where needed
- no known conflicting claim is hidden

### Merge only with uncertainty label when:
- the claim is useful but not fully proven
- the repo benefits from a provisional working note
- the caveat materially changes reader decisions

Suggested labels to preserve in drafts or planning notes:
- `provisional`
- `needs source`
- `needs validation`
- `year-range uncertain`
- `conflicting reports`

### Do not merge as settled fact when:
- the claim lacks a credible source for its risk level
- the year range is guessed
- the claim conflicts with another unresolved claim
- it is only true for one sub-range but is written as universal

## Special handling areas

### 1996 and other transition years
Require extra caution because transition-year assumptions often fail.
Prefer direct documentation or strong corroboration before treating a rule as settled.

### Trigger and ignition data
These are swap-critical.
Do not promote platform-specific decoder names or tooth-pattern descriptions from weak evidence.

### Injector data
Separate:
- known stock injector spec
- estimated tuning starting value
- measured characterization data

Do not collapse these into one “spec.”

### Connector and pinout data
A connector family ID alone is not enough.
Critical pin/polarity/keying claims should be corroborated before being treated as authoritative.

## Conflict handling
When sources disagree:
1. keep both claims visible
2. label the conflict explicitly
3. attach year/era scope if that may explain the disagreement
4. route the issue into research planning instead of forcing a merge

## Relationship to other skillbuilding files
- use likely-risk context from `skillbuilding/critical-unknowns.md`
- classify the gap with `skillbuilding/gap-taxonomy.md`
- capture source-by-source claims with `skillbuilding/templates/source-intake.md`
- profile suspected weak areas with `skillbuilding/templates/likely-gap-profile.md`
