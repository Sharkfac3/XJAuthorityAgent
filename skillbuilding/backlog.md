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

Use `skillbuilding/templates/backlog-item.md` when drafting a new entry outside the table.

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
| BL-001 | 1996 transition-year audit and expansion | audited | confirmed gap | audit file | stock Jeep identification | `vehicle/era3/1996-notes.md` | era 3 overview and related leaf files | 17 | usable with caveats | 1996-specific swap-affecting exceptions are identified, scoped, and routed to the right canonical files |
| BL-002 | AW4 TPS coexistence hardening | suspected | likely gap | expand file | wiring and physical integration | `swap/wiring/aw4-tps.md` | `vehicle/trans/aw4.md`, wiring docs | 17 | trusted | retained-input behavior, wiring options, and failure symptoms are explicit enough for implementation |
| BL-003 | Trigger pattern validation by era | researched | confirmed gap | validate file | ECU configuration for first start | `vehicle/era1/trigger.md`, `vehicle/era2/trigger.md`, `vehicle/era3/trigger.md` | ignition docs and platform decoder naming | 18 | trusted | each era trigger description is scoped, validated, and aligned with supported ECU platform naming. **Resolved:** Era 2/3 crank pattern confirmed 18-2-2-2 all sub-years; Speeduino decoder confirmed `Jeep 2000` (source: wiki.speeduino.com); rusEFI `Jeep 18-2-2-2` confirmed carries to Era 3. **Still open:** Era 1 Speeduino decoder name (`Renix 44-2-2` unverified); 2000–2001 cam sensor connector family/pinout (see BL-011). |
| BL-004 | Sensor calibration reuse matrix | audited | confirmed gap | expand file | ECU configuration for first start | era sensor leaf files + `swap/tuning/first-start.md` | sensor docs by era | 15 | usable with caveats | reusable sensors, required calibrations, and known caveats are explicit by era |
| BL-005 | Connector sourcing and replacement strategy | audited | confirmed gap | expand file | wiring and physical integration | `swap/wiring/connectors/` | connector family docs, wiring docs | 15 | usable with caveats | critical connector families include sourcing direction, reuse/replace guidance, and repin caveats |
| BL-006 | First-start validation checklist hardening | audited | confirmed gap | expand file | ECU configuration for first start | `swap/tuning/first-start.md` | trigger, injectors, ignition, sensors | 14 | trusted | a reader can verify safe pre-crank conditions without hidden assumptions |
| BL-007 | Troubleshooting flow framework | audited | confirmed gap | new file | troubleshooting and ongoing validation | `swap/` future troubleshooting docs | tuning and sensor packages | 13 | usable with caveats | top failure modes are grouped into a canonical troubleshooting structure with clear routing |
| BL-008 | XJ-specific ECU platform tradeoff review | audited | confirmed gap | expand file | swap strategy selection | `swap/ecu-selection/requirements.md` + platform files | Speeduino/rusEFI docs, XJ constraints | 12 | usable with caveats | platform guidance reflects XJ-specific trigger, idle, AW4, and supportability tradeoffs |
| BL-009 | Injector characterization for first start | audited | confirmed gap | expand file | ECU configuration for first start | `vehicle/era1/injectors.md`, `vehicle/era2/injectors.md`, `vehicle/era3/injectors.md`, `swap/tuning/first-start.md` | fuel pressure splits, sensor calibration work | 14 | usable with caveats | injector flow, pressure context, dead time assumptions, and safe first-start defaults are explicit by era |
| BL-010 | Era 3 power-relay subrange hardening | audited | confirmed gap | expand file | wiring and physical integration | `vehicle/era3/power-relay.md` | `vehicle/era3/wiring.md`, `vehicle/era3/1996-notes.md`, era 2 power-relay doc | 14 | trusted | era 3 relay behavior is explicit for 1996, 1997–1999, and 2000–2001 where differences matter |
| BL-011 | 2000–2001 cam sensor connector and routing validation | audited | confirmed gap | validate file | wiring and physical integration | `vehicle/era3/trigger.md` + connector leaf under `swap/wiring/connectors/` | coil-rail ignition docs, JTEC connector docs, FSM validation | 16 | trusted | the 2000–2001 cam sensor connector family, pin expectations, and routing are confirmed and reflected in canonical files |
| BL-012 | XJ ECU platform comparison matrix | audited | confirmed gap | new file | swap strategy selection | `swap/ecu-selection/platform-comparison.md` | `swap/ecu-selection/requirements.md`, platform files, AW4 and IAC constraints | 11 | usable with caveats | a side-by-side matrix supports platform choice across trigger support, IAC, ignition outputs, AW4 fit, logging, and supportability |
| BL-013 | Datalogging and post-change validation workflow | audited | confirmed gap | new file | troubleshooting and ongoing validation | `swap/tuning/datalogging.md`, `swap/tuning/validation-routine.md` | first-start, VE, ignition, closed-loop, and troubleshooting docs | 10 | usable with caveats | readers can capture logs, review key channels, version tune changes, and run a repeatable validation routine after changes |

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
