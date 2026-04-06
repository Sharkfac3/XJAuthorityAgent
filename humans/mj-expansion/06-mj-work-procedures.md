# Prompt 6 — MJ Work Procedures

Copy and paste the prompt below into a new chat session to run this step.

Prerequisite: Prompts 1–5 must be complete before running this one.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then read:
- `vehicle/mj/overview.md`
- `vehicle/mj/divergence.md`
- `work/index.md`

## Your task

Make the work branch MJ-aware. The vast majority of XJ work procedures apply directly to the MJ for shared systems. Your job is to:
1. Add MJ applicability notes to existing XJ work files where hardware is shared
2. Create MJ-specific procedure notes where the XJ procedure does not apply or differs

## Decision rule

- **Procedure is identical for MJ**: Add `## MJ Comanche applicability` note to the existing XJ file.
- **Procedure applies but with a meaningful caveat**: Add a note explaining the caveat.
- **Procedure is MJ-specific or does not apply at all**: Create a new file under `work/` in the appropriate subfolder.

## Work through each branch

### Maintenance (`work/maintenance/`)

Read `work/maintenance/index.md`. Then evaluate each maintenance subcategory:

- Most routine maintenance (oil change, coolant flush, belt replacement, filter service, differential fluid) applies identically to MJ — add MJ applicability notes to index and key leaf files
- Any maintenance item that is specific to the XJ body (windshield washer routing, tailgate seals, wagon-specific drainage) — note it does not apply to MJ
- MJ-specific maintenance items: bed floor drain plugs, bed seam sealing, cab-to-bed junction weatherstrip — create `work/maintenance/mj-specific.md` if there are meaningful MJ-only items

### Repairs (`work/repairs/`)

Read `work/repairs/index.md`. Evaluate each subcategory:

- Engine, fuel, ignition, transmission, transfer case, axle, and suspension repairs — add MJ applicability notes; procedures are shared for shared hardware
- Body repairs — XJ body repair content does not apply to MJ cab or bed. Note this clearly.
- Create `work/repairs/mj-body/index.md` if there is community-verified MJ body repair content worth capturing (cab corner repair, bed floor repair, cab-to-bed panel sealing). Do not create speculative content — only create this if you have verifiable facts to put in it.

### Upgrades (`work/upgrades/`)

Read `work/upgrades/index.md`. Evaluate each subcategory:

- Powertrain upgrades (stroker, injectors, grounds, headlights): shared hardware — add MJ applicability notes
- Body/interior upgrades (XJ-specific): note they do not apply to MJ
- Suspension upgrades: front suspension upgrades that target XJ coil springs and trackbar geometry apply to MJ front suspension. Rear suspension lift upgrades differ — MJ uses leaf springs in a pickup configuration with different spring rates and shackle geometry. Add caveat notes to any lift or suspension upgrade content.
- Create `work/upgrades/mj-suspension.md` covering MJ-specific rear suspension lift and spring upgrade considerations if verifiable content exists.

### Swaps (`work/swaps/`)

Read `work/swaps/index.md`. Evaluate each swap type:

**ECU swaps** (`work/swaps/ecu/`):
- Era 1 and Era 2 ECU swap content applies directly to MJ — add applicability notes to `work/swaps/ecu/index.md` (already partially done) and to key stage files
- Era 3 ECU content is XJ-only — add a note to era 3 files that they do not apply to MJ
- The 2.5L I-4 engine in MJ has different I/O requirements (4 injectors, not 6). Create `work/swaps/ecu/ecu-selection/mj-2.5l-requirements.md` documenting the 2.5L-specific ECU selection constraints.

**Axle swaps** (`work/swaps/axles/`):
- Axle swap procedures that apply to the Dana 30 front and Dana 35 / C8.25 rear will apply to MJ front axle work
- MJ rear axle is on a leaf-spring pickup setup — the spring perch, shackle, and U-bolt arrangement differs from XJ rear axle setup. Add caveats to any rear axle swap content.

**Engine swaps** (`work/swaps/engine/`):
- If XJ engine swap content exists, add MJ applicability notes. Shared engine means procedures are largely the same, but firewall, engine bay dimensions, and some accessory routing may differ.

### Inspections (`work/inspections/`)

Read `work/inspections/index.md`. Evaluate:

- Pre-purchase inspection: the XJ pre-purchase checklist covers powertrain, electrical, and structural items. Add an MJ applicability note and create `work/inspections/pre-purchase/mj-checklist.md` covering MJ-specific inspection points:
  - Cab floor rust (MJ cab has different rust patterns than XJ wagon)
  - Bed floor rust and bed rail condition
  - Cab-to-bed body mount condition
  - Pickup frame rail / unibody transition integrity
  - Bed-to-cab gap and alignment (indicator of structural twist)
  - Same powertrain checks as XJ (apply directly)

- Pre-swap inspections: add MJ applicability notes to existing pre-swap content; procedures are shared for shared systems.

### Setup and calibration (`work/setup-and-calibration/`)

- All setup and calibration content (engine TDC, drivability, alignment, ECU) applies to MJ for shared systems — add MJ applicability notes to the index and key files.

## Placement rules

- New MJ files go under the appropriate existing `work/` subfolder — do not create a separate `work/mj/` tree
- Add applicability notes to existing files rather than duplicating content
- Mark uncertain claims with `Status: needs verification`
- Do not create files for MJ-specific content you cannot source to verifiable community knowledge

## Output

Leave a plain-text summary listing:
1. Files updated with MJ applicability notes
2. New MJ-specific files created
3. Any content gaps identified (procedures with no MJ coverage and no verifiable content to fill them)
