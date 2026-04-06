# Prompt 3 — MJ Vehicle Systems

Copy and paste the prompt below into a new chat session to run this step.

Prerequisite: Prompts 1 and 2 must be complete before running this one.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then read:
- `vehicle/mj/overview.md`
- `vehicle/mj/divergence.md`
- `vehicle/systems/index.md`

## Your task

Build MJ-specific vehicle system content for every system where the MJ diverges meaningfully from the XJ. For systems that are fully shared, add a MJ applicability note to the existing XJ file rather than creating a new one.

## Decision rule for each system

Before creating any file, check: **Does the MJ differ from the XJ in any way that would change an expert answer?**

- If **no**: Add a one-line MJ applicability note to the bottom of the existing XJ system file. Do not create a new MJ file.
- If **yes**: Create a `vehicle/mj/systems/<system>/` file documenting only the divergence. Cross-link to the shared XJ file for everything that is the same.

## Systems to evaluate

Work through each system below. Read the existing XJ system file before deciding.

### Fully shared systems (expected — verify before concluding)
These are expected to be fully shared with XJ. Read the XJ file, add an MJ applicability note if it is missing, and move on:
- `vehicle/systems/engine/` — 4.0L block, head, and injection architecture is shared
- `vehicle/systems/fuel/` — Same fuel system architecture within each era
- `vehicle/systems/ignition/` — Same ignition architecture within each era
- `vehicle/systems/transmission/` — AX-5, AX-15, AW4 are shared; verify nothing MJ-specific
- `vehicle/systems/transfer-case/` — NP231, NP242 shared; NP207 early MJ (verify)
- `vehicle/systems/axles/` — Dana 30 front, Dana 35 / C8.25 rear are shared
- `vehicle/systems/4wd/` — Same 4WD engagement architecture
- `vehicle/systems/charging-starting/` — Same alternator and starting architecture

### Systems that likely diverge (build MJ-specific content)

**Cooling system** (`vehicle/systems/cooling/`)
- Read `vehicle/systems/cooling/overview.md`
- MJ is a pickup with a different body, different airflow path, and potentially different radiator sizing
- Document: Did the MJ use the same radiator as XJ? Same fan shroud? Same thermostat housing? Were there engine-bay cooling differences due to the pickup body?
- Create `vehicle/mj/systems/cooling.md` if meaningful differences exist

**Electrical** (`vehicle/systems/electrical/`)
- Read `vehicle/systems/electrical/index.md` and `vehicle/systems/electrical/overview.md`
- The MJ shares the ECU and sensor electrical architecture with XJ but the body electrical (windows, locks, wipers, lighting, cluster) is truck-specific
- Document: What body electrical differs in MJ vs XJ? Same fuse box? Different wiring harness connectors for the cab? Different instrument cluster pinout?
- Create `vehicle/mj/systems/electrical.md` covering MJ body electrical divergence

**Body** (`vehicle/systems/body/`)
- Read `vehicle/systems/body/overview.md`, `vehicle/systems/body/rust-locations.md`, `vehicle/systems/body/water-intrusion.md`
- The MJ body is completely different from the XJ. None of the XJ body content applies to MJ body panels, doors, glass, or wagon structure.
- Create `vehicle/mj/systems/body.md` covering:
  - MJ cab structure (short-bed and long-bed)
  - MJ bed (the pickup bed — dimensions, tie-down points, floor materials)
  - MJ rust locations (known rust problem areas specific to the pickup body and bed structure)
  - MJ water intrusion points (different from XJ wagon — cab corners, bed-to-cab junction, tailgate)
  - Cross-link to XJ body content and note it does NOT apply

**Interior** (`vehicle/systems/interior/`)
- Read `vehicle/systems/interior/overview.md`
- MJ interior (dash, seats, trim) is truck-specific and not interchangeable with XJ
- Create `vehicle/mj/systems/interior.md` covering:
  - MJ dash variants by trim (Pioneer, Eliminator, Laredo, Briarwood)
  - MJ seat configurations (bucket seats, bench seat options)
  - MJ trim levels and package content
  - What XJ interior content does and does not apply to MJ

**Suspension** (`vehicle/systems/suspension/`)
- Read `vehicle/systems/suspension/overview.md`
- Front suspension: shared coil-spring SLA geometry
- Rear suspension: Both use leaf springs, but MJ spring rates and shackle geometry differ for pickup duty
- Create `vehicle/mj/systems/suspension.md` if rear suspension specs differ meaningfully

## Placement rules

- MJ divergence files live under `vehicle/mj/systems/`
- Applicability notes on existing XJ files go at the bottom of the file under a `## MJ Comanche applicability` heading
- Do not duplicate shared content — cross-link
- Mark uncertain claims with `Status: needs verification`

## Output

Leave a plain-text summary listing:
1. Systems confirmed as fully shared (MJ note added to XJ file)
2. Systems with MJ-specific files created (with file paths)
3. Any facts marked as needing verification
