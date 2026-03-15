# Skillbuilding Backlog

Use this file as the active work queue for improving the repo.

## Purpose
The rest of `skillbuilding/` defines how to think about gaps, evidence, maturity, and readiness.
This file is where that framework turns into concrete work.

Use this backlog to:
- capture likely high-value unknowns
- track confirmed gaps from audits
- separate research work from writing work
- sequence work by impact and dependency value
- define what “done” means before work starts

## Rules
- Prefer confirmed gaps over vague ideas.
- Likely gaps may appear here, but they must be labeled clearly.
- Canonical destinations must point to `vehicle/`, `swap/`, or `book/`.
- Meta-framework work in `skillbuilding/` should be secondary to swap-critical canonical work.
- Do not mark an item complete just because a file exists.
- Use the lifecycle from `skillbuilding/work-item-lifecycle.md`.

## Recommended fields
For each backlog item, capture:
- ID
- title
- status (`suspected`, `audited`, `researched`, `normalized`, `drafted`, `hardened`, `trusted`, `deferred`)
- source type (`likely gap`, `confirmed gap`, `hardening follow-up`, `research lead`)
- task type (`new file`, `expand file`, `audit file`, `validate file`, `refactor file`)
- domain layer
- canonical destination
- dependency notes
- priority score
- target maturity (`partial`, `usable with caveats`, `trusted`)
- definition of done

## Priority bands
Use the rubric from `skillbuilding/prioritization-rubric.md`.

- `14–18` → do soon
- `9–13` → important, schedule next
- `4–8` → useful but lower urgency
- `0–3` → defer unless it supports another task

## Backlog structure

### Active candidates
Use this section for work that is likely next.

| ID | Title | Status | Source Type | Task Type | Domain Layer | Canonical Destination | Dependencies | Priority Score | Target Maturity | Definition of Done |
|---|---|---|---|---|---|---|---|---:|---|---|
| BL-001 | 1996 transition-year audit and expansion | suspected | likely gap | audit file | stock Jeep identification | `vehicle/era3/1996-notes.md` | era 3 overview and related leaf files | 17 | usable with caveats | 1996-specific swap-affecting exceptions are identified, scoped, and routed to the right canonical files |
| BL-002 | AW4 TPS coexistence hardening | suspected | likely gap | expand file | wiring and physical integration | `swap/wiring/aw4-tps.md` | `vehicle/trans/aw4.md`, wiring docs | 17 | trusted | retained-input behavior, wiring options, and failure symptoms are explicit enough for implementation |
| BL-003 | Trigger pattern validation by era | suspected | likely gap | validate file | ECU configuration for first start | `vehicle/era1/trigger.md`, `vehicle/era2/trigger.md`, `vehicle/era3/trigger.md` | ignition docs and platform decoder naming | 18 | trusted | each era trigger description is scoped, validated, and aligned with supported ECU platform naming |
| BL-004 | Sensor calibration reuse matrix | suspected | likely gap | expand file | ECU configuration for first start | era sensor leaf files + `swap/tuning/first-start.md` | sensor docs by era | 15 | usable with caveats | reusable sensors, required calibrations, and known caveats are explicit by era |
| BL-005 | Connector sourcing and replacement strategy | suspected | likely gap | expand file | wiring and physical integration | `swap/wiring/connectors/` | connector family docs, wiring docs | 15 | usable with caveats | critical connector families include sourcing direction, reuse/replace guidance, and repin caveats |
| BL-006 | First-start validation checklist hardening | suspected | likely gap | expand file | ECU configuration for first start | `swap/tuning/first-start.md` | trigger, injectors, ignition, sensors | 14 | trusted | a reader can verify safe pre-crank conditions without hidden assumptions |
| BL-007 | Troubleshooting flow framework | suspected | likely gap | new file | troubleshooting and ongoing validation | `swap/` future troubleshooting docs | tuning and sensor packages | 13 | usable with caveats | top failure modes are grouped into a canonical troubleshooting structure with clear routing |
| BL-008 | XJ-specific ECU platform tradeoff review | suspected | likely gap | expand file | swap strategy selection | `swap/ecu-selection/requirements.md` + platform files | Speeduino/rusEFI docs, XJ constraints | 12 | usable with caveats | platform guidance reflects XJ-specific trigger, idle, AW4, and supportability tradeoffs |

### Parked / deferred
Use this section for real work that should wait.

| ID | Title | Reason Deferred | Revisit Trigger |
|---|---|---|---|
| BL-D01 | Year-by-year exception expansion beyond known high-risk cases | only worth doing when confirmed by audit or source conflict | repeated audit findings or confirmed new year split |

### Completed / promoted
Move items here when the target outcome has actually been reached.

| ID | Title | Final Status | Canonical Destination | Notes |
|---|---|---|---|---|

## How to use this file
1. Add new items after an audit, research plan, or hardening review.
2. Score them with `skillbuilding/prioritization-rubric.md`.
3. Assign the right lifecycle stage from `skillbuilding/work-item-lifecycle.md`.
4. Point each item at the narrowest truthful canonical destination.
5. Re-score items when dependencies change or evidence becomes easier to obtain.

## Related files
- `skillbuilding/domain-map.md`
- `skillbuilding/gap-taxonomy.md`
- `skillbuilding/critical-unknowns.md`
- `skillbuilding/prioritization-rubric.md`
- `skillbuilding/work-item-lifecycle.md`
- `skillbuilding/file-maturity.md`
