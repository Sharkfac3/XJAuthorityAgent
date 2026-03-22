# Migration Plan

## Purpose
Plan the migration from the current ECU-swap-centered repo into the broader Jeep XJ architecture without losing canonical facts, provenance, or routing clarity.

## Scope
This document plans migration only.
It does not perform the full move, rewrite, or split.

## Ground rules
- Preserve canonical facts.
- Do not silently discard content.
- Keep current canonical paths valid until replacement paths exist.
- Separate file moves from content rewriting.
- Prefer compatibility notes and redirects over abrupt path removal.
- Flag broad or mixed-purpose files before moving them.

## Current-state audit summary
The repo already has a strong scaffold for the target architecture, but most mature content is still concentrated in legacy ECU-swap paths:

- `vehicle/` contains the stock fact base, but much of it is still era-first and swap-support-oriented.
- `swap/` contains the densest procedural content and still acts like the practical center of the repo.
- `book/` mostly fits its intended role, but `book/outline.md` is still tied to the older ECU-swap-book identity.
- `agents/` has begun the folder migration (`agents/assistant/`, `agents/book/`) but still relies on top-level legacy role prompts.
- `skillbuilding/` is already appropriately separated as meta/governance workflow support and should not be merged into canonical knowledge trees.

The main migration challenge is not raw file movement. It is disentangling mixed-purpose content so stock facts, procedures, diagnostics, sourcing, and agent behavior each land in the right domain.

## 1. Migration strategy

### Strategy summary
Use a phased migration with compatibility layers.
Do not rewrite the whole repo in one pass.

### Core approach
1. **Stabilize destination branches first**
   - Treat the new scaffold under `vehicle/`, `work/`, `diagnostics/`, and `sourcing/` as the target state.
   - Add or refine local router files before moving dense content.

2. **Move low-risk routers before dense leaves**
   - Move or replace index-style files first.
   - Keep redirect notes in legacy paths.

3. **Migrate by content type, not just by folder**
   - Stock facts stay in `vehicle/`.
   - Procedures move to `work/`.
   - Symptom-first and test-sequence material moves to `diagnostics/`.
   - connector, donor, and replacement-selection content moves to `sourcing/`.

4. **Split mixed-purpose files before or during migration**
   - Do not lift-and-drop broad files into the new tree if they still mix facts, procedures, and diagnostics.
   - Preserve provenance by noting the source file in the destination file's transition note.

5. **Leave `swap/` as a compatibility branch during the transition**
   - `swap/` remains canonical until its replacements exist.
   - When a migrated destination is ready, the legacy file should become a redirect or compatibility note rather than silently disappearing.

6. **Treat the migration as wave-based**
   - Wave 1: low-risk path normalization and router alignment.
   - Wave 2: ECU work-branch migration from `swap/` into `work/swaps/ecu/`.
   - Wave 3: extraction of diagnostics and sourcing from mixed legacy files.
   - Wave 4: cleanup, redirects, and agent/book alignment.

## 2. Migration order

### Wave 0 — freeze the conceptual model
Do first:
- Keep `docs/project-reframe.md`, `docs/repo-taxonomy.md`, and `docs/structure-map.md` as the architectural source of truth.
- Use this migration plan and `docs/migration-map.md` as the execution reference.

### Wave 1 — low-risk structural alignment
Goal: normalize obvious path mismatches without changing technical meaning.

Recommended moves:
- Normalize legacy era content into `vehicle/years/...` paths while preserving file meaning.
- Normalize `vehicle/trans/...` into `vehicle/systems/transmission/...`.
- Replace README-style folder homes with `index.md` where helpful, leaving README compatibility notes if needed.
- Keep content mostly intact during this wave.

### Wave 2 — establish the ECU work branch
Goal: make `work/swaps/ecu/` the target home for active ECU swap execution content.

Recommended moves:
- `swap/index.md` → `work/swaps/ecu/index.md`
- `swap/ecu-selection/*` → `work/swaps/ecu/selection/*`
- procedural wiring content under `swap/wiring/` → `work/swaps/ecu/wiring/` or `work/swaps/ecu/integration/`
- tuning/first-start content under `swap/tuning/` → `work/swaps/ecu/tuning/`

Keep `swap/` as a redirecting compatibility branch after each destination exists.

### Wave 3 — extract misplaced diagnostics and sourcing
Goal: stop storing non-fact and non-procedure content in the wrong branch.

Recommended moves:
- Era `diagnostics.md` files: split into `diagnostics/` and `work/inspections/` material.
- Connector family identification and replacement guidance: move from `swap/wiring/connectors/` into `sourcing/connectors/`.
- Any donor or selection guidance hidden in procedural files should move to `sourcing/`.

### Wave 4 — align support layers
Goal: make routing and presentation match the new repo identity.

Recommended moves:
- Broaden `agents/assistant/index.md` so it starts by classifying task type, not by always loading swap content.
- Keep `agents/book/index.md`, but make its technical loading rules domain-aware beyond ECU swaps.
- Move or nest project-specific book artifacts such as the ECU-swap outline under a more specific branch.
- Keep `skillbuilding/` as a meta-framework and update references so it targets the broader repo, not only swap expansion.

### Wave 5 — cleanup and controlled deprecation
Goal: reduce ambiguity without breaking old routes.

Actions:
- Replace migrated legacy files with short redirect/compatibility notes.
- Mark legacy paths as transitional in local indexes.
- Remove true duplicates only after destination content is verified against source meaning.

## 3. Low-risk first moves
These can happen early because they are mostly path normalization, not heavy rewriting.

### High-confidence low-risk moves
- `vehicle/era1/overview.md` → `vehicle/years/era1/overview.md`
- `vehicle/era2/overview.md` → `vehicle/years/era2/overview.md`
- `vehicle/era3/overview.md` → `vehicle/years/era3/overview.md`
- `vehicle/era3/1996-notes.md` → `vehicle/years/1996-notes.md` or `vehicle/years/era3/1996-notes.md` after one convention is chosen
- `vehicle/trans/aw4.md` → `vehicle/systems/transmission/aw4/overview.md` as an initial holding move
- `vehicle/trans/manual.md` → `vehicle/systems/transmission/manual/overview.md`
- `swap/index.md` → `work/swaps/ecu/index.md` with `swap/index.md` retained as a compatibility router
- `swap/ecu-selection/*` → `work/swaps/ecu/selection/*`
- `swap/tuning/*` → `work/swaps/ecu/tuning/*` as a first-pass procedural home

### Why these are low-risk
- They already fit the target taxonomy.
- Their main problem is path placement, not content ambiguity.
- They can preserve wording initially and be refined later.

## 4. Items that should stay where they are temporarily
These items should remain in place until their destination structure is ready or their content is split.

### Keep temporarily in `swap/`
- `swap/wiring/connectors/`
  - Reason: the content mixes connector identification, replacement guidance, and swap-specific harness use.
  - Action later: split between `sourcing/connectors/` and `work/swaps/ecu/wiring/`.

- `swap/wiring/aw4-tps.md`
  - Reason: it bridges stock transmission behavior and swap integration.
  - Action later: move after the `work/swaps/ecu/integration/` and `vehicle/systems/transmission/aw4/` branches are both stable.

### Keep temporarily in `vehicle/`
- `vehicle/engine.md`
  - Reason: it is a useful canonical engine baseline, but it is still a broad root-level file and includes swap-oriented notes.
  - Action later: split into `vehicle/systems/engine/4.0l/overview.md` plus any swap-context note that belongs under `work/swaps/ecu/`.

- `vehicle/era*/diagnostics.md`
  - Reason: these files mix actual diagnostics, pre-swap inspection, and era-specific context.
  - Action later: split rather than direct-move.

- `vehicle/era*/wiring.md`
  - Reason: they combine stock architecture with swap-adapter relevance.
  - Action later: preserve as year-era stock wiring context, then extract procedure-only notes into `work/swaps/ecu/wiring/`.

### Keep temporarily in `agents/`
- legacy top-level role prompts: `agents/writer.md`, `agents/technical.md`, `agents/wiring.md`, `agents/tuning.md`, `agents/reviewer.md`
  - Reason: active folder-local replacements are not fully established.
  - Action later: move into a stable helper structure and update `agents/book/index.md` and other agent routers.

## 5. Files that need redirects or compatibility notes
Redirects are needed anywhere an old path is likely to remain referenced by humans, agents, or other docs.

### Must-have redirects or compatibility notes
- `swap/index.md`
- all migrated `swap/ecu-selection/*.md`
- all migrated `swap/tuning/*.md`
- `vehicle/era1/overview.md`
- `vehicle/era2/overview.md`
- `vehicle/era3/overview.md`
- `vehicle/era3/1996-notes.md`
- `vehicle/trans/aw4.md`
- `vehicle/trans/manual.md`
- any agent file path referenced directly by `agents/book/index.md` or other routers
- `book/outline.md` if moved into a more specific project branch

### Redirect note format
Each compatibility file should say:
- this path is transitional
- the new canonical path
- whether the content has been moved as-is, split, or partially migrated
- what still remains at the legacy path, if anything

## 6. Where old ECU-swap concepts become one branch of a broader system
The old repo center should become a narrower branch of the new architecture.

### Primary branch mapping
- old ECU execution center: `swap/`
- new ECU execution center: `work/swaps/ecu/`

### Broader-system mapping
- stock engine-management facts that were only written for swap prep remain or move under `vehicle/`
- fault isolation currently embedded in era notes moves under `diagnostics/`
- connector-family and practical parts-choice guidance moves under `sourcing/`
- project-execution steps live under `work/swaps/ecu/`
- reusable tuning and validation methods may later branch from `work/swaps/ecu/` into `work/setup-and-calibration/` if they become broader than ECU swaps

### Example conversions
- era stock trigger facts: `vehicle/years/eraX/...` or later `vehicle/systems/ignition/...`
- ECU platform choice: `work/swaps/ecu/selection/`
- harness strategy and grounds: `work/swaps/ecu/wiring/`
- AW4 swap interaction: `work/swaps/ecu/integration/` plus stock baseline in `vehicle/systems/transmission/aw4/`
- connector-family replacement guidance: `sourcing/connectors/`
- first-start and validation: `work/swaps/ecu/tuning/` or later `work/setup-and-calibration/engine-management/`

## 7. What to do with existing `agents/`, `book/`, and `skillbuilding/` materials

### `agents/`
Keep `agents/` as behavior and routing only.
Do not move technical facts into it.

Planned direction:
- keep `agents/assistant/index.md` and `agents/book/index.md` as the primary entrypoints
- update both to use the broader domain-classification model
- keep top-level legacy role prompts temporarily
- later move legacy role prompts into a stable helper branch such as `agents/helpers/` or per-agent local helper files once naming is agreed

### `book/`
Keep `book/` as presentation-only guidance.
Most current files already fit.

Planned direction:
- keep `book/audience.md` and `book/writing/*` in place
- review `book/outline.md` because it reflects the older ECU-swap-book deliverable rather than the broader repo identity
- move project-specific outline material into a scoped branch if multiple deliverables are expected, for example `book/projects/xj-ecu-swap-book/outline.md`

### `skillbuilding/`
Keep `skillbuilding/` where it is.
It already matches the target model.

Planned direction:
- do not migrate `skillbuilding/` into technical branches
- update its routing examples, backlog framing, and audit language so they apply to the broader Jeep XJ repo rather than only ECU swap coverage
- use it as the operational framework for later migration waves, audits, and gap-filling

## Broad files that need splitting before full migration
These should be explicitly split rather than moved whole.

- `vehicle/engine.md`
  - mixes durable stock baseline with swap-oriented language
- `vehicle/trans/aw4.md`
  - mixes stock transmission facts with ECU swap integration guidance
- `vehicle/trans/manual.md`
  - contains stock baseline plus swap notes
- `vehicle/era1/diagnostics.md`
- `vehicle/era2/diagnostics.md`
- `vehicle/era3/diagnostics.md`
  - each mixes diagnostics with pre-swap inspection workflow
- `vehicle/era1/wiring.md`
- `vehicle/era2/wiring.md`
- `vehicle/era3/wiring.md`
  - each mixes stock wiring architecture with adaptation guidance
- `swap/wiring/connectors/index.md` and family branches
  - mix sourcing-style connector identification with procedural swap use
- `book/outline.md`
  - still serves a legacy project identity rather than a durable presentation rule

## Misplaced content to flag under the new taxonomy
- diagnostics content currently stored under `vehicle/era*/diagnostics.md`
- sourcing/connector-selection content currently stored under `swap/wiring/connectors/`
- swap-specific procedural notes embedded in some stock fact files such as `vehicle/trans/aw4.md`
- project-specific deliverable framing in `book/outline.md`
- legacy top-level agent prompts that should eventually live under a clearer agent-helper structure

## Dependency and blocker summary

### Dependencies
- destination router files under `work/`, `diagnostics/`, and `sourcing/`
- one chosen convention for `vehicle/years/` era and year-specific file placement
- one chosen convention for agent helper-file placement
- redirect-note format

### Main blockers
- mixed-purpose legacy files that cannot be moved intact without creating drift
- unresolved decision on whether some ECU tuning content remains under `work/swaps/ecu/` or eventually moves into `work/setup-and-calibration/`
- unresolved split boundary between stock wiring facts, swap wiring procedure, and connector sourcing

## Success criteria
The migration is successful when:
- stock facts are routable through `vehicle/`
- ECU swap execution is routable through `work/swaps/ecu/`
- diagnostics no longer hide in stock-reference files
- sourcing decisions no longer hide in wiring procedure folders
- `agents/` only routes and instructs
- `book/` only governs presentation
- legacy paths still provide compatibility until all references are updated
