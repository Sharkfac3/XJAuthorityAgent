# Gap Fill: Transmission and Transfer Case

Copy and paste the prompt below into a new chat session with the Knowledgebase Builder agent active.

---





probably about to limit out on this






You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then check `vehicle/index.md` and `work/index.md` to understand existing structure before writing anything.

## Task

The XJ Cherokee transmission and transfer case are undocumented. Build foundational coverage for both.

## Transmissions in scope

The XJ Cherokee came with these transmissions depending on year and engine:

**Manual:**
- BA-10/5 (Peugeot) — 1987–1989, known weak link, commonly replaced
- AX-15 (Aisin) — 1989–1995, robust, desirable

**Automatic:**
- AW4 (Aisin Warner) — 1987–2001, the only automatic offered with the 4.0L

## Transfer cases in scope

- NP231 — part-time, slip-yoke, most common
- NP242 — full-time/part-time selectable (Command-Trac II), less common
- NP207 — early, less common, predecessor to NP231

## What to build

**Vehicle-level identity files:**
- `vehicle/systems/transmission/overview.md` — which trans came in which years, gear ratios, known strengths/weaknesses, swap considerations
- `vehicle/systems/transmission/aw4.md` — AW4 identity, shift solenoids, TPS interaction, fluid spec, common failures
- `vehicle/systems/transmission/ax15.md` — AX-15 identity, fluid spec, gear ratios, common failures
- `vehicle/systems/transmission/ba10.md` — BA-10/5 identity, why it fails, why builders replace it

- `vehicle/systems/transfer-case/overview.md` — which t-case came in which years, what distinguishes NP231 from NP242
- `vehicle/systems/transfer-case/np231.md` — slip yoke vs. SYE (slip yoke eliminator), output shaft spline count, fluid spec, chain wear
- `vehicle/systems/transfer-case/np242.md` — selectable 4WD operation, when full-time is appropriate, fluid spec

## Key facts to capture

- AW4 shift behavior depends on TPS signal from the ECU — this is already cross-referenced in `vehicle/era2/sensors/tps.md` and `vehicle/era1/sensors/tps.md`; link back to those files
- BA-10/5 is a known weak point; AX-15 is a popular direct swap replacement
- NP231 slip yoke causes driveshaft vibration at lifted ride heights — SYE is the standard fix
- NP231 and NP242 have different output shaft configurations affecting driveshaft requirements
- Fluid specs matter: AW4 uses ATF+4 (not Dexron), NP231/NP242 use ATF

Place all files under `vehicle/systems/transmission/` and `vehicle/systems/transfer-case/`. Update `vehicle/systems/` index to include these.
Also be sure to triple check information with online sources as you work. If its not backed by forum posts we dont want the information in our repository.