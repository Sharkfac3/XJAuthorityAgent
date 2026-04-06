# Prompt 5 — MJ Sourcing

Copy and paste the prompt below into a new chat session to run this step.

Prerequisite: Prompts 1–3 must be complete before running this one.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then read:
- `vehicle/mj/overview.md`
- `vehicle/mj/divergence.md`
- `sourcing/index.md`

## Your task

Build MJ sourcing content. The sourcing branch covers donor selection, interchange, OEM vs aftermarket tradeoffs, and connectors. Most XJ sourcing content applies to MJ for shared powertrain and drivetrain components. Your job is to document where MJ sourcing differs and add the MJ-specific sourcing that doesn't exist yet.

## What to build

### 1. MJ Donor Profile

Read `sourcing/donor-vehicles/index.md` and any existing donor vehicle files.

Create `sourcing/donor-vehicles/mj-comanche.md` covering:

**The MJ as a donor vehicle for XJ builds:**
- What an MJ donates to an XJ build: powertrain (engine, transmission, transfer case, axles) — all interchange
- What an MJ does NOT donate to XJ: body panels, doors, glass, interior pieces — nothing interchanges
- When to choose an MJ as a donor over another XJ: availability, lower prices on the market, clean drivetrain

**Using other vehicles as donors for an MJ:**
- XJ as a donor: all powertrain and drivetrain interchanges; body does not
- ZJ as a donor for MJ: same rules as ZJ-to-XJ (rear disc hardware, 4.0L HO engine, C8.25 axle)
- MJ-to-MJ body: the only source for cab, bed, and body panels — note rarity and market scarcity
- What to inspect when buying an MJ for donor use vs. for restoration

### 2. MJ Interchange

Read `sourcing/interchange/index.md` and existing interchange files.

Create or update interchange content for MJ:

**`sourcing/interchange/mj-xj-drivetrain.md`** — Document what interchanges directly between MJ and XJ:
- Engine (4.0L I-6 and 2.5L I-4): direct interchange
- AW4, AX-15, AX-5: direct interchange
- NP231, NP242: direct interchange
- Dana 30 front axle assemblies: direct interchange (same WMS, same geometry)
- Dana 35 rear axle: interchanges with caveats (verify WMS and spring perch differences)
- Chrysler 8.25 rear: interchanges with caveats (verify WMS)
- ECU (Renix and SBEC): direct interchange within era
- All electrical sensors: direct interchange within era

**`sourcing/interchange/mj-body.md`** — Document body non-interchange explicitly:
- Cab panels, doors, glass: MJ only — no XJ interchange
- Bed panels: MJ only
- Interior: MJ only
- This file exists to prevent sourcing mistakes — if someone is looking for MJ body parts, they need MJ-specific sources

### 3. MJ-specific OEM vs Aftermarket

Read `sourcing/oem-vs-aftermarket/index.md`.

Identify if any OEM-vs-aftermarket content is XJ-specific in a way that changes the answer for MJ. Most won't — the powertrain is shared. If any content is truly shared (cooling, sensors, brakes), add an MJ applicability note to the existing file rather than creating a new one.

If MJ-specific OEM vs aftermarket content is needed (e.g., MJ body seals, MJ-specific trim pieces), create `sourcing/oem-vs-aftermarket/mj-specific.md`.

### 4. MJ Wear Items

Read `sourcing/wear-items/index.md`.

The MJ uses the same fluids, filters, belts, hoses, and brake components as the XJ for all shared systems. Add MJ applicability notes to the relevant existing files rather than creating MJ-specific files unless the part numbers differ.

For brake components: if the MJ rear axle (leaf-spring drum or disc) uses different hardware than the XJ, document it in a note on the relevant brake sourcing file.

### 5. Update `sourcing/index.md`

Read it. Add a routing note for MJ sourcing — direct the expert agent to the MJ donor profile and MJ interchange files when sourcing questions are MJ-specific.

## Placement rules

- New MJ sourcing files go under the appropriate `sourcing/` subfolder
- Add applicability notes to existing XJ files where hardware is shared — do not duplicate
- Mark uncertain part interchange claims with `Status: needs verification` — incorrect interchange guidance is high-risk

## Output

Leave a plain-text summary listing:
1. New files created (with paths)
2. Existing files updated with MJ notes (with paths)
3. Any interchange claims marked as needing verification (list them explicitly — these are safety-critical)
