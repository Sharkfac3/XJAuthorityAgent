# Source Policy

Use this file to decide what kinds of sources are acceptable for repo-building work, how to record provenance, and when a claim is strong enough to move into canonical content.

## Purpose
This project will grow from mixed source types:
- factory/service information
- ECU platform documentation
- vendor data
- direct inspection and testing
- community writeups
- personal field notes

Those sources do not all carry the same weight.
This policy exists to keep the repo honest, traceable, and useful.

## Core rules
1. **Record where a claim came from.**
   - Do not merge technical claims with no provenance.
2. **Match source strength to claim risk.**
   - High-risk swap claims need stronger support.
3. **Do not hide uncertainty.**
   - If a source is weak, label the claim accordingly.
4. **Do not flatten year/era scope.**
   - A source applying to one year range must not be written as universal.
5. **Prefer canonical truth over convenience.**
   - If a source is useful but weak, keep it in planning/research flow until validated.

## Source classes

### Class A — Primary technical sources
Use as strongest support when available.

Examples:
- OEM factory service manuals
- official wiring diagrams
- official parts catalogs
- official Speeduino or rusEFI documentation
- official firmware decoder documentation
- vendor datasheets and connector catalog documents

Typical use:
- trigger definitions
- pinouts
- relay architecture
- sensor specs
- ECU feature support

## Class B — Direct validation sources
Use as strong support when well documented.

Examples:
- bench measurements
- waveform captures
- continuity checks
- connector inspection with photos/notes
- running-vehicle validation
- repeatable install/test results

Typical use:
- confirming connector identity
- validating sensor behavior
- checking polarity or wiring assumptions
- validating practical platform compatibility

## Class C — Secondary technical synthesis
Useful, but not enough by itself for many high-risk claims.

Examples:
- well-researched forum summaries
- long-form community writeups with evidence
- builder notes referencing manuals or measurements
- vendor support replies without formal docs

Typical use:
- discovering likely directions
- finding terminology
- identifying edge cases to validate
- supporting medium-risk guidance with caveats

## Class D — Informal or weak sources
Useful for hypothesis generation only unless later validated.

Examples:
- unsourced forum posts
- memory-based claims
- anecdotal social media notes
- undocumented assumptions
- agent inference without evidence

Typical use:
- likely-gap discovery
- research lead generation
- backlog seeding

Do not treat these as settled canonical truth.

## What must be recorded for a source-backed claim
At minimum, capture:
- source type
- source name or description
- date captured, if relevant
- what exact claim the source supports
- year/era range the claim applies to
- any caveat or uncertainty the source introduces

Use `skillbuilding/templates/source-intake.md` when normalizing source material.

## Provenance expectations by claim type

### High-risk technical claims
Examples:
- trigger decoder name
- tooth pattern description
- critical pinout or polarity
- AW4 retained inputs
- power/relay behavior
- injector characterization treated as authoritative

Required standard:
- Class A, or
- Class B plus corroboration, or
- strong field validation with explicit scope and cross-checking

Not enough on its own:
- community consensus
- single unsourced anecdote
- agent synthesis

### Medium-risk technical claims
Examples:
- sensor reuse guidance
- broad harness strategy
- platform fit guidance
- first-start setup assumptions

Required standard:
- at least one strong technical source, or
- practical validation plus caveats, or
- multiple weaker sources with cross-checking and explicit uncertainty

### Low-risk explanatory claims
Examples:
- concept explanations
- glossary support
- plain-language summaries

Required standard:
- accurate synthesis grounded in canonical technical content

## When forum/community information is acceptable
Community information is acceptable when it is used correctly.

Good uses:
- identifying likely problem areas
- finding alternate terminology
- locating likely year-range splits to investigate
- supporting a claim that already has stronger evidence

Bad uses:
- treating repeated hearsay as proof
- using one forum post as authority for a high-risk spec
- copying a claim into canonical docs without checking scope or provenance

## When personal notes are acceptable
Personal notes can be valuable if they are specific and scoped.

Acceptable when they include:
- what vehicle or parts were inspected
- year/era context
- what was observed or measured
- what was inferred vs directly seen
- any uncertainty or limitation

Not acceptable when they are:
- vague memory
- detached from year/era scope
- written as universal without support

## Citation/provenance style for planning work
In `skillbuilding/`, concise provenance is enough.

Suggested pattern:
- source class:
- source name:
- supports claim:
- year/era scope:
- confidence:
- caveats:

This folder is for project-building work, so full academic citation format is not required.
Traceability is required.

## Merge policy

### Can merge into canonical docs when:
- provenance is known
- source strength matches claim risk
- year/era range is explicit
- caveats are preserved
- conflicting claims are not hidden

### Should stay in skillbuilding/research flow when:
- provenance is weak
- source scope is unclear
- claim is interesting but unverified
- year-range may differ but is not confirmed
- evidence conflicts materially

## Conflict policy
When sources disagree:
1. do not force a clean merge
2. preserve the disagreement in planning notes
3. check whether the conflict is really a year/era split
4. route the issue into research planning or source intake
5. merge canonically only after the conflict is resolved or clearly bounded

## Special caution areas
These areas should be held to a higher standard:
- 1996 transition-year behavior
- trigger and ignition pattern data
- connector pinouts and keying
- injector characterization
- AW4/TCU interaction
- power, relay, and grounding architecture

## Relationship to other skillbuilding files
- evidence strength and merge thresholds → `skillbuilding/evidence-standards.md`
- likely high-risk topics → `skillbuilding/critical-unknowns.md`
- gap classification → `skillbuilding/gap-taxonomy.md`
- source normalization → `skillbuilding/templates/source-intake.md`
- lifecycle tracking → `skillbuilding/work-item-lifecycle.md`
