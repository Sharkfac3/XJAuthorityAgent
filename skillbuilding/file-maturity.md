# File Maturity Model

Use this file to classify how trustworthy and complete a canonical repo file is.

## Purpose
A file existing is not the same as a file being reliable.
This model gives the project a shared way to describe maturity during audits, backlog planning, and release hardening.

It is especially useful when a file is:
- present but thin
- technically correct but incomplete
- useful only with caveats
- ready for normal downstream use

## Scope
This model is for evaluating canonical content in:
- `vehicle/`
- `swap/`
- `book/`

It can also be used for package-level evaluation across related files.

## Maturity levels

### 0. Stub
The file exists mainly as a placeholder or outline.

Typical signs:
- minimal content
- broad topic named but not developed
- no practical decision support
- little or no scoped year/era information

Use implications:
- not safe to rely on
- should trigger backlog or research work

### 1. Partial
The file contains some useful material, but cannot yet support confident use by itself.

Typical signs:
- one or more important facts are present
- important gaps remain
- edge cases are absent
- year/era scope may be incomplete
- procedure steps may be missing dependencies

Use implications:
- useful as a starting point only
- not ready as authoritative guidance

### 2. Usable with caveats
The file is substantially helpful, but caveats must remain visible.

Typical signs:
- main workflow or fact set is present
- most important decisions are supported
- known uncertainties are labeled
- missing details exist but do not fully invalidate the file
- year/era limits are called out where known

Use implications:
- can be used with care
- reviewers and downstream agents must preserve caveats
- a release-hardening pass may still identify blockers for full trust

### 3. Trusted
The file is mature enough for normal downstream use.

Typical signs:
- core facts or procedures are present and coherent
- year/era scope is explicit
- major caveats are already handled
- evidence strength is appropriate for the topic risk
- missing details are minor rather than swap-critical
- the target reader can use the file with confidence

Use implications:
- suitable for routine use by readers and agents
- still open to improvement, but not dependent on hidden assumptions

## Evaluation dimensions
Rate maturity using these dimensions together, not in isolation.

### 1. Coverage completeness
Ask:
- Does the file answer the main question it is supposed to answer?
- Are the swap-critical details present?
- Are obvious next-step dependencies missing?

### 2. Year/era clarity
Ask:
- Is the applicable year range explicit?
- Are exceptions labeled clearly?
- Is 1996 handled when relevant?

### 3. Evidence adequacy
Ask:
- Does the confidence level match the risk of the claim?
- Are weak claims labeled as such?
- Are unsupported universal statements avoided?

### 4. Practical usability
Ask:
- Could a reader or agent act on this file correctly?
- Does it explain enough to avoid likely misuse?
- Are key dependencies named or linked?

### 5. Audience fit
Ask:
- Is the content understandable for the intended DIY reader?
- Are terms defined when needed?
- Is “why before how” preserved for procedures?

## Package-level maturity
Some files should be evaluated as part of a package, not alone.

Examples:
- one era overview plus its leaf files
- a wiring package plus connector docs
- ECU selection requirements plus platform comparison docs
- first-start plus ignition and trigger docs

Rule:
A package is only as mature as its critical dependency gaps allow.
A strong overview file does not make a weak dependency package trusted.

## Maturity guidance by level

### Promoting from Stub to Partial
Requires:
- real scoped content
- a defined question the file answers
- at least minimal year/era framing where relevant

### Promoting from Partial to Usable with caveats
Requires:
- main facts or workflow present
- major unknowns made visible
- no hidden swap-critical assumptions
- caveats preserved explicitly

### Promoting from Usable with caveats to Trusted
Requires:
- no unresolved swap-blocking gaps in normal use
- acceptable evidence support for the file’s claim type
- explicit year/era boundaries
- enough clarity for the intended reader or downstream agent

## Warning signs that force a lower maturity rating
Lower the maturity rating if any of these appear:
- year range is implied rather than stated
- exceptions are known but not called out
- the file depends on unstated assumptions
- the file is technically correct but not operationally useful
- the file contains unsupported universal claims
- critical connectors, trigger details, relay behavior, or safety caveats are missing when central to the topic

## Suggested audit output format
When rating a file, return:
- file path
- maturity rating (`stub`, `partial`, `usable with caveats`, `trusted`)
- strengths
- blockers
- caveats to preserve
- next action needed

## Relationship to other skillbuilding files
- use `skillbuilding/evidence-standards.md` for claim strength
- use `skillbuilding/source-policy.md` for provenance expectations
- use `skillbuilding/work-item-lifecycle.md` for stage tracking
- use `skillbuilding/skills/release-hardening.md` when deciding whether a file or package is trusted enough for use
