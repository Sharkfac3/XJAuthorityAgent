# Repository Taxonomy

This repo serves two jobs at once:
1. preserve Jeep XJ technical knowledge that materially affects an open-source ECU swap
2. provide structured context to coding/writing agents with minimal token waste

The taxonomy below is intentionally strict so facts stay canonical, year-specific differences do not get flattened, and the repo stays centered on completing the swap rather than cataloging years for their own sake.

## Core rule
Store a fact in the narrowest file that can state it truthfully.

Examples:
- A fact true for all 1988–2001 4.0L XJs belongs in `vehicle/engine.md`
- A fact true only for 1991–1995 belongs in `vehicle/era2/...`
- A fact true only for 1996 belongs in `vehicle/era3/1996-notes.md`
- A how-to procedure belongs in `swap/...`, not `vehicle/...`
- A writing instruction belongs in `book/...`, not `vehicle/...`

## Canonical folder roles

### `vehicle/`
Source of technical facts about the Jeep XJ itself.

`vehicle/` exists to explain the stock system the swap is replacing.

Use for:
- engine facts
- transmission facts
- era-specific hardware and diagnostics
- year-range deltas
- sensor and trigger details

Do not use for:
- step-by-step swap procedures
- prose/style guidance
- agent behavior instructions

#### `vehicle/engine.md`
Cross-era invariants only.

Allowed:
- displacement
- firing order
- broad operating character
- facts true across the whole platform or clearly labeled year splits

Not allowed:
- era-specific connector details
- wiring procedures
- facts that only apply to one ECU era unless explicitly labeled

#### `vehicle/trans/`
Transmission facts only.
- `aw4.md` for AW4 behavior and constraints
- `manual.md` for manual-transmission constraints

#### `vehicle/era1/`, `vehicle/era2/`, `vehicle/era3/`
Era-specific fact domains.

Each era folder should follow this pattern where applicable:
- `overview.md` — era identity, major architecture, important caveats, links to leaf files
- `trigger.md` — crank/cam pattern facts
- `injectors.md` — injector specs and fitment facts
- `power-relay.md` — stock power-control architecture
- `wiring.md` — stock wiring architecture notes for that era
- `diagnostics.md` — stock diagnostic behavior and pre-swap checks
- `sensors/<sensor>.md` — sensor-specific facts for that era

#### Year-specific exceptions
If a single model year breaks the era pattern, give it its own file instead of forcing caveats into every leaf file.

Current example:
- `vehicle/era3/1996-notes.md`

Future examples if needed:
- `vehicle/era2/1991-notes.md`
- `vehicle/era3/2000-2001-coil-rail.md` if ignition notes outgrow the current split

### `swap/`
Source of swap execution knowledge.

This is the primary project axis. Era files support it, but the main question is always: what is required to make the aftermarket ECU work in the Jeep?

Use for:
- ECU selection
- wiring procedures
- connector identification
- tuning workflow
- swap-specific constraints

Do not use for:
- stock Jeep facts that belong in `vehicle/`
- book prose standards

#### `swap/ecu-selection/`
Decision support and platform comparison.

#### `swap/wiring/`
Swap wiring strategy and connector documentation.

Taxonomy inside `swap/wiring/`:
- `grounds.md` — grounding philosophy and required practices
- `harness.md` — harness-level strategy
- `aw4-tps.md` — swap-specific AW4 interface procedure
- `connectors/` — physical connector identification and pin-family notes

#### `swap/wiring/connectors/`
Connector family taxonomy.

- `index.md` — tiny router only
- one folder per connector family
- one `overview.md` per family where needed
- one leaf file per actual connector use-case when pinout/keying differs materially

Examples:
- `renix-native/tps.md`
- `packard-56/cps.md`
- `ecu-body/jtec.md`

#### `swap/tuning/`
Open-source-ECU tuning workflow and targets.

### `book/`
Presentation-layer guidance only.

Use for:
- audience definition
- chapter outline
- style rules
- callout conventions
- safety-writing conventions

Do not use for:
- canonical Jeep facts
- swap specs

### `agents/`
Agent behavior and loading instructions.

Use for:
- role behavior
- what files to load for a task
- review rules

Do not use for:
- new technical facts
- duplicate prose standards already covered by `book/`

### `docs/`
Repo governance for humans and agents.

Use for:
- taxonomy
- content audits
- migration notes
- future restructuring plans

This folder is not canonical technical source material for Jeep facts.

## Duplication policy
Some duplication is intentional and should remain lightweight.

Allowed duplication:
- `overview.md` files summarizing the era and pointing to leaf docs
- agent/router files naming canonical files to load
- book outline files pointing to source folders

Avoid duplication of:
- detailed specs
- connector pinouts
- sensor ranges
- year-specific exceptions

## Year and era policy
Preserving model-year differences matters more than minimizing file count.

Rules:
- Never collapse a year-specific exception into a generic era statement
- If a file must mention a split, label the exact year range
- Treat 1996 as a special-case file load whenever era 3 wiring, sensors, or diagnostics are involved
- If a new year-specific exception is discovered, add a dedicated note file rather than scattering caveats everywhere

## Token-efficiency policy
- Start with `AGENTS.md`
- Load one era overview, not all three, unless comparing eras
- Load leaf files only for the actual question
- Use `book/` only for writing/review tasks
- Use `agents/` only for role behavior
- Do not load `docs/` by default unless restructuring or auditing the repo
