# Driveshaft Vibration

## Purpose
Fault-isolate driveshaft and U-joint vibration on the XJ Cherokee: worn U-joints, slip yoke condition, and driveshaft angle problems common after suspension lifts.

## Symptom definition
Use this leaf when there is a vibration felt through the floor or body that tracks with vehicle speed (not engine RPM) and is consistent with driveshaft rotation — typically a rhythmic buzz, shake, or low-frequency rumble.

## Do not use this leaf when
- The vibration tracks with engine RPM regardless of vehicle speed → engine or transmission mount issue, not a driveshaft problem
- The noise is a bang or clunk on takeoff or coasting → U-joint lash or slip yoke end-play; see axle noise or clunk-on-takeoff paths
- The vibration appeared after axle work and is accompanied by noise on turns → front axle U-joint or wheel bearing issue; see [`axle-noise.md`](axle-noise.md)

---

## Front vs. rear isolation

The simplest and most reliable test is to **remove the front driveshaft** and take a test drive on a safe, straight road at the speed where vibration is present.

- Vibration disappears → front driveshaft or front axle is the source
- Vibration persists → rear driveshaft, rear axle, or wheel is the source

This test is fast (8 bolts at the front axle slip yoke end on most XJs) and removes ambiguity before any component replacement.

---

## Common branches

### U-joint wear branch

**Symptoms:** Vibration that is speed-dependent; may worsen under acceleration or deceleration. In advanced cases, a rhythmic clunk instead of or alongside the vibration.

**Inspection:**
1. With the driveshaft in hand (removed or with vehicle on a lift), rotate the shaft slowly and feel for roughness or binding in the U-joint rotation
2. Grasp the U-joint body and try to move the bearing caps axially (side-to-side in their bores) — any movement indicates worn needle bearings
3. Look for rust coming out of the bearing cap caps — brown rust powder or weeping at the caps is a sign of worn or unsealed bearings
4. Check for missing grease fittings or grease fittings that will not take grease (indicating a seized nipple or joint that is past service)

U-joints on the XJ are not serviceable once worn — they are pressed-in and replaced as a unit. Replace U-joints in matching pairs (both ends of one shaft) rather than one at a time.

**Front driveshaft specifics:** The front driveshaft on most XJs uses a double-cardan (CV) joint at the transfer case end and a standard U-joint at the axle end. Inspect both ends and the center ball stud in the CV joint.

---

### Slip yoke condition branch

**The stock NP231 (and NP242) rear output uses a slip yoke** — the rear driveshaft slides into the transfer case output rather than bolting to a fixed flange. The slip yoke moves in and out as the suspension cycles and the driveshaft angle changes.

**Symptoms of slip yoke problems:**
- Vibration at highway speed that temporarily improves after injecting grease into the slip yoke fitting, then returns
- Vibration that is worse with the vehicle lightly loaded (slip yoke deeper in the bore) vs. heavily loaded

**Inspection:**
- With the rear driveshaft in the normal installed position, check for rust, corrosion, or mechanical wear on the exposed splined section of the slip yoke
- A worn slip yoke or worn output shaft bore will have measurable side-play; the yoke should not wobble in the bore
- On a heavily corroded yoke, the splines themselves erode and create an out-of-round rotating mass

**Note:** Slip yoke problems on lifted vehicles are typically addressed with an SYE kit (see below), not by slip yoke replacement alone.

---

### Driveshaft angle after lift branch

**When it appears:** A vibration that was not present before a suspension lift, or one that appeared gradually as the lift was increased.

**Root cause:** U-joints have an optimal operating angle — typically below 3°. When suspension lift increases the angle between the transfer case output and the rear axle pinion, the U-joints operate at steeper angles, creating a velocity variation in each rotation that produces vibration.

**Year-specific note:** 1996+ XJs do not have an extension housing on the transfer case output, making them more sensitive to angle changes with lift. Vibration can appear at 2 inches of lift on a 1996+; pre-1996 XJs are somewhat more tolerant.

**Test:** Measure the operating angle by placing an angle gauge on the driveshaft near each end and at the pinion yoke. If the operating angle exceeds ~3°, driveshaft geometry is contributing to vibration.

**Resolution pointer:** A Slip Yoke Eliminator (SYE) kit converts the rear output to a fixed flange and moves the sliding joint into the driveshaft itself (a double-cardan CV joint). This allows the rear driveshaft angle to be corrected independently of vehicle height and eliminates the stock slip yoke. An SYE requires a custom-length rear driveshaft to match the new geometry.

See [`../../vehicle/systems/transfer-case/overview.md`](../../vehicle/systems/transfer-case/overview.md) for transfer case identification (NP231 vs NP242 — SYE availability differs).

---

## Exit criteria

- **U-joint wear:** replace U-joints; pair both ends of the affected shaft
- **Worn slip yoke or output bore:** if the vehicle is at stock height, slip yoke replacement; if lifted, SYE is the correct fix
- **Driveshaft angle (lifted vehicle):** SYE kit + custom rear driveshaft; route to `work/`
- **Vibration persists after U-joint and angle corrections:** check for driveshaft balance (a driveshaft can be out of balance from impact damage or after welding work)

## Related stock reference
- Transfer case identification and slip yoke context: [`../../vehicle/systems/transfer-case/overview.md`](../../vehicle/systems/transfer-case/overview.md)
- Axle noise isolation: [`axle-noise.md`](axle-noise.md)
