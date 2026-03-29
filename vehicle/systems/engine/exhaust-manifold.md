# 4.0L Exhaust Manifold

**Branch router:** [overview.md](overview.md)

## Purpose
Document the 4.0L exhaust manifold failure mode — why it cracks, how to recognize it, and what to do about it.

## Scope
All 4.0L years in scope (1988–2001). Exhaust manifold cracking is near-universal on the 4.0L; it is a question of when, not if.

---

## The problem

The 4.0L uses a cast iron exhaust manifold. Iron is a poor thermal conductor and expands and contracts significantly with every heat cycle. The manifold is bolted rigidly to the iron head and has no expansion joints. Over thousands of heat cycles, stress concentrates at the collector (where the individual ports merge into the downpipe outlet) and between ports. Eventually the manifold cracks.

This failure is so common it is effectively a wear item on the 4.0L. Nearly every XJ with significant mileage will have a cracked manifold, visible crack or not.

---

## Symptoms

### Ticking or tapping noise when cold
The most characteristic symptom. A cracked manifold leaks exhaust under pressure at the crack. At cold idle, the crack is slightly open because the manifold has not yet expanded from heat. As the engine warms, the iron expands and the crack closes partially or fully, and the ticking quiets or disappears.

This **cold-tick that quiets when warm** pattern is the diagnostic tell for a cracked exhaust manifold. It distinguishes manifold cracking from valvetrain noise (which does not depend on exhaust temperature) and from exhaust header bolts (which may have a similar pattern but are at different locations).

### Exhaust smell in the cabin
A crack upstream of the firewall allows exhaust gases to enter the engine bay. With the ventilation system drawing air from the cowl, some exhaust can enter the cabin. Noticeably more common at idle or low-speed driving where the crack is open and airflow through the engine bay is minimal.

### Visible crack or soot deposits
On direct inspection, a crack may be visible as a hairline fracture across the manifold surface. More commonly, you will see black soot deposits streaking outward from the crack location, particularly after the engine has been run. The soot stain is often the easier thing to find.

### O2 sensor contamination
A crack downstream of the upstream (pre-cat) O2 sensor can allow outside air to dilute the exhaust sample the sensor reads. The PCM may interpret this as a lean condition and richen the mixture. On OBD-II vehicles (1996+) this may trigger a P0171 (system lean, bank 1) code without an obvious fuel delivery cause.

---

## Diagnosis

### Cold inspection
Inspect after an overnight soak with the engine fully cold. Look at the manifold surface and the collector area with a flashlight. Look for:
- Visible hairline cracks across the manifold surface
- Soot staining or black deposit streaks emanating from a point on the manifold
- Staining at the manifold-to-head gasket joint (indicates a different but related sealing failure)

### Running inspection (with caution)
With the engine warm and at idle, a rag or piece of paper held near (not touching) manifold seam areas will flutter noticeably when an exhaust pulse escapes a crack. Keep clear of the hot manifold and belts. This technique can pinpoint a crack location that is not visually obvious.

Do not run your hand near the manifold — it will be hot enough to cause an immediate burn.

---

## Repair options

### Welding
Cast iron can be welded, but it requires controlled preheat and post-heat to avoid introducing new stress cracks at the heat-affected zone. A proper iron weld by a competent shop can extend manifold life, but another crack will typically develop at the same or an adjacent location eventually. Welding is a temporary measure.

### Replacement manifold (OEM or aftermarket)
A new OEM-spec cast iron manifold is the like-for-like repair. It will eventually crack again for the same reasons, but a fresh casting buys substantial service life. Aftermarket direct-fit replacements are available and are generally comparable to OEM.

Note: HO manifolds (1991–2001) lack the EGR port tube present on Renix manifolds (1988–1990). Renix and HO manifolds will bolt to either head — the exhaust ports are the same — but EGR provisions differ and the castings are different shapes. Match the manifold to the engine management era.

### Header conversion
An aftermarket tubular steel header eliminates the cast iron manifold entirely. Steel headers do not crack in the same way. This is the permanent fix for the failure mode. Headers also provide modest power gains on the 4.0L.

Considerations:
- Clearance varies by header design; some fitment issues exist with XJ steering and body geometry
- May require O2 sensor bung relocation
- If the vehicle has a catalytic converter, confirm the header is compatible with the downstream cat

---

## Engine safety

A cracked exhaust manifold is not immediately damaging to the engine. Unlike a cooling or oiling failure, exhaust leaking from the manifold does not cause progressive internal damage on its own. However:

- The O2 sensor contamination effect (above) can cause ongoing fuel trim issues on OBD-II vehicles
- Exhaust in the cabin is a health hazard with extended exposure
- The crack will worsen over time; eventually the manifold may crack through completely, and a large section of manifold casting can fail
- Manifold stud and bolt corrosion is common on high-mileage XJs; early replacement is easier than emergency replacement with seized studs

Do not defer indefinitely.

---

## See also
- [`vehicle/engine.md`](../../engine.md) — known weaknesses overview
- [`vehicle/era2/ho-engine.md`](../../era2/ho-engine.md) — HO vs Renix manifold differences (EGR provisions)
- [`vehicle/systems/cooling/head-cracking.md`](../cooling/head-cracking.md) — the other major thermal failure mode on the 4.0L

---

## Sources
Community-verified via NAXJA, JeepForum, CherokeeForum; exhaust manifold failure pattern is a long-established community-wide observation across the full XJ production run.
