# Connector Rehabilitation

## Purpose
Save or restore factory connectors on high-mileage XJs. Many connectors are serviceable with cleaning and new terminals. Some require rehousing or pigtail replacement.

---

## When to rehouse vs. replace

**Clean and reuse when:**
- The connector housing is intact with no cracking or melted areas
- The locking tab is functional or is a type that does not rely on the tab for retention
- Pin corrosion is surface-level — green or white oxidation that cleans off

**Rehouse (replace housing only) when:**
- The housing is cracked, split, or deformed, but the wire pigtail is still good
- The locking tab is broken and the connector type requires it for secure retention
- A direct replacement housing with new pins is available and cheaper than a full pigtail

**Replace the full pigtail when:**
- The housing is cracked or melted and no replacement housing is available separately
- The wires at the back of the connector are corroded for 2+ inches (corrosion has wicked into the wire strands)
- The terminal pins are corroded, collapsed, or damaged and cannot be removed cleanly

---

## Cleaning corroded pins

### Supplies
- Electrical contact cleaner (CRC QD Contact Cleaner or equivalent — not WD-40)
- Small brush (soft-bristle toothbrush or connector cleaning brush)
- Dental pick or fine scribe
- Dielectric grease (Permatex 22058 or equivalent)
- Compressed air

### Procedure
1. Disconnect the connector. Never spray contact cleaner into a connector while installed in the circuit.
2. Spray contact cleaner into the connector face and allow it to penetrate for 30 seconds.
3. Work the contacts gently with a small brush to remove loose oxidation.
4. Use a dental pick to clear debris from individual pin cavities — do not use abrasives inside the connector body.
5. Re-spray and allow to fully evaporate (contact cleaner leaves no residue when dry).
6. Inspect pin engagement: pins should seat firmly and not push back when a mating pin is inserted.
7. Apply a small amount of dielectric grease to the mating face of the connector before reassembly. Do not pack the cavities — a thin coat on each pin is sufficient. Dielectric grease prevents future moisture ingress and slows re-oxidation.

**Dielectric grease note:** Dielectric grease does not conduct electricity. It works by displacing moisture at the contact interface. Contacts must be fully mated through the grease for conduction — this is normal behavior.

---

## EV1 injector connector brittle tab procedure

EV1 (Bosch Jetronic) connectors are used on all injectors on 1987–1998 XJs. The plastic locking tab becomes brittle with age and breaks on removal. This is a well-documented and near-universal failure on high-mileage XJs. Source: JeepForum community documentation confirms broken EV1 tabs as routine on these vehicles.

**Year range:** 1987–1998. The 1999–2001 Era 3 vehicles use EV6 (USCAR) connectors which have a different release mechanism.

### Release procedure (intact tab)
1. Disconnect battery negative.
2. Insert an EV1 release pick from the side of the connector — not from the top or the wire side.
3. Depress the locking tab while pulling the connector straight off the injector body.
4. Do not twist. The injector inlet O-ring can become stuck — a straight pull is required.

### Broken tab — what to do
A broken tab does not mean the connector is immediately unusable. The connector will still seat and maintain contact without the tab. However, it can vibrate loose over time.

Options:
- **Replacement pigtail:** Cut the old connector 3–4 inches back from the body. Splice a new pre-made pigtail in its place using an open-barrel crimp connector with adhesive-lined heat shrink on each joint. Do not solder — this section of the harness is in a high-vibration zone (see `harness-repair.md` for why). Replacement EV1 pigtails (Standard Motor Products PC-946280 or equivalent) are available from RockAuto and Amazon.
- **Full 6-injector pigtail harness:** For vehicles where multiple connectors are broken or degraded, a complete 6-injector sub-harness pigtail kit is available from XJ specialty suppliers. This replaces all six connectors at once and is the recommended approach for a full harness restoration. See `harness-repair.md`.

Cross-references: `vehicle/era1/injectors.md`, `vehicle/era2/injectors.md`

---

## Metri-Pack 150 re-pin procedure

Metri-Pack 150 connectors are the standard sensor connector on Era 2 (1991–1995) and Era 3 (1996–2001) XJs. Applications include TPS, MAP, CTS, IAT, and IAC sensor connectors.

### Tools required
- Metri-Pack 150 terminal release tool (the correct pick for the 1.5mm series — do not substitute)
- Replacement 1.5mm Metri-Pack 150 terminals and seals (Delphi/Aptiv, Waytek Wire, or Del City)
- Ratcheting crimper sized for 1.5mm Metri-Pack terminals

### Procedure
1. Identify the connector as Metri-Pack 150 by the small terminal cavities (1.5mm). Do not use a 280 or 630 release tool — it will deform the cavity.
2. Release the secondary lock (if present) by pressing the outer lock bar sideways before attempting terminal removal.
3. Insert the release tool into the terminal cavity from the wire side (rear of the connector body).
4. Depress the terminal retention lances while simultaneously pushing the terminal forward and withdrawing the wire rearward.
5. The terminal will slide out the rear. Do not pull the wire without releasing the lance — the terminal will deform.
6. Inspect the cavity for debris or corrosion. Clean if needed.
7. Crimp the replacement terminal onto the wire using a ratcheting crimper — the terminal has a wire crimp and an insulation crimp tab. Both must be engaged.
8. Insert the new terminal into the cavity until the retention lances click. Pull lightly on the wire to confirm lock.
9. Re-engage the secondary lock.

### Seals
Metri-Pack 150 uses a wire seal on each terminal. Match the seal to the wire gauge. Missing or torn seals allow moisture into the connector and are a common corrosion source. Replace seals whenever re-pinning.

---

## Identifying and replacing broken locking tabs

Many XJ connectors use a friction or press-fit retention tab that can break, leaving the connector seated but not locked. A connector without a functional tab will vibrate loose, particularly near the engine.

For most sensor connectors (Metri-Pack 150 and 280): a broken tab means the connector body should be replaced. The terminal pins can be salvaged by transfer into a new housing if the housing is available. Otherwise, replace with a full pigtail.

For larger connectors (fuse block, PDC, multi-pin body connectors): these typically use a sliding secondary lock or a bolt-through mount rather than a snap tab — inspect the secondary lock mechanism separately from the housing.

---

## Cross-references
- EV1 injector connector detail: `work/swaps/ecu/wiring/connectors/ev1-bosch/injectors.md`
- Metri-Pack series overview: `work/swaps/ecu/wiring/connectors/metri-pack/overview.md`
- Firewall connector pin work: `firewall-connector.md`
- Full injector harness replacement: `harness-repair.md`
