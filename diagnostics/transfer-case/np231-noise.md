# NP231 Noise

## Purpose
Fault-isolate noise originating from the NP231 transfer case: chain slap, output bearing noise, and slip yoke vibration.

## Symptom definition
Use this leaf when there is a noise or vibration that appears to come from the center of the driveline — behind the transmission and ahead of the rear driveshaft — and that changes with transfer case range or shaft rotation.

## Do not use this leaf when
- The noise is present only on turns or only under steering input → likely a front axle or wheel bearing issue; route to `diagnostics/driveline/axle-noise.md`
- The primary complaint is difficulty getting into or out of 4WD → route to [`np231-shift-issues.md`](np231-shift-issues.md)
- Vibration is constant and started after a lift installation → also see [`../driveline/driveshaft-vibration.md`](../driveline/driveshaft-vibration.md)

---

## Common branches

### Chain slap branch

**What it sounds like:** A slapping, rattling, or knocking sound from the transfer case that may vary with throttle or RPM. Can sound like something loose inside the case.

**Cause:** The NP231's drive chain stretches over time. A worn chain has enough slack to slap the inside of the case housing. This is the most common NP231 internal noise.

**Quick field test:**
1. With the transmission in Park and the transfer case in 4H (all four wheels locked), place a hand on the transfer case housing and have an assistant blip the throttle briefly.
2. Alternatively: remove the front driveshaft at the output flange. With the front shaft disconnected, rotate the front output yoke by hand. Movement of more than approximately ¼" in either direction before the chain takes up indicates a worn chain.

**Inspect drained fluid:** When draining transfer case fluid, look for aluminum sparkle or metallic debris. A badly worn chain can score the aluminum case interior.

**Consequence of ignoring it:** A heavily worn chain can crack through the case and cause sudden fluid loss.

**Resolution:** Chain replacement. Requires case disassembly. If the case interior is already scored, evaluate case condition before investing in chain only.

---

### Output bearing noise branch

**What it sounds like:** A steady hum or rumble that tracks with vehicle speed (not engine RPM). The noise may be present in all transfer case ranges or only when the relevant output shaft is spinning.

**Front output bearing:**
- Noise present in 4WD only (when front shaft is spinning)
- Rules out if noise disappears when front driveshaft is removed and vehicle is driven in 2WD

**Rear output bearing:**
- Noise present in 2WD and 4WD (rear shaft is always spinning in all modes on an NP231)
- Harder to isolate without disassembly; compare to rear axle pinion bearing noise (which will also be present in both 2WD and 4WD)

**Distinguishing transfer case bearing from axle bearing:**
- If noise is present with the rear driveshaft removed (vehicle on a lift, driven briefly), the source is at or ahead of the rear output — transfer case or transmission tailshaft
- If noise disappears with the rear driveshaft removed, the noise source is in the driveshaft, axle, or rear wheel bearings

---

### Slip yoke vibration branch

**What it sounds like:** A rhythmic vibration, often speed-dependent (not RPM-dependent), felt through the floor and sometimes heard as a low rumble or buzz.

**When it appears:** Slip yoke vibration typically becomes noticeable after a suspension lift of 2 inches or more. The slip yoke is the stock rear output design on both the NP231 and NP242 — it works acceptably at stock height but becomes a vibration source at lifted angles.

**Root cause:** The slip yoke slides in and out of the transfer case output shaft as the driveshaft moves through its angles. When the driveshaft operating angle increases due to lift, the slip yoke is pushed further out of its normal travel range. This creates vibration and adds stress to the output shaft.

A corroded or worn slip yoke adds to the problem — check the yoke and the mating output shaft bore for wear and corrosion.

**Resolution pointer:** A Slip Yoke Eliminator (SYE) kit converts the rear output to a fixed yoke and requires a custom-length rear driveshaft with a CV (double-cardan) front joint. This is the standard fix for lifted XJs with NP231 or NP242 transfer cases. Aftermarket support for SYE is much more widely available for the NP231 than for the NP242.

See [`../../vehicle/systems/transfer-case/overview.md`](../../vehicle/systems/transfer-case/overview.md) for transfer case identification.

---

## Exit criteria

Route out of this leaf when evidence points to:
- **Chain slap** → internal service decision; evaluate case condition before committing to rebuild
- **Output bearing** → transfer case teardown/rebuild; confirm bearing location (front vs rear output) before disassembly
- **Slip yoke vibration** → SYE kit + custom driveshaft; route to `work/` for execution

## Related stock reference
- NP231 and NP242 specs and year matrix: [`../../vehicle/systems/transfer-case/overview.md`](../../vehicle/systems/transfer-case/overview.md)
- 4WD engagement and shift modes: [`../../vehicle/systems/4wd/overview.md`](../../vehicle/systems/4wd/overview.md)
- Shift problems: [`np231-shift-issues.md`](np231-shift-issues.md)
