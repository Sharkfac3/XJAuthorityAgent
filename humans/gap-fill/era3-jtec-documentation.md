# Gap Fill: Era 3 JTEC Documentation (1996–2001)

Copy and paste the prompt below into a new chat session with the Knowledgebase Builder agent active.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then read `vehicle/era2/overview.md` and all files under `vehicle/era2/` to understand the structure you are mirroring.

## Task

Era 3 (JTEC, OBD-II, 1996–2001) is nearly undocumented. Era 1 and Era 2 both have full coverage. Your job is to build Era 3 to the same depth.

## What to build

Create the following files, mirroring the structure of `vehicle/era2/`:

**Overview and identity:**
- `vehicle/era3/overview.md` — JTEC identity, OBD-II distinction from Era 2, what makes this era distinct, leaf file table, common failures

**Trigger system:**
- `vehicle/era3/trigger.md` — CPS type and location, cam sensor, distributor (1996–1999) vs DIS coil rail (2000–2001), open source ECU config notes

**Power relay:**
- `vehicle/era3/power-relay.md` — ASD relay behavior on JTEC (same concept as Era 2 but different PCM)

**Injectors:**
- `vehicle/era3/injectors.md` — Flow rate, fuel pressure (49 psi on Era 3, up from 39 psi on Era 2), impedance, connector type (EV6 on 1997+), upgrade options

**Sensors:**
- `vehicle/era3/sensors/map.md`
- `vehicle/era3/sensors/tps.md`
- `vehicle/era3/sensors/cts.md`
- `vehicle/era3/sensors/iat.md`
- `vehicle/era3/sensors/o2.md` — Era 3 has upstream AND downstream O2 (OBD-II requirement)
- `vehicle/era3/sensors/iac.md`

**Wiring and diagnostics:**
- `vehicle/era3/wiring.md` — PCM location, connector differences from Era 2, DIS wiring notes for 2000+
- `vehicle/era3/diagnostics.md` — OBD-II scan tool use, common DTCs for the 4.0L

## Key Era 3 facts to research and document

- JTEC PCM replaced SBEC in 1996
- OBD-II compliance: downstream O2 sensor added, full DTC library
- Fuel pressure increased to 49 psi in 1996+ (injectors are not interchangeable with Era 1/2 at same flow rate)
- Injector connector changed to EV6 (Multec) on 1997+ (1996 may be EV1 — verify)
- 2000–2001 XJ: distributorless ignition (DIS), coil rail waste spark — document this as a sub-generation
- 1996–1999: still distributor-based cam sync
- JTEC PCM is behind the glovebox, same general location as SBEC

Cross-reference `vehicle/era2/ho-engine.md` where relevant — the HO engine mechanical profile applies to Era 3 as well.

After building, update `vehicle/era3/overview.md` with a complete leaf file table and add Era 3 to any top-level indexes that reference Era 1 and Era 2.
Also be sure to triple check information with online sources as you work.