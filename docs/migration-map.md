# Migration Map

## Purpose
Path-specific migration map for the major existing content areas in the repo.

## Reading notes
- This map plans migration; it does not perform it.
- `keep` means stay in place for now.
- `move` means a direct relocation is reasonable.
- `split` means the source mixes multiple content types and should become multiple destination files.
- `merge` means the source should be absorbed into an existing destination branch.
- `deprecate` means the source should become a redirect or compatibility note after migration.

## Migration map

| Current path | Proposed new path | Decision | Reason | Dependencies / blockers | Risk notes |
|---|---|---|---|---|---|
| `vehicle/index.md` | `vehicle/index.md` | keep | Already matches the new architecture as the stock-facts router. | None. | Low risk; update links as child branches mature. |
| `vehicle/years/index.md` | `vehicle/years/index.md` | keep | Already functions as the correct time-based router. | Final decision on exact `1996-notes.md` placement. | Low risk. |
| `vehicle/systems/index.md` | `vehicle/systems/index.md` | keep | Already functions as the correct subsystem router. | Child branches need deeper leaves over time. | Low risk. |
| `vehicle/packages/index.md` | `vehicle/packages/index.md` | keep | Correct destination router under target taxonomy. | Needs future package leaves. | Low risk; currently scaffold-heavy. |
| `vehicle/configurations/index.md` | `vehicle/configurations/index.md` | keep | Correct destination router for stock combinations and matrices. | Needs future configuration leaves. | Low risk; currently scaffold-heavy. |
| `vehicle/interchange-baselines/index.md` | `vehicle/interchange-baselines/index.md` | keep | Correct destination for factual stock interchange baselines. | Needs future factual interchange leaves. | Low risk; avoid drifting into sourcing advice. |
| `vehicle/engine.md` | `vehicle/systems/engine/4.0l/overview.md` plus any swap-only notes moved into `work/swaps/ecu/` | split | Valuable stock engine baseline, but still broad and mildly swap-oriented at the repo root. | Need destination folder under `vehicle/systems/engine/`; must separate stock facts from swap framing. | Medium risk of losing nuance if moved as-is. |
| `vehicle/era1/overview.md` | `vehicle/years/era1/overview.md` | move | Pure era router/reference content; path normalization only. | Create `vehicle/years/era1/`. | Low risk; leave redirect note at old path. |
| `vehicle/era2/overview.md` | `vehicle/years/era2/overview.md` | move | Same as Era 1: fits the target `vehicle/years/` structure. | Create `vehicle/years/era2/`. | Low risk. |
| `vehicle/era3/overview.md` | `vehicle/years/era3/overview.md` | move | Same as Era 1/2; the right target is the new years branch. | Create `vehicle/years/era3/`. | Low risk; maintain `1996` cross-link. |
| `vehicle/era3/1996-notes.md` | `vehicle/years/1996-notes.md` or `vehicle/years/era3/1996-notes.md` | move | Strong year-specific reference note; belongs in the years branch. | Need one repo-wide convention for transition-year placement. | Medium risk if naming is inconsistent across years. |
| `vehicle/era1/wiring.md` | `vehicle/years/era1/wiring.md` with procedure-only notes later extracted to `work/swaps/ecu/wiring/` | split | Mostly stock era wiring context, but includes swap-adapter guidance. | Need `vehicle/years/era1/` and later extraction rules for procedure content. | Medium risk of keeping mixed-purpose content too long. |
| `vehicle/era2/wiring.md` | `vehicle/years/era2/wiring.md` with procedure-only notes later extracted to `work/swaps/ecu/wiring/` | split | Same pattern as Era 1. | Same as above. | Medium risk. |
| `vehicle/era3/wiring.md` | `vehicle/years/era3/wiring.md` with procedure-only notes later extracted to `work/swaps/ecu/wiring/` | split | Same pattern as Era 1/2, plus 1996/2000-2001 special handling. | Need year-edge-case links and extraction rules. | Medium risk; risk of duplicating year caveats. |
| `vehicle/era1/diagnostics.md` | `diagnostics/engine/era1-control-system-triage.md` plus `work/inspections/pre-swap/era1-health-check.md` | split | File mixes true diagnostics with pre-swap inspection workflow. | Need `diagnostics/engine/` and `work/inspections/pre-swap/` destinations. | High risk if moved whole; meaning would blur. |
| `vehicle/era2/diagnostics.md` | `diagnostics/engine/era2-control-system-triage.md` plus `work/inspections/pre-swap/era2-health-check.md` | split | Same mixed-purpose pattern as Era 1. | Same as above. | High risk. |
| `vehicle/era3/diagnostics.md` | `diagnostics/engine/era3-control-system-triage.md` plus `work/inspections/pre-swap/era3-health-check.md` | split | Same mixed-purpose pattern, plus OBD-II code-reading context. | Same as above. | High risk; do not flatten 1996/2000-2001 exceptions. |
| `vehicle/era1/injectors.md` | `vehicle/systems/fuel/injectors/era1-renix.md` | move | Primarily stock fuel-system reference content. | Need `vehicle/systems/fuel/injectors/` branch. | Medium risk if era caveats are not preserved. |
| `vehicle/era2/injectors.md` | `vehicle/systems/fuel/injectors/era2-sbec.md` | move | Same as Era 1 injectors. | Same as above. | Medium risk. |
| `vehicle/era3/injectors.md` | `vehicle/systems/fuel/injectors/era3-jtec.md` | move | Same as above; system-based destination is more durable. | Same as above. | Medium risk; preserve 2000-2001 context if needed. |
| `vehicle/era1/power-relay.md` | `vehicle/systems/electrical/engine-management-power/era1-renix.md` | move | Stock electrical/power architecture fact, not a vehicle root-level era fact forever. | Need `vehicle/systems/electrical/engine-management-power/`. | Medium risk if cross-links to swap wiring are lost. |
| `vehicle/era2/power-relay.md` | `vehicle/systems/electrical/engine-management-power/era2-sbec.md` | move | Same as Era 1 power-relay note. | Same as above. | Medium risk. |
| `vehicle/era3/power-relay.md` | `vehicle/systems/electrical/engine-management-power/era3-jtec.md` | move | Same as above. | Same as above. | Medium risk. |
| `vehicle/era1/trigger.md` | `vehicle/systems/ignition/triggers/era1-renix.md` | move | Stock trigger-pattern fact belongs under ignition/system reference. | Need `vehicle/systems/ignition/triggers/`. | Medium risk; preserve downstream swap references. |
| `vehicle/era2/trigger.md` | `vehicle/systems/ignition/triggers/era2-sbec.md` | move | Same as Era 1 trigger note. | Same as above. | Medium risk. |
| `vehicle/era3/trigger.md` | `vehicle/systems/ignition/triggers/era3-jtec.md` | move | Same as above. | Same as above. | Medium risk; keep coil-rail/distributor split visible. |
| `vehicle/era1/sensors/*` | `vehicle/years/era1/sensors/*` initially, with later normalization into system branches where useful | move | Low-risk first move is path normalization into `vehicle/years/`; deeper system normalization can come later. | Create `vehicle/years/era1/sensors/`. | Low-to-medium risk; avoid premature over-splitting. |
| `vehicle/era2/sensors/*` | `vehicle/years/era2/sensors/*` initially, with later normalization into system branches where useful | move | Same rationale as Era 1 sensors. | Create `vehicle/years/era2/sensors/`. | Low-to-medium risk. |
| `vehicle/era3/sensors/*` | `vehicle/years/era3/sensors/*` initially, with later normalization into system branches where useful | move | Same rationale as Era 1/2 sensors. | Create `vehicle/years/era3/sensors/`. | Low-to-medium risk; preserve 2000-2001 differences. |
| `vehicle/era3/evap.md` | `vehicle/systems/fuel/evap/era3-jtec.md` | move | EVAP is a stock subsystem fact and fits better under fuel/emissions system content. | Need EVAP branch under `vehicle/systems/fuel/` or a separate emissions branch if later added. | Medium risk; avoid burying an OBD-II-only topic. |
| `vehicle/era3/ignition/coil-rail.md` | `vehicle/systems/ignition/coil-rail/2000-2001.md` | move | System-specific ignition hardware reference. | Need durable ignition component-family branch. | Low-to-medium risk. |
| `vehicle/era3/ignition/distributor.md` | `vehicle/systems/ignition/distributor/era3-1996-1999.md` | move | Same as above. | Need durable ignition component-family branch. | Low-to-medium risk. |
| `vehicle/trans/aw4.md` | `vehicle/systems/transmission/aw4/overview.md` plus swap-only integration notes moved to `work/swaps/ecu/integration/aw4-tps.md` | split | Current file mixes stock transmission facts with ECU swap integration guidance. | Need transmission branch and ECU integration branch. | High risk if moved whole; would preserve taxonomy drift. |
| `vehicle/trans/manual.md` | `vehicle/systems/transmission/manual/overview.md` plus any swap-specific note moved to `work/swaps/ecu/compatibility/manual-transmission.md` | split | Same issue as AW4, though smaller. | Need transmission branch and a narrow compatibility leaf if required. | Medium risk. |
| `vehicle/systems/*/overview.md` scaffold files | same paths | keep | These already define the target system routers. | Future leaf creation only. | Low risk. |
| `swap/index.md` | `work/swaps/ecu/index.md` | move then deprecate | The current swap index is really the ECU swap workflow home. | Need `work/swaps/ecu/` router in place first. | Low risk if legacy path becomes a redirect router. |
| `swap/ecu-selection/requirements.md` | `work/swaps/ecu/selection/requirements.md` | move then deprecate old path | Clear ECU swap planning/procedure support content. | Need `work/swaps/ecu/selection/`. | Low risk. |
| `swap/ecu-selection/iac-strategy.md` | `work/swaps/ecu/selection/iac-strategy.md` | move then deprecate old path | Selection/planning content inside the ECU swap workflow. | Same as above. | Low risk. |
| `swap/ecu-selection/rusefi.md` | `work/swaps/ecu/selection/rusefi.md` | move then deprecate old path | Platform-choice content belongs under ECU swap selection. | Same as above. | Low risk. |
| `swap/ecu-selection/speeduino.md` | `work/swaps/ecu/selection/speeduino.md` | move then deprecate old path | Same as above. | Same as above. | Low risk. |
| `swap/ecu-selection/speeduino-ocelot.md` | `work/swaps/ecu/selection/speeduino-ocelot.md` | move then deprecate old path | Same as above. | Same as above. | Low risk. |
| `swap/ecu-selection/wideband.md` | `work/swaps/ecu/selection/wideband.md` or later `sourcing/wear-items/wideband-selection.md` if it becomes buyer-oriented | move | Currently supports swap planning; keep near selection first. | Need decision on whether the file stays planning-focused or becomes sourcing-focused. | Medium risk of split later. |
| `swap/wiring/grounds.md` | `work/swaps/ecu/wiring/grounds.md` | move then deprecate old path | Pure procedural integration content. | Need `work/swaps/ecu/wiring/`. | Low risk. |
| `swap/wiring/harness.md` | `work/swaps/ecu/wiring/harness-strategy.md` | move then deprecate old path | Pure procedural strategy content. | Need `work/swaps/ecu/wiring/`. | Low risk. |
| `swap/wiring/era1-renix-ocelot.md` | `work/swaps/ecu/wiring/era1-renix-ocelot.md` | move then deprecate old path | Narrow ECU swap procedure for a specific platform path. | Need `work/swaps/ecu/wiring/`. | Low risk. |
| `swap/wiring/aw4-tps.md` | `work/swaps/ecu/integration/aw4-tps.md` with cross-link to `vehicle/systems/transmission/aw4/overview.md` | move | This is ECU swap integration work, not generic stock transmission fact. | Need `work/swaps/ecu/integration/` and AW4 stock baseline destination. | Medium risk if stock AW4 facts are not separated first. |
| `swap/wiring/connectors/index.md` | `sourcing/connectors/index.md` plus work-branch links from `work/swaps/ecu/wiring/` | split | Folder mixes connector identification/replacement guidance with swap wiring usage. | Need `sourcing/connectors/` router and a rule for keeping procedure-only notes in `work/`. | High risk if moved as one block; taxonomy would stay muddled. |
| `swap/wiring/connectors/ecu-body/*` | `sourcing/connectors/ecu-body/*` | move | Primarily connector family identification and compatibility guidance. | Need `sourcing/connectors/ecu-body/`. | Medium risk if pinout/procedure content is embedded. |
| `swap/wiring/connectors/ev1-bosch/*` | `sourcing/connectors/ev1-bosch/*` | move | Primarily connector family and replacement-choice content. | Need `sourcing/connectors/ev1-bosch/`. | Low-to-medium risk. |
| `swap/wiring/connectors/ev6-uscar/*` | `sourcing/connectors/ev6-uscar/*` | move | Same as EV1 connector family guidance. | Need `sourcing/connectors/ev6-uscar/`. | Low-to-medium risk. |
| `swap/wiring/connectors/metri-pack/*` | `sourcing/connectors/metri-pack/*` | move | Same sourcing-style connector reference. | Need `sourcing/connectors/metri-pack/`. | Low-to-medium risk. |
| `swap/wiring/connectors/packard-56/*` | `sourcing/connectors/packard-56/*` | move | Same sourcing-style connector reference. | Need `sourcing/connectors/packard-56/`. | Low-to-medium risk. |
| `swap/wiring/connectors/renix-native/*` | `sourcing/connectors/renix-native/*` with stock-era context linked from `vehicle/years/era1/` | move | Connector family identification and replacement guidance fit sourcing better than procedure. | Need cross-links back to Renix stock wiring context. | Medium risk because this family is tightly tied to Renix-era stock architecture. |
| `swap/tuning/first-start.md` | `work/swaps/ecu/tuning/first-start.md` | move then deprecate old path | Clearly part of ECU swap execution and validation. | Need `work/swaps/ecu/tuning/`. | Low risk. |
| `swap/tuning/ignition.md` | `work/swaps/ecu/tuning/ignition.md` | move then deprecate old path | Same as above. | Same as above. | Low risk. |
| `swap/tuning/idle-tuning.md` | `work/swaps/ecu/tuning/idle-tuning.md` | move then deprecate old path | Same as above. | Same as above. | Low risk. |
| `swap/tuning/ve-table.md` | `work/swaps/ecu/tuning/ve-table.md` | move then deprecate old path | Same as above. | Same as above. | Low risk. |
| `swap/tuning/afr-targets.md` | `work/swaps/ecu/tuning/afr-targets.md` | move then deprecate old path | Same as above. | Same as above. | Low risk. |
| `swap/tuning/closed-loop.md` | `work/swaps/ecu/tuning/closed-loop.md` | move then deprecate old path | Same as above. | Same as above. | Low risk. |
| `swap/tuning/wot-tuning.md` | `work/swaps/ecu/tuning/wot-tuning.md` | move then deprecate old path | Same as above. | Same as above. | Low risk. |
| `swap/tuning/trail-tuning.md` | `work/swaps/ecu/tuning/trail-tuning.md` | move then deprecate old path | Same as above. | Same as above. | Low risk. |
| `book/README.md` | `book/index.md` or keep as README-only compatibility note | merge | The folder should have a stable router; `README.md` is useful but less canonical than `index.md`. | Need decision on repo-wide README vs `index.md` policy. | Low risk. |
| `book/audience.md` | `book/audience.md` | keep | Correct presentation-layer guidance in the right domain. | None. | Low risk. |
| `book/writing/style.md` | `book/writing/style.md` | keep | Correct presentation-layer guidance. | None. | Low risk. |
| `book/writing/callouts.md` | `book/writing/callouts.md` | keep | Correct presentation-layer guidance. | None. | Low risk. |
| `book/writing/safety.md` | `book/writing/safety.md` | keep | Correct presentation-layer guidance. | None. | Low risk. |
| `book/outline.md` | `book/projects/xj-ecu-swap-book/outline.md` | move | This is a project-specific deliverable outline, not a general root-level presentation rule. | Need agreement on project/deliverable branch naming under `book/`. | Medium risk if multiple deliverables emerge later and naming is inconsistent. |
| `agents/README.md` | `agents/index.md` or keep as README-only compatibility note | merge | The folder should have one stable router/entrypoint. | Need repo-wide policy for README vs `index.md`. | Low risk. |
| `agents/assistant/index.md` | `agents/assistant/index.md` | keep then revise | Correct path already exists, but its loading rules still assume ECU swap first. | Needs content update to follow domain-classification-first routing. | Medium risk of stale routing if not updated after migration. |
| `agents/book/index.md` | `agents/book/index.md` | keep then revise | Correct path already exists, but it still leans heavily on legacy role prompts and swap-centric framing. | Needs update after book/helper reorganization. | Medium risk. |
| `agents/assistant/README.md` | `agents/assistant/index.md` or deprecate | merge | Redundant once folder-local `index.md` is the stable entrypoint. | Need README policy decision. | Low risk. |
| `agents/book/README.md` | `agents/book/index.md` or deprecate | merge | Same as assistant README. | Need README policy decision. | Low risk. |
| `agents/writer.md` | keep temporarily; later `agents/helpers/writer.md` or equivalent | keep temporarily | Still actively referenced by `agents/book/index.md`; destination helper structure is not finalized. | Need naming decision for shared/helper agent files. | Medium risk if moved before references are updated. |
| `agents/technical.md` | keep temporarily; later `agents/helpers/technical.md` or equivalent | keep temporarily | Same as above. | Same as above. | Medium risk. |
| `agents/wiring.md` | keep temporarily; later `agents/helpers/wiring.md` or equivalent | keep temporarily | Same as above. | Same as above. | Medium risk. |
| `agents/tuning.md` | keep temporarily; later `agents/helpers/tuning.md` or equivalent | keep temporarily | Same as above. | Same as above. | Medium risk. |
| `agents/reviewer.md` | keep temporarily; later `agents/helpers/reviewer.md` or equivalent | keep temporarily | Same as above. | Same as above. | Medium risk. |
| `skillbuilding/index.md` | `skillbuilding/index.md` | keep | Already correctly placed as repo-building workflow guidance. | None. | Low risk; update wording to broader repo scope over time. |
| `skillbuilding/*` framework files | same paths | keep | These belong in the meta framework and should not be migrated into canonical technical branches. | None. | Low risk; only risk is scope drift if technical facts leak in. |

## Priority notes

### Best first-wave candidates
- era overview moves into `vehicle/years/`
- transmission baseline moves into `vehicle/systems/transmission/`
- ECU selection and tuning moves into `work/swaps/ecu/`
- `swap/index.md` replacement with `work/swaps/ecu/index.md`

### Hold until split rules are ready
- era diagnostics files
- era wiring files
- `vehicle/engine.md`
- `vehicle/trans/aw4.md`
- connector-family branch under `swap/wiring/connectors/`
- `book/outline.md`

## Redirect expectations
The following legacy paths should become compatibility notes after migration:
- `swap/index.md`
- `swap/ecu-selection/*`
- `swap/tuning/*`
- `vehicle/era*/overview.md`
- `vehicle/era3/1996-notes.md`
- `vehicle/trans/aw4.md`
- `vehicle/trans/manual.md`
- any moved `book/outline.md` path
