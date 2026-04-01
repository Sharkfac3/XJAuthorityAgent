# Harness Repair

## Purpose
Repair or replace damaged sections of the factory XJ wiring harness. Covers splice methods, sub-harness replacement, and when full replacement is warranted over repair.

---

## Splice methods

### The correct method: open-barrel crimp + adhesive-lined heat shrink

Crimping is the OEM standard for automotive wiring — every factory harness, on every XJ and every production vehicle, was built with crimped terminals, not solder. High Performance Academy (hpacademy.com) documents extensively why this is the case: a properly executed open-barrel crimp is stronger than the wire itself — under tensile load, the conductor strands fail before the crimp does.

**Open-barrel (bare metal) crimp connectors are the correct tool for wire splices.** These are not the same as the pre-insulated plastic-jacketed butt connectors sold at auto parts stores — see the "What not to use" section below.

#### Procedure

1. Strip both wire ends 3/4 inch using a proper wire stripper. Do not nick conductor strands — damaged strands reduce the crimp cross-section and create a weak point.
2. Select a bare copper open-barrel splice crimp sized to the wire gauge.
3. Insert both stripped ends into the barrel crimp.
4. Crimp both ends using a **ratcheting crimper with the correct die for the terminal series**. A ratcheting crimper prevents under-crimping by holding the jaws until the full crimp cycle is complete. A generic plier-type crimper does not produce a gas-tight joint.
5. Visually inspect the crimp — 1–2 mm of bare conductor should be visible at the end of the barrel, confirming the wire is fully seated. An improperly seated wire will back out of the barrel and fail.
6. Slide adhesive-lined (glue-lined) heat shrink over the completed crimp and shrink with a heat gun. The adhesive liner must flow out the ends of the tube — this seals the joint against moisture. Without the adhesive liner, the heat shrink is only mechanical protection, not a moisture seal.

#### Tooling note
A quality ratcheting crimper designed for open-barrel terminals (Iwiss, Knipex, or equivalent) runs $30–$80 and is the only tool that will produce a reliable crimp at the small gauge sizes used in the XJ harness (18–22 AWG sensor wiring). Do not skip the tool. A bad crimp is a future no-start or misfire that will be very difficult to trace.

---

### Why solder is not the correct method for wire splices

Solder is not used in professional automotive harness construction or in motorsport wiring. The failure mode is specific and predictable: solder wicks into the wire strands by capillary action, turning a flexible conductor into a rigid zone. The rigid section does not move — the wires flanking it do. Under continuous vibration, the conductor strands crack at the rigid-to-flexible boundary. This failure mode is well-documented by High Performance Academy and confirmed by OEM wiring standards (SAE J2030, USCAR-21) which specify crimp-only for all production vehicle harness connections.

**The failure is not in the solder joint itself — it is at the edge of the solder zone where the wire transitions from rigid to flexible.** This point is under constant fatigue stress in a vehicle harness.

Era 1 Renix vehicles came from the factory with some junctions that were crimped and then flow-soldered as part of the production process. That was a manufacturing method of the 1980s. It is not the standard to replicate during repair.

**If you must solder** — for example, shielding drain wires or a situation where crimping is genuinely not possible — mechanically support the joint with proper heat shrink and ensure it cannot flex. This is the only motorsport context where solder appears: shielded cable drain wire terminations, always supported.

---

### What not to use: pre-insulated butt splice connectors

The red, blue, and yellow plastic-jacketed butt splice connectors sold at auto parts stores are not the correct tool for harness repair. These are closed-barrel (pre-insulated) connectors. The problems with them, documented in automotive wiring communities:

- The plastic sleeve prevents visual inspection of the crimp — you cannot see whether the conductor strands are fully seated in the barrel
- They are designed for a different crimping geometry than open-barrel terminals and do not produce a gas-tight connection with a standard hand crimper
- Cheaper versions use a seamed barrel (not extruded tube) — the seam can open under load
- The plastic jacket can trap moisture at the wire entry point
- Quality varies widely — many sold at retail are not rated for automotive temperature cycles

High-level motorsport practitioners — including those who could use any method they choose on their own vehicles — do not use these connectors. Source: High Performance Academy forum documentation and professional wiring community consensus.

**The correct alternative** is a bare copper open-barrel splice crimp, properly tooled, sealed with adhesive-lined heat shrink. This is what OEMs use.

---

### Scotchlok / T-tap connectors — do not use

Scotchlok (IDC) T-tap connectors cut through wire insulation to make contact with the conductor. Documented failure modes, well-established in NAXJA and XJ community documentation:

- Uneven cutting of insulation corrodes the wire strands from inside over time
- Contact failure under vibration
- Moisture wicking into the tap from the cut opening
- Gradual strand severing

Their presence on a high-mileage XJ during inspection is a flag — remove and replace with a proper crimp whenever found on a circuit that matters.

**Posi-Tap connectors:** More acceptable than Scotchloks for low-current signal taps since they do not cut strands. Not a permanent repair method — use a proper open-barrel crimp for any structural repair.

---

## Wire specification for repair work

When replacing wire in a harness repair, use **TXL wire** (thin-wall cross-linked polyethylene). TXL is rated to SAE J1128, Ford M1L-123A, and Chrysler MS-8288 — these are the OEM automotive harness specifications. TXL wire:

- Is rated to 125°C continuous (257°F) — handles engine bay heat
- Has a thinner wall than GPT or standard primary wire at the same AWG rating, matching the compact bundle geometry of the factory harness
- Is oil, fuel, coolant, and solvent resistant
- Is available in bulk from Waytek Wire, Del City, or specialty automotive wire suppliers at low cost

Match the wire gauge to the original conductor. Do not upsize indiscriminately — it will not fit back into connector terminals or match the original crimp barrel dimensions.

---

## When to repair vs. replace a sub-harness

### Repair is appropriate when:
- Damage is isolated (one or two wires) and the surrounding harness is in good condition
- The wire routing and connector locations are intact
- The damaged section is accessible for clean splicing

### Replace the sub-harness when:
- Multiple wires in the same bundle are damaged (rodent damage, heat melting)
- The loom and bundling is deteriorated throughout a section
- Splice repairs have already been stacked on previous repairs in the same area
- The wire insulation is brittle and crumbling throughout a run — this indicates the entire section is at end of service life

For the injector sub-harness specifically, full replacement is almost always preferable to splicing individual pigtails on high-mileage vehicles.

---

## Injector sub-harness replacement

The injector sub-harness is a separate wiring bundle with six EV1 or EV6 connector pigtails that plug onto the fuel injectors. It runs along the intake manifold and is exposed to engine heat. On high-mileage XJs, the pigtail connectors develop broken locking tabs and the loom hardens and cracks.

**Replacement kits:** Full 6-injector pigtail harness kits are available from XJ specialty suppliers. These replace the entire sub-harness bundle including all six connector pigtails at once. This is the recommended approach when more than two connectors show damage, or when the loom condition is poor throughout.

**Era compatibility:**
- Era 1 (1987–1990) and Era 2 (1991–1998): EV1 (Bosch Jetronic) connectors — use an EV1 6-pigtail kit
- Era 3 (1999–2001): EV6 (USCAR) connectors — confirm connector type before ordering

**Splice-in procedure:**
1. Cut the old sub-harness at the point where it branches from the main engine harness — typically 6–8 inches from the main loom junction.
2. Label each wire before cutting. The injector firing order matters — each pigtail goes to a specific injector.
3. Splice in the new sub-harness using **open-barrel crimp connectors with adhesive-lined heat shrink** at each joint. Do not solder these joints — this section of the harness is directly exposed to engine vibration.
4. Re-protect the new bundle with split loom or wire wrap tape.

---

## Firewall connector cleaning and re-pinning

The main firewall multi-pin connector is a priority repair point on all XJs. See `firewall-connector.md` for the full procedure.

---

## Loom and wrapping

When re-wrapping repaired sections:
- **Split loom** (polyethylene corrugated) for general protection — leave the ends open enough that they do not trap moisture
- **High-temperature wire wrap tape** (self-fusing silicone or high-temp cloth tape) for sections near the exhaust manifold — standard split loom melts in that zone
- **Cloth wire loom tape** for a factory-appearance restoration

Do not re-wrap repairs until all joints are confirmed good with a continuity and voltage-drop check under load.

---

## Cross-references
- Connector-level repair: `connector-rehab.md`
- Firewall connector: `firewall-connector.md`
- ECU swap wiring (different scope): `work/swaps/ecu/wiring/`
- EV1 connector sourcing and procedure: `work/swaps/ecu/wiring/connectors/ev1-bosch/injectors.md`
