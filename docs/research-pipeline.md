# Research Pipeline

This document defines the repeatable path from a new Jeep XJ topic idea to trusted canonical content.

Use it when the repo needs to expand coverage without creating structural drift.

It should be used with:
- `docs/repo-taxonomy.md`
- `docs/content-governance.md`
- `docs/file-creation-rules.md`
- `skillbuilding/evidence-standards.md`
- `skillbuilding/source-policy.md`
- `skillbuilding/work-item-lifecycle.md`
- `skillbuilding/file-maturity.md`
- `skillbuilding/prioritization-rubric.md`

## Purpose
The repo should grow by a controlled pipeline:
1. propose a topic
2. classify it into the taxonomy
3. collect and normalize evidence
4. draft only the narrowest truthful canonical files
5. harden those files over time
6. keep uncertainty visible until trust is earned

This pipeline is for both humans and agents.
It tells maintainers where planning work belongs, where canon belongs, and when a file is ready to be treated as trusted.

---

# 1. Pipeline summary

```text
topic proposal
  -> intake
  -> taxonomy classification
  -> backlog seeding
  -> research brief
  -> source intake and normalization
  -> canonical drafting
  -> hardening review
  -> trusted package
  -> revisit when new evidence appears
```

## Core rule
Do not move directly from "we should cover this" to broad canonical writing.
A topic should pass through intake, classification, evidence handling, and staged maturity.

---

# 2. Stages and outputs

## Stage 1: Topic proposal
A topic enters the system from one of these channels:
- repeated user questions
- known repo gaps
- transition-year uncertainty
- subsystem coverage gaps found during audits
- maintenance or diagnostic blind spots
- recurring sourcing decisions
- existing broad files that need splitting

### Required output
A short intake note that captures:
- proposed topic name
- the question being answered
- why the topic matters
- likely top-level domain
- likely system
- whether it is stock baseline or modified-state
- known compatibility dimensions

Primary companion doc:
- `docs/topic-intake-rules.md`

## Stage 2: Taxonomy classification
Classify the topic before doing deep research.

### Required decisions
1. Is the main question stock fact, procedure, diagnostics, sourcing, or governance?
2. Does it belong in `vehicle/`, `work/`, `diagnostics/`, `sourcing/`, `docs/`, or transitional `swap/`?
3. Is it stock baseline or modified-state guidance?
4. Which system owns it?
5. Do year, era, package, drivetrain, ABS, transmission, axle family, or donor family change the answer?
6. Does it need a single leaf or a branch with multiple child files?

### Required output
- intended canonical destination
- any supporting domains that will need cross-links
- a branch split plan if the topic is too broad for one file

Primary companion docs:
- `docs/repo-taxonomy.md`
- `docs/file-creation-rules.md`
- `docs/topic-intake-rules.md`

## Stage 3: Backlog seeding and prioritization
Once the topic is classified, turn it into trackable work.

### Required decisions
- Is this a suspected gap or a confirmed gap?
- Is this a research task, writing task, hardening task, or refactor task?
- What maturity is the first realistic target: `stub`, `partial`, `usable with caveats`, or `trusted`?
- What score does it get under the prioritization rubric?

### Required output
A backlog item with:
- title
- status
- source type
- task type
- domain layer
- canonical destination
- dependency notes
- priority score
- target maturity
- definition of done

Primary companion docs:
- `docs/backlog-seeding-guide.md`
- `skillbuilding/backlog.md`
- `skillbuilding/prioritization-rubric.md`

## Stage 4: Research brief
Break the topic into answerable questions before gathering sources.

### Required decisions
- What exact claims need proof?
- Which claims are high-risk vs medium-risk vs low-risk?
- What source classes are acceptable for each claim?
- Which uncertainties must remain visible even after a first draft?

### Required output
A topic brief that states:
- scope
- exclusions
- claim list
- evidence plan
- likely file splits
- likely blockers

Primary companion docs:
- `skillbuilding/work-item-lifecycle.md`
- `skillbuilding/evidence-standards.md`
- `skillbuilding/source-policy.md`

## Stage 5: Source intake and normalization
Collect source findings and separate them into stable categories.

### Required decisions
For each claim, record:
- source class
- source description
- scope and year range
- what the source supports
- confidence level
- caveats
- conflicts with other sources

### Required output
A normalized source intake package containing:
- confirmed facts
- likely but unverified claims
- conflicting claims
- unresolved questions
- recommended canonical destinations

Primary companion docs:
- `skillbuilding/source-policy.md`
- `skillbuilding/evidence-standards.md`

## Stage 6: Canonical drafting
Only validated, scoped claims move into canonical content.

### Drafting rules
- put the main truth in one canonical file
- cross-link instead of duplicating facts across domains
- keep routers small
- split broad topics into durable branches
- preserve explicit uncertainty labels where needed
- narrow the path if the claim is only true for a subset

### Required output
One or more canonical files in:
- `vehicle/`
- `work/`
- `diagnostics/`
- `sourcing/`
- transitional `swap/` when the topic is ECU swap execution

Primary companion docs:
- `docs/content-governance.md`
- `docs/file-creation-rules.md`
- `docs/naming-conventions.md`

## Stage 7: Hardening review
Review the draft package before treating it as normal downstream truth.

### Review questions
- is the domain correct?
- is stock truth separated from procedure and diagnostics?
- are compatibility limits explicit?
- is uncertainty preserved?
- is evidence strength appropriate to claim risk?
- does the package support real use without hidden assumptions?

### Required output
A hardening verdict:
- maturity rating
- blockers
- caveats to preserve
- next action needed

Primary companion docs:
- `skillbuilding/file-maturity.md`
- `skillbuilding/work-item-lifecycle.md`

## Stage 8: Trusted maintenance
Trusted does not mean frozen.
A trusted package should still be revisited when:
- a new year split appears
- donor/interchange reality changes
- a procedure proves too broad in use
- diagnostics reveal hidden ambiguity
- migration changes the canonical destination

### Required output
One of:
- no action
- hardening follow-up backlog item
- refactor/split task
- conflict investigation task

---

# 3. Topic classes inside the pipeline

## A. New topic
A topic not yet represented canonically.

Typical outputs:
- new branch seed
- new backlog item
- new canonical leaf or folder

## B. Expansion topic
A topic already exists, but coverage is too thin.

Typical outputs:
- package maturity upgrade
- compatibility leaf
- missing procedure or diagnostic leaf

## C. Hardening topic
A topic exists and is useful, but evidence, scope, or caveat handling is weak.

Typical outputs:
- source-backed corrections
- explicit uncertainty labels
- transition-year split
- better cross-links

## D. Refactor topic
A topic exists in the wrong shape.

Typical outputs:
- split broad file into branch + leaves
- relocate mixed-purpose content
- convert duplicated facts into canonical source + pointers

---

# 4. Source quality and evidence handling

## Match evidence strength to claim risk
Use `skillbuilding/evidence-standards.md` and `skillbuilding/source-policy.md`.

### High-risk claims
Examples:
- critical pinouts
- stock architecture that affects fitment or safety
- torque/spec values treated as authoritative
- transition-year hardware differences
- major diagnostics branch points

Expected support:
- Class A primary technical source, or
- Class B direct validation plus corroboration

### Medium-risk claims
Examples:
- service intervals used as guidance
- donor selection rules
- general maintenance branching
- common failure pattern summaries

Expected support:
- one strong source or documented practical validation, plus caveats where needed

### Low-risk claims
Examples:
- plain-language overview
- router summary
- glossary support

Expected support:
- accurate synthesis grounded in canonical material

## Provenance minimum
Every research-stage claim should record:
- source class
- source name or description
- claim supported
- year/era scope
- confidence label
- caveats or conflicts

---

# 5. Uncertainty preservation rules

## Core rule
Useful uncertainty should remain visible until it is resolved.
Do not smooth it away for readability.

## Approved labels
Use labels such as:
- `confirmed`
- `strongly supported`
- `likely`
- `provisional`
- `unverified`
- `conflicting`
- `needs source`
- `year-range uncertain`
- `transition-year caution`

## Where uncertainty should live
- in source-intake artifacts during research
- in canonical prose when the uncertainty still matters downstream
- in compatibility files when the uncertainty is split-dependent
- in backlog items when further validation is required

## When to split instead of caveat
Create a narrower file or branch when:
- one year range is clearly different
- one drivetrain or package changes the rule materially
- one donor family changes procedure or sourcing logic
- repeated caveats are making a file unreadable

---

# 6. Broad-topic splitting rules

Broad topics must be broken into durable branches before they become mega-docs.

## Split triggers
Split a topic when any of these are true:
- it mixes stock facts, procedures, diagnostics, and sourcing
- it spans multiple durable systems
- it needs repeated year or package caveats
- it contains multiple work classes
- it naturally requires more than one leaf type

## Recommended split order
1. domain
2. work class or system
3. component family or project family
4. compatibility split
5. leaf job type

## Example
Broad topic:
- "brakes"

Better split:
- `vehicle/systems/brakes/`
- `work/maintenance/brakes/`
- `work/repairs/brakes/`
- `work/upgrades/brakes/`
- `diagnostics/brakes/`
- `sourcing/interchange/brakes/`

## Rule for stubs
A stub may name a branch, but it must not pretend to answer the whole topic.
Stub scope should stay explicit.

---

# 7. Stub-to-trusted maturity path

Use the maturity model from `skillbuilding/file-maturity.md`.

## Stub
Use only to establish scope and destination.
A stub should:
- state the topic clearly
- define boundaries
- list the next expected child leaves or proof needs
- avoid broad technical claims

## Partial
Use when some real content exists, but important gaps remain.
A partial file should:
- answer at least one bounded question
- state known limits
- point to missing dependencies

## Usable with caveats
Use when the main path is present, but uncertainty remains.
A usable file should:
- support a real reader decision
- preserve caveats directly
- avoid hidden assumptions

## Trusted
Use when the package is ready for routine downstream use.
A trusted file or package should:
- have explicit scope
- have adequate evidence for claim risk
- surface major compatibility splits
- no longer hide swap-blocking or platform-blocking unknowns for normal use

## Promotion rule
Promote maturity only after reviewing the package, not just the presence of text.

---

# 8. Prioritization across repo domains

The repo now spans the full XJ platform, so prioritization cannot remain swap-only.

## Primary prioritization order
1. safety-critical and immobilizing diagnostics
2. maintenance and repair items that affect broad platform usability
3. stock platform baselines needed by many downstream topics
4. high-friction sourcing and interchange decisions
5. high-value upgrades and modifications
6. swap expansion and hardening
7. restoration depth work

## Why this order
- diagnostics and maintenance serve the widest share of XJ owners
- stock baselines unlock accurate work, sourcing, and diagnostics coverage
- sourcing and interchange reduce wrong-part drift
- upgrades and swaps matter, but should build on baseline truth
- restoration should grow steadily without displacing urgent operational coverage

## Priority lenses to apply together
For each topic, score:
- reader impact
- wrong-decision risk
- dependency leverage
- year/era ambiguity risk
- evidence feasibility
- domain balance across the repo

Use `skillbuilding/prioritization-rubric.md` and adapt it beyond swap-only impact when planning platform-wide coverage.

---

# 9. Required handoffs between docs and skillbuilding

## `docs/` owns
- pipeline rules
- intake rules
- taxonomy placement
- anti-drift governance
- roadmap structure

## `skillbuilding/` owns
- evidence capture
- source intake artifacts
- backlog entries
- maturity reviews
- research and hardening workflows

## Canonical content roots own
- the final Jeep truth, procedures, diagnostics, and sourcing guidance

Rule:
Do not let `docs/` or `skillbuilding/` become the hidden encyclopedia.

---

# 10. Minimum checklist before canonical writing

Before adding new canonical content, confirm:
1. the topic has a defined canonical home
2. the question type is classified correctly
3. stock vs modified-state is explicit
4. the system owner is explicit
5. compatibility splits are known or called out as unknown
6. source quality matches claim risk
7. uncertainty labels are ready where needed
8. the topic has a clear target maturity
9. backlog and dependency context are captured if the package is not yet trusted

---

# 11. Summary

The repo should expand through a repeatable chain:
- propose
- classify
- prioritize
- research
- normalize
- draft canonically
- harden
- trust
- revisit when new evidence appears

That process keeps the expanded XJ knowledge system scalable, agent-friendly, and resistant to structural drift.
