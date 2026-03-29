# Gap Fill: Wiring Restoration

Copy and paste the prompt below into a new chat session with the Knowledgebase Builder agent active.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then read `work/restoration/wiring/index.md` and any existing content under `work/restoration/` before writing.

## Task

`work/restoration/wiring/` is a stub referenced by sourcing files but has no content. Build it out. This section covers restoring degraded factory wiring on high-mileage XJs — it is not the ECU swap wiring section (that lives under `work/swaps/ecu/wiring/`).

## What to build

**`work/restoration/wiring/index.md`** — update the existing router with a full leaf table

**`work/restoration/wiring/inspection.md`**
- How to inspect an XJ wiring harness: what to look for (brittle insulation, rodent damage, splice corrosion, melted sections near exhaust, chafed ground wires)
- Where the XJ harness is most vulnerable (firewall pass-throughs, engine bay near exhaust manifold, floor harness under carpet near drain plug areas)
- Tools needed for inspection

**`work/restoration/wiring/ground-straps.md`**
- All factory ground strap locations on the XJ
- Most commonly corroded: engine block to chassis, head to firewall, battery negative to chassis, body to frame
- Prep and replacement procedure
- Symptoms of bad grounds (random electrical gremlins, gauge erratic behavior, hard starts)
- Cross-reference `vehicle/era1/wiring.md` and `vehicle/era2/wiring.md` for era-specific ground notes

**`work/restoration/wiring/connector-rehab.md`**
- When to rehouse vs. replace a connector
- Cleaning corroded pins: electrical contact cleaner, dielectric grease application
- Identifying and replacing broken locking tabs
- EV1 injector connector brittle tab procedure (cross-reference `vehicle/era1/injectors.md` and `vehicle/era2/injectors.md`)
- Metri-Pack 150 re-pin procedure

**`work/restoration/wiring/harness-repair.md`**
- Acceptable splice methods: solder + heat shrink preferred; no push-in connectors
- When to replace a full sub-harness vs. repair
- Injector sub-harness replacement (full 6-injector pigtail kits available from XJ suppliers)
- Firewall connector cleaning and re-pinning

**`work/restoration/wiring/firewall-connector.md`**
- Location of the main firewall multi-pin connectors
- Common corrosion patterns
- Pin extraction and cleaning procedure
- Which pins are highest priority (CPS, O2, injectors)

Keep this section focused on restoration of factory wiring on existing vehicles. Swap-specific wiring belongs in `work/swaps/ecu/wiring/`. Link to that section where relevant rather than duplicating content.
Also be sure to triple check information with online sources as you work.