# White Exhaust Smoke

## Purpose
Distinguish normal cold-start vapor from coolant-burning exhaust, and route to the correct diagnosis when coolant burning is confirmed.

## Symptom definition
Use this leaf when white or light gray smoke is visible from the exhaust tailpipe.

## The critical distinction first

**Cold-start condensation is normal.** When a cold engine starts in cool or humid conditions, water vapor in the exhaust condenses into visible white steam at the tailpipe. This is water, not coolant. It:
- Appears immediately at cold start
- Clears completely within 1–5 minutes as the exhaust system warms
- Has no smell, or a faint neutral odor
- Does not recur once the engine is at operating temperature

**Do not diagnose a cold-start puff of white vapor as a coolant problem.** This is a very common false alarm.

## When to be concerned

Coolant burning in the combustion chamber produces white exhaust that is different in character:
- **Persistent** — continues after the engine has fully warmed up
- **Sweet-smelling** — coolant (ethylene glycol) has a distinctly sweet odor when burned; this smell in the exhaust is a reliable indicator
- **Dense or billowing** — thicker than normal condensation vapor
- **Associated with coolant loss** — the overflow bottle level drops over time without a visible external leak

If white exhaust appears at operating temperature and has a sweet smell: **this is coolant burning in the engine.** Move to diagnosis immediately.

## Causes of coolant burning

All of these allow coolant to enter one or more combustion chambers:
1. **Cracked cylinder head** — the 4.0L 0331 casting (2000–mid-2001) is prone to cracking between cylinders 3–4; see [`vehicle/systems/cooling/head-cracking.md`](../../vehicle/systems/cooling/head-cracking.md)
2. **Failed head gasket** — the gasket between head and block fails at a coolant passage adjacent to a cylinder
3. **Warped head from prior overheating** — a head that was distorted by heat no longer seals flat against the block

On a 2000–2001 XJ, the 0331 head is the first suspect. On any other year XJ with an overheating history, head gasket or warpage from prior overheat is more likely.

## Diagnostic sequence

### Step 1: Confirm the symptom is real
At operating temperature with engine warm, check:
- Is the smoke present continuously, not just at cold start?
- Does it have a sweet odor?
- Is the coolant level dropping between checks?

If yes to any of these after the engine is warm → proceed.

### Step 2: Combustion leak test
Draw air from above the coolant in the overflow bottle or radiator through a combustion leak test kit. A color change = combustion gases are in the coolant circuit = internal leak confirmed.

This test is positive even before oil contamination occurs and is the fastest confirmation without disassembly.

### Step 3: Check for milky oil
Pull the oil fill cap and the dipstick. Milky or light brown residue = coolant has entered the oil. If this is present, the engine has been running with contaminated lubrication — assess for additional damage.

Note: clean oil does not rule out a head crack. Coolant can burn in the cylinder without ever reaching the oil gallery.

### Step 4: Compression test
A cylinder adjacent to the leak will typically show lower compression than the others. Compare all six cylinders. A significant low outlier at cylinder 3 or 4 on a 2000–2001 XJ is strong supporting evidence for a head crack at that location.

## After confirmation

Route to [`vehicle/systems/cooling/head-cracking.md`](../../vehicle/systems/cooling/head-cracking.md) for:
- Head casting identification
- Repair options (head replacement vs. other)
- Casting-specific guidance for 0331 vs. 0630 heads

## Other causes of white exhaust (non-coolant)

- **Rich fuel mixture burning off** — white/gray puff under deceleration can be unburned fuel; typically accompanied by fuel smell, not sweet smell
- **Burning transmission fluid** — if the transmission cooler in the radiator is leaking, ATF can enter the cooling circuit and eventually the engine; ATF exhaust smells different (petroleum/burning oil odor)
- **Burning oil** — oil smoke is typically blue-gray, not white, and smells of burning oil; usually more visible under load

If the smoke is not white or sweet-smelling, reconsider whether this is a cooling problem.

## Exit criteria
Route out of this leaf when the combustion leak test result determines the next step:
- Positive combustion test → [`vehicle/systems/cooling/head-cracking.md`](../../vehicle/systems/cooling/head-cracking.md)
- Negative combustion test with continued symptom → reconsider cause; compression test next
- Confirmed cold-start only → no further action required
