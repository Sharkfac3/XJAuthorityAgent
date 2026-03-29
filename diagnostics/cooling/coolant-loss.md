# Coolant Loss with No Visible Leak

## Purpose
Provide a fault-isolation path for XJs losing coolant without an obvious external puddle or drip.

## Symptom definition
Use this leaf when:
- The coolant level in the overflow bottle or radiator is dropping over time
- There is no puddle under the vehicle
- There are no visible drips, stains, or wet spots on hoses, clamps, fittings, or the radiator

## Do not use this leaf when
- There is a visible external leak with a known location — fix the external leak
- White exhaust accompanies the coolant loss → also load [`white-exhaust.md`](white-exhaust.md) in parallel
- Overheating is the primary complaint and the coolant loss is incidental → start with the overheating leaves

## Why invisible coolant loss matters

Coolant does not disappear on its own. Invisible loss falls into a short list of causes:
1. **Internal combustion leak** — coolant is being burned in the combustion chamber and exiting as steam through the exhaust
2. **Evaporation through an unsealed system** — a bad cap, cracked overflow bottle, or missing cap allows coolant to vent to atmosphere rather than being recovered
3. **External leak that is vaporizing or dripping somewhere unseen** — weep hole drip that evaporates on a hot engine, heater core seeping into the cabin, or a small hose leak at the back of the engine

The most serious cause is #1. The diagnostic sequence below separates internal from external causes before assuming the worst.

## Diagnostic sequence

### Step 1: Eliminate the cap and overflow bottle
A radiator cap that does not seal or hold pressure will vent coolant when the system heats up instead of routing it to the overflow bottle. A cracked or absent overflow bottle means the coolant vented cannot be recovered.

- Inspect the overflow bottle for cracks, particularly at the neck and mounting area
- Test the radiator cap with a cooling system pressure tester — it should hold rated pressure (typically ~16 PSI); replace if it does not
- Confirm the overflow bottle hose is connected and not cracked

This is the lowest-effort first check and rules out a common benign cause.

### Step 2: Check for external leaks that are not visible cold
Some leaks only occur under heat and pressure:
- Run the engine to operating temperature
- Inspect hose-to-fitting connections, clamp areas, radiator tank seams, heater hose connections at the firewall, and the water pump weep hole (see [`vehicle/systems/cooling/water-pump.md`](../../vehicle/systems/cooling/water-pump.md))
- Look for dried coolant residue (white or rust-colored mineral deposits) anywhere on the engine or bay — these are traces of past leaks that evaporated

### Step 3: Combustion leak test
If external causes are ruled out, test for combustion gases in the coolant. This is the definitive non-teardown test for an internal leak.

Procedure:
1. Bring the engine to operating temperature
2. Remove the overflow bottle or radiator cap carefully (system is hot and pressurized — use a rag, open slowly)
3. Draw air from above the coolant surface through a combustion leak test kit
4. Color change (blue to yellow/green) = combustion gases in coolant = internal leak

A positive test on a 2000–2001 XJ with original head strongly indicates the 0331 head cracking failure. On other year XJs, it indicates a head gasket failure or head crack from prior overheating.

### Step 4: Check the oil
Coolant mixing with oil produces milky, light-brown residue visible on the oil fill cap and dipstick. Check both.

- Milky oil = coolant is entering the oil circuit — this is a serious finding; the engine has been running with contaminated oil
- Clean oil does not rule out a head crack (coolant may be entering the combustion chamber without reaching the oil)

### Step 5: Pressure test
A cooling system pressure test identifies whether the system holds pressure. If the system bleeds down with no external leak, coolant is escaping internally.

- Apply pressure to the cold, full system with a pressure tester
- A system that holds pressure is either losing coolant through the cap (test separately) or has a very minor evaporative leak
- A system that slowly bleeds down with no external leak = internal leak path

## When the combustion leak test is positive
Route to [`vehicle/systems/cooling/head-cracking.md`](../../vehicle/systems/cooling/head-cracking.md) for head casting identification, diagnosis confirmation, and repair options.

## Exit criteria
Route out of this leaf when you have identified the leak mechanism:
- External leak → repair in `work/repairs/cooling/`
- Cap or overflow system → replace components
- Internal combustion leak → [`vehicle/systems/cooling/head-cracking.md`](../../vehicle/systems/cooling/head-cracking.md)
