# 4.0L Head Cracking

**Branch router:** [index.md](index.md)

## Purpose
Document the 4.0L cylinder head cracking failure — which castings are vulnerable, why it happens, how to recognize it early, and what to do about it.

## Scope
All 4.0L XJ years are at some risk from sustained overheating, but the 2000–mid-2001 0331 casting is structurally prone to cracking even without severe abuse. This leaf covers the failure mode, symptoms, diagnosis, and repair options.

---

## The problem

The 4.0L iron head can crack near the coolant passages in the exhaust port area between cylinders 3 and 4. When it does, combustion gases enter the coolant circuit (or coolant enters the combustion chamber), leading to a cascade of symptoms that worsen rapidly if ignored.

**This is not just a head gasket failure** — the head itself cracks. A head gasket replacement alone will not fix a cracked head.

---

## Which castings are affected

The full casting history is documented in [`vehicle/era2/ho-engine.md`](../../era2/ho-engine.md). Summary relevant to this failure:

| Casting | Years (XJ) | Cracking risk |
|---------|------------|---------------|
| 0331 (early) | 2000–mid-2001 | **High.** Thinner walls in exhaust port area; cracks between cylinders 3–4 even without severe abuse. Avoid. |
| 0331 TUPY | Mid-2001+ (TJ/WJ donors) | Low. Revised Brazilian casting; no cracking issue. Desirable replacement head. |
| 0630 | 1996–1999 | Low. Solid casting; not prone to cracking. |
| Earlier HO heads | 1991–1995 | Low for casting failure specifically; vulnerable to warping from overheating like any iron head, but not prone to the 3–4 crack pattern. |

The 0331 early casting was Chrysler's final XJ head design. It has larger intake and exhaust passages than the 0630 for improved flow, but the wall between the #3 and #4 exhaust ports was cast too thin. A large batch of these was produced with low-quality iron early in the 2000 model year, compounding the issue.

**If the vehicle is a 2000 or 2001 XJ, confirm the head casting number before assuming the head is healthy.** The casting number is stamped on top of the head, visible after removing the valve cover.

---

## Causes

1. **Casting defect (0331 only):** Structural thinness in the exhaust port area makes early 0331 heads prone to cracking without an overheating event
2. **Chronic overheating:** Any head is vulnerable to cracking or warping if repeatedly overheated — even once severely
3. **Coolant neglect:** Degraded coolant loses its corrosion inhibitors; internal corrosion weakens the casting over time
4. **Age and thermal cycling:** Decades of heat cycles stress any iron casting

---

## Early symptoms

These symptoms appear before the crack fully propagates and the situation becomes obvious:

- **Sweet-smelling white exhaust at operating temperature** — coolant entering the combustion chamber burns off as white steam with a distinctly sweet odor. Do not confuse with cold-start condensation, which is normal, odorless, and clears within a few minutes of warm-up.
- **Coolant loss with no visible external leak** — coolant disappears from the overflow bottle or radiator with no puddle under the vehicle and no visible drips or stains on hoses, clamps, or fittings
- **Persistent overheating** — system continues running hot even after thermostat, water pump, and fan clutch have been confirmed good

**Late-stage symptom (worst case):**
- **Milky oil** — coolant mixing with oil produces a light brown, milky residue visible on the oil fill cap or dipstick. At this stage the engine has been running with contaminated oil; additional damage is likely.

---

## Diagnosis

### Step 1: Combustion leak test (block test)
This is the most reliable non-teardown test. A combustion leak test kit (also called a block test or exhaust gas analyzer) uses a chemical fluid that changes color — typically from blue to yellow/green — in the presence of combustion gases.

Procedure:
1. Let the engine reach operating temperature
2. Remove the radiator cap or overflow bottle cap (carefully — system is hot and pressurized)
3. Draw air from above the coolant surface through the test fluid using the included bulb
4. A color change indicates combustion gases are present in the coolant circuit = internal leak

Test kits are available at most auto parts stores for $20–30. This test does not require disassembly.

### Step 2: Cooling system pressure test
A pressure test confirms whether the system holds pressure. A system that bleeds down overnight with no external leak points to an internal leak path (head crack or head gasket).

### Step 3: Compression test
A cylinder with a crack or compromised gasket adjacent to a coolant passage will typically show low compression. Run a compression test on all six cylinders and compare. Cylinder 3 or 4 reading significantly lower than the others supports a head crack diagnosis.

### Step 4: Visual inspection
With the valve cover off, the top of the head between cylinders 3 and 4 can sometimes be inspected directly. Cracks may be visible as a hairline fracture, or may only appear under dye penetrant testing.

---

## Repair options

### Head replacement (preferred)
Replace the cracked head with a known-good casting. Preferred options in order:

1. **0331 TUPY** (from a mid-2001+ TJ or WJ donor) — best flow, no cracking issue, direct drop-in on 2000–2001 XJ
2. **0630** (from a 1996–1999 XJ, ZJ, TJ, or YJ donor) — solid casting, slightly less flow than TUPY 0331, but requires attention to coil rail mounting boss differences and temperature sender location when swapping to a 2000+ chassis; see `vehicle/era2/ho-engine.md` for details
3. **Remanufactured aftermarket head** — verify casting number and supplier reputation; quality varies

When replacing the head, also replace:
- Head gasket (MLS multi-layer steel preferred over OEM composite)
- Head bolts (torque-to-yield; do not reuse)
- Thermostat and housing gasket
- Coolant flush

### Resleeve / crack repair
Welding or crack-repair compounds are sometimes attempted but are not recommended for a long-term fix on a running engine. Iron head welding requires controlled preheat and post-heat to avoid introducing new stress cracks. Community consensus is that head replacement is more reliable than weld repair.

---

## Risk note: a single overheating event

The 4.0L head is cast iron, but it is not immune to warping from a single severe overheat. Even if the engine is brought back to normal temperature before damage is visible, a head that has been overheated once should be checked for warpage at a machine shop before assuming it is still serviceable. The 0331 casting in particular has less margin for thermal stress.

**Do not ignore an overheating event.** Catching it early costs a thermostat and a coolant flush. Catching it late costs a head.

---

## See also
- [`vehicle/era2/ho-engine.md`](../../era2/ho-engine.md) — full head casting table, DIS/coil rail mounting boss differences, temperature sender location by year
- [`water-pump.md`](water-pump.md) — water pump failure modes
- [`overheating-diagnosis.md`](overheating-diagnosis.md) — full overheating diagnostic sequence
- [`diagnostics/cooling/coolant-loss.md`](../../../diagnostics/cooling/coolant-loss.md) — coolant loss with no visible external leak
- [`diagnostics/cooling/white-exhaust.md`](../../../diagnostics/cooling/white-exhaust.md) — white exhaust smoke diagnosis

---

## Sources
Community-verified via NAXJA, CherokeeForum (0331 head overview thread), JeepStrokers cylinder head FAQ, Allpar Jeep 4.0 documentation; combustion leak test procedure cross-referenced against standard cooling system diagnostic practice.
