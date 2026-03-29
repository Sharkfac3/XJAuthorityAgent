# Overheating Diagnosis

**Branch router:** [index.md](index.md)

## Purpose
Provide a structured diagnostic sequence for a 4.0L XJ that is running hot or overheating, and document the risk that a single overheating event poses to the engine.

## Scope
This is a stock-baseline reference for understanding the likely causes in order of probability and ease of testing. For symptom-specific starting points, see the diagnostics branch.

---

## Before anything else

**Do not continue driving an overheating XJ.** The 4.0L head is vulnerable to warping from sustained high heat. If the gauge is climbing toward or into the red:
1. Turn off A/C if equipped (removes one heat load)
2. Turn the cabin heater on full blast (transfers heat from coolant to cabin air — a meaningful reduction in extreme cases)
3. Pull over and shut off the engine as soon as it is safe to do so
4. Let the engine cool completely before opening the radiator cap or overflow bottle

**Never open a hot radiator cap.** A pressurized system at operating temperature will eject scalding coolant.

---

## Diagnostic sequence

Work through these in order. Most overheating problems are upstream causes, not dramatic failures. Start cheap and fast before assuming the worst.

### 1. Thermostat stuck closed

**Probability: High.** A thermostat that fails closed prevents coolant from circulating through the radiator. The engine heats rapidly, the radiator stays cold.

- Check: With the engine warm, the upper radiator hose should be hot to the touch. If the upper hose is cold or only slightly warm while the engine is overheating, the thermostat is likely stuck closed.
- Confirm: Replace the thermostat with a known-good unit (stock 195°F). This is the lowest-cost first test.

### 2. Low coolant level

**Probability: High.** An air pocket in the system reduces heat transfer and can cause localized hot spots that read high at the temperature sender even when the system is not fully overheaded.

- Check: Confirm the overflow bottle level when cold. If low, add coolant and check for external leaks before assuming the problem is solved.
- A system that repeatedly needs coolant has a leak — find it.

### 3. Air in the system

**Probability: Moderate.** Air trapped in the system after a coolant flush or component replacement will cause erratic temperature readings and intermittent overheating.

Air bleed procedure:
1. Fill the system slowly through the radiator neck (or overflow bottle, depending on year) with the engine cold
2. With the radiator cap off, squeeze the upper radiator hose several times to work out air bubbles
3. Start the engine and let it idle with the cap off until the thermostat opens (you will see coolant begin circulating in the radiator neck)
4. Top off, replace cap, check overflow bottle level
5. Drive and recheck the overflow bottle level after the first heat cycle

Some XJs benefit from parking on an incline (front elevated) during the bleed to help air move toward the fill point.

### 4. Weak or failed fan clutch

**Probability: Moderate, especially for idle-only overheating.** The mechanical fan clutch engages more aggressively as temperature rises. A worn clutch slips at all temperatures, reducing airflow at idle where the clutch is the primary cooling source.

- Check: With the engine fully warmed up, shut it off. Immediately try to spin the fan blade by hand. A good clutch will resist. A completely failed clutch will spin freely with minimal resistance.
- Also check: missing or cracked fan shroud, which defeats both the mechanical fan and electric auxiliary fan efficiency at low speed

### 5. Water pump failure

**Probability: Lower, but should be confirmed.** A pump with a failed impeller or worn bearing moves less coolant, reducing heat transfer.

- Check weep hole for dripping; check pulley for wobble. See [`water-pump.md`](water-pump.md).
- A pump that has lost impeller fins due to erosion will show no external symptoms — this is found on teardown.

### 6. Clogged or degraded radiator

**Probability: Lower on younger vehicles; significant on high-mileage or neglected XJs.** Years of scale, sediment, and degraded coolant can restrict the radiator core internally.

- Check: Infrared thermometer across the radiator face after warmup — cold spots in the core indicate blocked passages
- External: inspect radiator fins for packed debris, bent fins, or damage at the front face
- A radiator with significant internal restriction requires a professional flush or replacement

### 7. Head gasket failure or cracked head

**Probability: Lower as a standalone cause, but must be ruled out if the above checks are clean.** Combustion gases entering the cooling circuit pressurize it and displace coolant, reducing circulation and causing overheating that resists conventional fixes.

- Classic sign: system overheats even after thermostat, pump, fan clutch, and radiator have been confirmed good
- Test: combustion leak test (block test) on the coolant reservoir — see [`head-cracking.md`](head-cracking.md)
- If the vehicle is a 2000 or 2001 XJ with an original 0331 head, move this step higher in the sequence

---

## The one-overheat risk

**A single severe overheating event can warp the 4.0L head.** Cast iron warps under sustained high heat, and a warped head will not seal properly against the block regardless of the head gasket condition.

Signs that a prior overheat may have warped the head:
- Head gasket replaced but overheating or coolant loss continues
- Combustion leak test positive after a known overheating incident
- Persistent coolant loss or white exhaust that started after the temperature gauge reached red

If the vehicle has a known overheating history, have the head checked for warpage at a machine shop before assuming a head gasket replacement will hold. A warped head requires surfacing (if within tolerance) or replacement.

---

## See also
- [`head-cracking.md`](head-cracking.md) — 0331 casting vulnerability and head crack diagnosis
- [`water-pump.md`](water-pump.md) — pump failure modes and inspection
- [`diagnostics/cooling/overheating-at-idle.md`](../../../diagnostics/cooling/overheating-at-idle.md) — symptom-first path for idle-only overheating
- [`diagnostics/cooling/overheating-at-speed.md`](../../../diagnostics/cooling/overheating-at-speed.md) — symptom-first path for highway overheating

---

## Sources
Community-verified diagnostic sequence via NAXJA, CherokeeForum, JeepForum; air bleed procedure consistent with XJ service manual guidance; one-overheat warpage risk is a consistent community-wide observation.
