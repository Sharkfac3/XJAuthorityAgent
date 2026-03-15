# Work Item Lifecycle

Use this file to track how a suspected gap moves from hypothesis to trusted canonical content.

## Purpose
The repo will grow more cleanly if project-building work follows a consistent lifecycle.
This reduces vague backlog items, hidden assumptions, and premature “done” status.

## Lifecycle stages

### 1. Suspected
A likely gap is identified from domain knowledge or project intuition.

Expected artifacts:
- optional `likely-gap-profile.md`
- reference to `critical-unknowns.md` if applicable

### 2. Audited
The repo has been reviewed and the suspected gap is either confirmed, narrowed, or dismissed.

Expected artifacts:
- `gap-report.md` entry
- optional `critical-unknown-review.md`

### 3. Researched
The question is broken into answerable pieces and evidence needs are defined.

Expected artifacts:
- `topic-brief.md`
- explicit evidence plan

### 4. Normalized
Raw source findings are separated into facts, conflicts, caveats, and open questions.

Expected artifacts:
- `source-intake.md`
- recommended canonical destinations

### 5. Drafted canonically
Validated content is written into `vehicle/`, `swap/`, or `book/`.

Expected artifacts:
- canonical file edits
- preserved caveats and year ranges

### 6. Hardened
The updated content is reviewed for trust, completeness, and audience fit.

Expected artifacts:
- release-hardening verdict
- blocker/caveat list if needed

### 7. Trusted
The content is ready for normal downstream use by readers and agents.

## Exit criteria by stage
- Suspected → Audited: actual files reviewed
- Audited → Researched: blocked decisions and evidence needs are clear
- Researched → Normalized: source material has been captured and organized
- Normalized → Drafted canonically: destination files and caveats are explicit
- Drafted canonically → Hardened: package reviewed against readiness criteria
- Hardened → Trusted: blockers resolved or caveats intentionally retained

## Rules
- Do not skip from suspected directly to trusted
- Do not mark a topic complete just because one file exists
- Use `usable with caveats` honestly when evidence or scope is still imperfect
- Keep unresolved year-range questions visible until closed

## Practical use
This lifecycle is especially useful for:
- trigger and ignition topics
- AW4 integration topics
- 1996 exception handling
- connector pinout validation
- injector and sensor characterization
