# Prompt 4 — MJ Diagnostics

Copy and paste the prompt below into a new chat session to run this step.

Prerequisite: Prompts 1–3 must be complete before running this one.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then read:
- `vehicle/mj/overview.md`
- `vehicle/mj/divergence.md`
- `diagnostics/index.md`

## Your task

Make the diagnostics branch MJ-aware. Most XJ diagnostic content applies directly to the MJ because the systems are shared. Your job is to identify which diagnostic files need an MJ applicability note, which need an MJ caveat, and where MJ-specific symptom content is needed.

## Decision rule for each diagnostic category

- **Fully shared diagnostic content**: Add `## MJ Comanche applicability` note to the existing file — "This diagnostic applies to MJ [years] with the same architecture."
- **Shared content with an MJ caveat**: Add a note explaining the specific exception (e.g., an Era 3 diagnostic that has no MJ equivalent).
- **MJ-specific symptoms that don't exist in XJ**: Create a new diagnostic file under the appropriate `diagnostics/` subcategory.

## Work through each diagnostic category

Read the index for each category listed in `diagnostics/index.md`, then evaluate the leaf files.

### Engine diagnostics
- Era 3 control-system triage (`diagnostics/engine/era3-control-system-triage.md`) — **XJ only**. Add a note: "Era 3 / JTEC does not exist in the MJ. MJ users with control system symptoms should use Era 1 or Era 2 content."
- Other engine diagnostic leaves — evaluate each for MJ applicability. Most should be shared (same engine). Add notes accordingly.

### Fuel diagnostics
- No-prime diagnosis — evaluate whether MJ fuel system differences (if any) change the diagnosis. If the pump, relay, and wiring are the same, note it. If MJ has a different relay arrangement in Era 1, flag it.

### Ignition diagnostics
- No-spark diagnosis — same ignition architecture within era; add MJ applicability note.

### Cooling diagnostics
- Evaluate overheating and coolant loss leaves for MJ applicability.
- If MJ has different cooling specs (radiator, fan shroud) that change diagnosis thresholds, note it.

### Charging and starting diagnostics
- Shared architecture — add MJ applicability notes.

### Transmission diagnostics (AW4)
- AW4 is identical in XJ and MJ — add MJ applicability note.

### Transfer-case diagnostics (NP231)
- NP231 is shared — add MJ applicability note.
- NP207 early MJ: if there is no existing NP207 diagnostic content, note the gap but do not create speculative content.

### Driveline diagnostics
- Axle noise, driveshaft vibration — shared hardware; add MJ applicability notes.
- MJ driveshaft: the MJ has a different driveshaft length and potentially different vibration characteristics due to the longer wheelbase. Note this difference if it changes diagnosis.

### Steering and suspension diagnostics
- Death wobble — XJ and MJ share the same front suspension architecture; add MJ applicability note.
- MJ rear suspension is leaf-spring pickup geometry — if there are rear-end vibration or handling symptoms specific to the pickup rear, create `diagnostics/steering-suspension/mj-rear-suspension.md`.

### Body electrical diagnostics
- Ground fault diagnosis, gauge cluster — evaluate for MJ. The MJ has a different instrument cluster and body electrical harness. Note where XJ wiring diagrams do not apply to MJ.

### Body and interior diagnostics
- Water intrusion, rust inspection — MJ has completely different body structure. These diagnoses do not apply as written.
- Create `diagnostics/body-and-interior/mj-water-intrusion.md` — MJ-specific water entry points (cab corners, cab-to-bed junction, bed floor, tailgate).
- Create `diagnostics/body-and-interior/mj-rust-inspection.md` — MJ-specific structural rust inspection (cab floor, bed structure, frame-to-unibody transition, cab corners).

## Update `diagnostics/index.md`

Read it. Add a section or note that clarifies:
- Which diagnostic branches apply to MJ (most of them)
- Which are XJ-only (Era 3 content)
- Where MJ-specific leaves exist

## Placement rules

- New MJ diagnostic files go under the appropriate `diagnostics/<category>/` folder
- Do not create MJ diagnostic files that duplicate XJ content — add notes to existing files instead
- Mark uncertain claims with `Status: needs verification`

## Output

Leave a plain-text summary listing:
1. Files updated with MJ applicability notes
2. New MJ-specific diagnostic files created
3. Era 3 XJ-only files marked as such
4. Any gaps flagged (symptoms with no coverage for either platform)
