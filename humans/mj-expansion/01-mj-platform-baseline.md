# Prompt 1 — MJ Platform Baseline

Copy and paste the prompt below into a new chat session to run this step.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then read `vehicle/years/scope-boundary.md` to understand the current XJ and MJ scope definitions.

## Your task

Build the MJ platform baseline in `vehicle/`. The goal is a foundation that mirrors the depth of the XJ baseline for everything that is MJ-specific or MJ-divergent.

## What to build

### 1. `vehicle/mj/overview.md`

Create the MJ platform overview. Cover:

- What the MJ is: Jeep Comanche pickup truck, built on the XJ Cherokee unibody platform, produced 1986–1992
- Production years and body variants (short-bed 119.4 in wheelbase; long-bed 131 in wheelbase)
- Engine options by year:
  - 2.5L I-4 (all years — standard on Pioneer trim)
  - 4.0L I-6 (1987+ — standard on Eliminator and higher trim)
- Transmission options by engine:
  - AX-5 5-speed manual (2.5L)
  - AX-15 5-speed manual (4.0L)
  - AW4 4-speed automatic (both engines)
- Transfer case options: NP207 (early), NP231, NP242 (SelecTrac)
- Axle configuration: Dana 30 front, Dana 35 or Chrysler 8.25 rear
- Drivetrain options: 2WD and 4WD
- Control eras: Era 1 / Renix (1986–1990), Era 2 / SBEC OBD-I (1991–1992) — no Era 3
- A clear statement: "The MJ shares all powertrain, ECU, and drivetrain architecture with the XJ Cherokee for the overlapping era years. For shared systems, load the corresponding XJ files — MJ-specific files only exist where the platforms diverge."

### 2. `vehicle/mj/index.md`

Create a router for the MJ content branch. Include:
- What to load for MJ-specific questions
- Link to `vehicle/mj/overview.md`
- Link to `vehicle/mj/divergence.md` (you will create this next)
- Link back to the XJ era files for shared content (`vehicle/era1/`, `vehicle/era2/`)
- A note that Era 3 content does not apply to MJ

### 3. `vehicle/mj/divergence.md`

Create a file that documents every meaningful difference between the MJ and XJ. Organize by system. For each system note:
- Whether it is shared (with a cross-link to the XJ file) or divergent (with a brief description of how)

Systems to cover:
- Engine: shared 4.0L I-6 and 2.5L I-4
- Transmission: shared AX-5, AX-15, AW4
- Transfer case: shared NP231, NP242; NP207 was MJ-available but rare
- Front axle: shared Dana 30 (same specs and geometry)
- Rear axle: shared Dana 35 and C8.25 (same specs)
- Front suspension: shared coil-spring SLA geometry
- Rear suspension: leaf-spring — same leaf-spring design as XJ but different shackle geometry and spring rates for pickup duty
- Body structure: divergent — MJ is a pickup (cab + bed); body panels, doors, glass, and unibody floor sections do not interchange with XJ
- Interior: divergent — different dash options, different seat configurations, different trim packages (Eliminator, Pioneer, Laredo, Briarwood, Sport)
- ECU and electrical: shared Renix and SBEC architecture; Era 3/JTEC does not exist in MJ
- Wheelbase: divergent — short (119.4 in) and long (131 in) vs XJ's 101.4 in
- Towing and payload: divergent — higher tow ratings due to pickup platform; document factory tow ratings if verifiable

### 4. Update `vehicle/years/index.md`

Read it first. Then add a routing note: "For MJ year and era content → `vehicle/mj/index.md`" if it is not already there.

## Placement rules

- All new files go under `vehicle/mj/`
- Do not duplicate any content that already exists in `vehicle/era1/` or `vehicle/era2/` — cross-link instead
- Do not invent specs you cannot source to community-verified data or documented factory specs
- Mark any uncertain claim with `Status: needs verification`

## Output

After completing the files, leave a short plain-text summary of what was created and any claims you marked as needing verification.
