# Firewall Connector

## Purpose
Service the main firewall multi-pin connectors that pass the engine harness through the firewall. Corrosion at these connectors is a documented source of electrical gremlins on all XJ years.

---

## Connector locations by era

### C101 — 1987–1988 (Renix)
**Location:** Driver's side firewall, above the brake booster/master cylinder.
**Mounting:** Attached to the firewall with one screw.
**Description:** A large multi-pin connector that passes nearly every critical engine signal — injectors, sensors, ECU grounds, and TCU signals — through the firewall in a single location.

C101 is the highest-risk connector in the XJ lineup. Community documentation on NAXJA notes that it "was a source of electrical resistance even when the vehicles were new." Chrysler eliminated C101 starting with the 1989 model year. On 1987–1988 vehicles, cleaning C101 is a mandatory first step before any electrical diagnosis.

**Cleaning procedure:** Unscrew the connector from the firewall. Separate the two halves. Soak in electrical contact cleaner. Work a soft brush through all pin cavities. Allow to fully dry. Inspect each pin for corrosion or pushed-back seating. Apply dielectric grease to all pins before reassembly.

Source: NAXJA community documentation on the 88XJ wiring harness and C101 corrosion.

### Main engine harness firewall pass-through — 1989–1996
**Location:** Driver-side firewall, routed through a rubber grommet. The engine harness enters the cab through this pass-through and connects to the under-dash fuse block and instrument cluster.
**Description:** No discrete multi-pin bulkhead connector — the harness passes through the grommet as a bundle. The grommet itself is the primary failure point: it dries out, cracks, and allows water to track down the wires into the cabin.

Inspect the grommet for cracking and replace if deteriorated. Seal any gaps with silicone RTV to prevent water intrusion.

### C107 — 1997–2001 (JTEC / PDC era)
**Location:** Driver's side firewall, behind the battery and PDC box.
**Description:** A large multi-pin bulkhead connector that passes the engine harness through the firewall. Documented by the community as a common source of random electrical gremlins on 1997–2001 XJs.

Failure modes:
- Pin corrosion from moisture tracking along wire insulation
- Pins backing out of the housing (secondary lock allows them to migrate under vibration)
- Connector housing not fully seated after service

Community-documented fix: Unplug C107, clean all pins with contact cleaner, apply dielectric grease, verify all pins are fully seated, and reconnect firmly. This is described on XJ forums as a 15-minute fix for a wide range of unexplained electrical problems on late-model XJs.

Source: XJ community documentation on electrical gremlins; multiple JeepForum and Cherokee Talk threads confirm C107 as a first-stop diagnosis for 97-01 XJ electrical issues.

---

## Common corrosion patterns

- **Pin face oxidation:** Green or white powdery oxidation on pin faces. Cleans well with contact cleaner and a brush in most cases.
- **Pin socket collapse:** Female pin sockets that have spread open from previous mating — no longer make firm contact with male pins. These must be re-tensioned with a pin pick or replaced.
- **Water intrusion:** Rust-colored staining inside the connector housing indicates water has tracked in through a cracked grommet or failed seal. Inspect for underlying wire corrosion — it may have wicked several inches up the wire insulation.
- **Pushed-back terminals:** Terminals that have migrated rearward in their cavities. These make intermittent contact and are a common cause of mystery electrical faults. Re-seat and verify secondary lock engagement.

---

## Pin extraction and cleaning procedure

### Tools required
- Electrical contact cleaner
- Soft brush (toothbrush or connector brush)
- Dental pick or fine scribe
- Appropriate terminal release tool for the connector series
- Dielectric grease
- Replacement terminals if needed (match to connector series)

### Procedure
1. **Disconnect battery negative** before working on any firewall connector.
2. **Unplug the connector.** Release the secondary lock (slider or push-tab) before attempting to separate the halves. Forcing a locked connector cracks the housing.
3. **Separate the halves.** Inspect both faces for visible corrosion, pushed pins, and debris.
4. **Spray with contact cleaner.** Saturate pin cavities. Allow to penetrate 30 seconds and drain.
5. **Brush all pin faces** — use a soft brush. Do not use abrasive material inside pin cavities.
6. **Re-spray and allow to fully evaporate.**
7. **Inspect each pin cavity.** Every pin should be fully forward in its cavity and retained by its locking lance. Use a dental pick to gently test seating — a pin that moves rearward under light pressure needs to be re-seated or replaced.
8. **Apply dielectric grease** to the mating face of one connector half — a thin coat covering all pins. Do not pack the cavities.
9. **Reconnect and engage the secondary lock fully.** A partially engaged secondary lock allows pins to back out under vibration.

### When to re-pin
If a pin is corroded beyond what contact cleaner removes, or the socket has collapsed and no longer makes firm contact, it must be extracted and replaced. Use the correct terminal release tool for the connector series. See `connector-rehab.md` for general terminal extraction procedure.

---

## Highest-priority pins

When time is limited or only specific symptoms are present, prioritize these circuits:

| Circuit | Why it matters |
|---------|---------------|
| CPS (crankshaft position sensor) | No-start or random stall if degraded |
| O2 sensor signal | Closed-loop fueling error, false codes |
| Injector power and grounds | Misfire or dead injector |
| ECU sensor ground | Corrupts all 5V sensor readings simultaneously |
| TPS signal | Fueling and shift quality on AW4-equipped vehicles |

---

## Cross-references
- General connector cleaning and re-pin: `connector-rehab.md`
- Era 1 wiring specifics (C101 context): `vehicle/era1/wiring.md`
- Era 2 wiring specifics: `vehicle/era2/wiring.md`
- Era 3 wiring specifics (C107 context): `vehicle/era3/wiring.md`
- ECU swap firewall connector notes: `work/swaps/ecu/wiring/`
