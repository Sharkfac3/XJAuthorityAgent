# Harness Repair

## Purpose
Repair or replace damaged sections of the factory XJ wiring harness. Covers splice methods, sub-harness replacement, and when full replacement is warranted over repair.

---

## Acceptable splice methods

Community consensus on XJ forums (NAXJA, JeepForum, Cherokee Talk) is consistent: solder with adhesive-lined heat shrink is the preferred repair method. Quality crimp with glue-lined heat shrink is the Mopar FSM-recommended method and is equally acceptable. Scotchlok T-tap connectors are strongly discouraged.

### Solder + adhesive-lined heat shrink (preferred)
1. Strip both wire ends back ~3/4 inch.
2. Slide a piece of adhesive-lined (glue-lined) heat shrink tube over one wire before splicing — large enough to cover the joint plus 1/2 inch on each side.
3. Lap or butt the stripped ends. For butt splices, use a pre-tinned butt sleeve or lap the strands.
4. Apply rosin-core solder until fully wicked through the strands. Do not use acid-core solder.
5. Allow to cool without moving.
6. Slide the heat shrink over the joint and shrink with a heat gun. The glue liner should flow out the ends, sealing the joint against moisture.

**Vibration note:** Solder creates a hard/soft transition point at the joint boundary. On circuits subject to continuous vibration (near the engine), some experienced builders prefer quality crimp + heat shrink to avoid this transition. Both methods are valid.

### Crimp + glue-lined heat shrink (FSM-recommended)
1. Strip both wire ends ~3/4 inch.
2. Use a quality ratcheting crimper sized to the wire gauge — never a generic plier-type crimper.
3. Insert both stripped ends into a bare copper butt splice crimp (not insulated — the heat shrink provides the seal).
4. Crimp both ends fully.
5. Cover with adhesive-lined heat shrink and shrink with a heat gun.

This method is what Mopar specifies in the XJ Factory Service Manual for wire repair. It produces a flexible, moisture-sealed joint that handles engine vibration well.

### Scotchlok / T-tap connectors — do not use
Scotchlok (IDC) T-tap connectors are widely documented as a failure source by the XJ and broader automotive community. Documented failure modes include:
- Uneven cutting of insulation that corrodes the wire strands from inside
- Contact failure under vibration
- Moisture wicking into the tap from the cut opening
- Gradual strand severing over time

Source: Community consensus documented on NAXJA, Garage Journal, and XJ-specific threads. These connectors are found on many high-mileage XJs from previous owners — their presence during inspection is a flag for current or future electrical problems.

**Posi-Tap connectors:** Considered more acceptable than Scotchloks in the community for low-current taps into existing wires (accessories, signal wires). They do not cut the wire strands. Still not a permanent repair method — use solder or crimp for any structural repair.

---

## When to repair vs. replace a sub-harness

### Repair is appropriate when:
- Damage is isolated (one or two wires) and the surrounding harness is in good condition
- The wire routing and connector locations are intact
- The damaged section is accessible for clean splicing

### Replace the sub-harness when:
- Multiple wires in the same bundle are damaged (rodent damage, melting)
- The loom and bundling is deteriorated throughout a section
- Splice repairs have already been stacked on previous repairs in the same area
- The wire insulation is brittle and crumbling throughout a run (indicates the entire section is at end of life)

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
2. Label each wire before cutting (the injector firing order matters — each pigtail goes to a specific injector).
3. Solder in the new sub-harness using adhesive-lined heat shrink at each joint.
4. Reprotect the new bundle with split loom or wire wrap tape.

---

## Firewall connector cleaning and re-pinning

The main firewall multi-pin connector is a priority repair point on all XJs. See `firewall-connector.md` for the full procedure.

---

## Loom and wrapping

When re-wrapping repaired sections, use:
- Split loom (polyethylene corrugated) for general protection — leave the ends open enough that they do not trap moisture
- High-temperature wire wrap tape (self-fusing silicone or high-temp cloth tape) for sections near the exhaust manifold — standard split loom melts in that zone
- Cloth wire loom tape is the factory-style appearance if keeping the harness stock-looking

Do not re-wrap repairs until all joints are confirmed good with a continuity check.

---

## Cross-references
- Connector-level repair: `connector-rehab.md`
- Firewall connector: `firewall-connector.md`
- ECU swap wiring (different scope): `work/swaps/ecu/wiring/`
- EV1 connector sourcing and procedure: `work/swaps/ecu/wiring/connectors/ev1-bosch/injectors.md`
