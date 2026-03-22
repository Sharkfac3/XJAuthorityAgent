# Backlog Seeding Guide

This document explains how to turn roadmap branches and topic intake decisions into a stable, repeatable work queue.

Use it with:
- `docs/topic-intake-rules.md`
- `docs/research-pipeline.md`
- `docs/coverage-roadmap.md`
- `skillbuilding/backlog.md`
- `skillbuilding/prioritization-rubric.md`
- `skillbuilding/work-item-lifecycle.md`
- `skillbuilding/file-maturity.md`

## Purpose
The backlog should not be a random idea pile.
It should be the controlled bridge between:
- topic proposals
- roadmap branch seeding
- evidence gathering
- canonical writing
- hardening and trust promotion

A seeded backlog item should be narrow enough to act on, broad enough to matter, and explicit about destination, maturity, and dependency.

---

# 1. What belongs in the backlog

Backlog items should represent real repo-building work such as:
- creating a missing branch router
- expanding a thin but important branch
- validating a high-risk claim
- hardening an existing package
- splitting a broad file into durable leaves
- adding a missing diagnostic or sourcing branch

Do not add vague aspirations such as:
- "cover brakes better"
- "do more diagnostics"
- "research body stuff"

Turn those into narrow, scoreable items.

---

# 2. Backlog item sources

A good backlog item usually comes from one of these channels:
- roadmap branch seeding
- topic intake
- audit result
- source conflict
- hardening review follow-up
- repeated user demand
- dependency discovered during writing

## Source-type labels
Use one of:
- `likely gap`
- `confirmed gap`
- `research lead`
- `hardening follow-up`
- `migration follow-up`
- `refactor need`

---

# 3. Convert a broad roadmap branch into backlog items

A roadmap branch is often too broad to enter the backlog directly.
Convert it into work items using this sequence.

## Step 1: identify the branch owner
Examples:
- stock baseline branch
- maintenance branch
- diagnostics branch
- sourcing branch

## Step 2: identify the first durable deliverable
Good first deliverables:
- domain router
- branch overview
- one high-value compatibility file
- one high-frequency procedure
- one high-frequency diagnostic leaf
- one donor/selection comparison

## Step 3: identify dependencies
Typical dependencies:
- year/era baseline not yet written
- system overview missing
- connector or donor family unclear
- sourcing branch needed before procedure can stay narrow

## Step 4: set target maturity
For branch-seeding items, the first target is usually:
- `stub` for routers only
- `partial` for a first useful leaf
- `usable with caveats` for a common workflow

Do not demand `trusted` by default for first-wave seeding.

---

# 4. Required backlog fields

When seeding a new item, capture at minimum:
- ID
- title
- status
- source type
- task type
- domain layer
- canonical destination
- dependencies
- priority score
- target maturity
- definition of done

Use the field meanings already established in `skillbuilding/backlog.md`.

## Recommended task-type labels
- `new file`
- `expand file`
- `audit file`
- `validate file`
- `refactor file`
- `seed branch`
- `harden package`

## Recommended status labels
Use lifecycle-aligned states:
- `suspected`
- `audited`
- `researched`
- `normalized`
- `drafted`
- `hardened`
- `trusted`
- `deferred`

---

# 5. Sizing rules for backlog items

## Good backlog item size
A good item usually produces one of:
- one router
- one narrow leaf
- one branch seed package
- one evidence-validation pass
- one hardening pass for a coherent package

## Too large
Split the item when it would require:
- multiple top-level domains at once
- an entire system encyclopedia
- all years and all variants in one pass
- both baseline facts and all procedures and diagnostics together

## Too small
Merge the item when it is only:
- a heading with no distinct user value
- a synonym for another item
- a micro-claim that cannot stand as a meaningful work unit

---

# 6. Priority rules for backlog seeding

Use `skillbuilding/prioritization-rubric.md`, but apply it with platform-wide logic.

## Default seeding order
1. blockers and safety-critical diagnostics
2. maintenance and repair items with broad owner impact
3. stock baseline files that unlock many branches
4. high-friction sourcing/interchange decisions
5. common upgrades
6. swap hardening and expansion
7. restoration depth work

## Good tie-breakers
When two items score similarly, prefer:
1. the one that unblocks more downstream files
2. the one with clearer year/era scope
3. the one with higher wrong-decision risk
4. the one with a faster evidence path

## Domain-balance rule
Do not let the backlog drift into one domain just because that domain already has momentum.
Maintain visible next-wave items across:
- stock baseline
- work procedures
- diagnostics
- sourcing/interchange
- migration/hardening

---

# 7. Stub seeding vs real writing

## Use stub seeding when
- the branch destination is clear
- deeper research will take time
- the repo benefits from explicit routing now
- the stub will help future backlog placement

## Do not use stub seeding when
- the path is still taxonomically unclear
- the branch would be pure filler
- the stub would look authoritative without evidence

## Stub definition of done
A good stub should:
- define scope
- state what the branch will and will not hold
- list likely next child leaves
- carry no unsupported universal claims

---

# 8. How stubs become trusted files

Use this promotion pattern:

## 1. Seed
Create router or narrow placeholder with explicit limits.

## 2. Research
Attach a topic brief and source plan.

## 3. Normalize
Record supported facts, caveats, and conflicts.

## 4. Draft
Write the narrowest truthful canonical file.

## 5. Harden
Rate maturity and preserve caveats.

## 6. Promote
Mark as `usable with caveats` or `trusted` only when the package actually supports use.

Rule:
Do not mark a branch mature just because the router exists.

---

# 9. Roadmap-to-backlog examples

## Example A: cooling system branch seed
Roadmap branch:
- `vehicle/systems/cooling/`

Bad backlog item:
- "write cooling system"

Better backlog sequence:
1. seed branch router for `vehicle/systems/cooling/`
2. create `work/maintenance/cooling/` router
3. add high-value leaf for cooling system refresh route
4. add diagnostic leaf for overheating at idle
5. add sourcing comparison for radiator/fan family choices if wrong-part risk appears high

## Example B: body/interior coverage
Roadmap branch:
- `work/repairs/interior/`
- `work/restoration/interior/`

Bad backlog item:
- "interior coverage"

Better backlog sequence:
1. seed repair vs restoration split
2. add headliner repair starter
3. add seat and trim attachment branch seed
4. add water-ingress diagnostic seed if repeated demand appears

## Example C: drivetrain coverage
Roadmap branch:
- `vehicle/systems/transmission/`
- `diagnostics/driveline/`
- `work/upgrades/driveline/`

Better backlog sequence:
1. stock baseline for AW4/transfer-case branch routing
2. maintenance leaf for fluid service path
3. diagnostic leaf for driveline vibration isolation
4. upgrade branch seed for SYE and related driveline changes

---

# 10. Definition-of-done guidance by item type

## Seed branch
Done when:
- branch path is correct
- router states scope clearly
- child topics are listed
- no false authority is implied

## New file
Done when:
- one bounded question is answered
- scope and compatibility are explicit
- canonical destination is correct
- caveats are preserved

## Validate file
Done when:
- high-risk claims are checked against acceptable source classes
- conflicts are surfaced or resolved
- downstream wording is corrected if needed

## Harden package
Done when:
- package maturity is rated
- blockers are known
- caveats are preserved
- next actions are explicit

## Refactor file
Done when:
- mixed-purpose content is split cleanly
- canonical ownership is clearer than before
- routing improves without losing truth

---

# 11. Recommended seeding cadence

Use a repeating cycle instead of one giant planning burst.

## Suggested cadence
1. review roadmap branch priorities
2. convert one branch family into 3 to 7 backlog items
3. score and rank them
4. execute the highest-value item
5. harden or split based on what is learned
6. reseed the next wave

This keeps the backlog current and prevents a stale giant plan.

---

# 12. Anti-drift rules for backlog seeding

Do not create backlog items that:
- point to the wrong top-level domain
- assume all future work belongs under `swap/`
- hide major year/era uncertainty
- mix stock baseline, work, diagnostics, and sourcing into one output
- define success as "file exists"
- seed vague folders like `misc/`, `general/`, or `other/`

---

# 13. Summary

Backlog seeding should translate roadmap structure into small, actionable, maturity-aware work items.
A good backlog item has:
- a clear destination
- a clear type of work
- a scoreable priority
- explicit dependencies
- a realistic target maturity
- a real definition of done
