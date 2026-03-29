# Axle Noise

## Purpose
Fault-isolate rear and front axle noise on the XJ Cherokee: ring and pinion whine, pinion bearing noise, wheel bearing hum, and distinguishing front axle from rear axle as the source.

## Symptom definition
Use this leaf when there is a humming, whining, growling, or grinding noise that varies with vehicle speed (not engine RPM) and appears to originate from a wheel end or the differential area.

## Do not use this leaf when
- Noise is present only on turns or hard off-road use with front axle shafts loaded → front U-joint or CV joint wear; see front axle specifics in [`../../vehicle/systems/axles/dana30-front.md`](../../vehicle/systems/axles/dana30-front.md)
- Noise is speed-dependent and rhythmic, and originated after a lift installation → also check driveshaft vibration at [`driveshaft-vibration.md`](driveshaft-vibration.md)
- There is clunking on takeoff or under load, not a continuous hum → U-joint lash or axle shaft end-play

---

## Front vs. rear isolation

Before diagnosing the source, determine whether the noise is from the front axle or the rear axle.

**Test 1 — Remove front driveshaft:**
Drive at the speed where noise is present with the front driveshaft removed. The front axle (on a 4WD XJ) stops rotating without the front driveshaft.
- Noise disappears → front axle/differential or front wheel bearings
- Noise persists → rear axle, rear wheel bearings, or driveshaft

**Test 2 — Driving behavior:**
- Noise that changes when swerving left and right at highway speed suggests a wheel bearing (load shifts side to side)
- Noise that changes with throttle application vs. coast but not with steering input suggests a pinion bearing or ring and pinion issue

---

## Common branches

### Wheel bearing branch

**Sound:** A constant low-pitched hum or growl that is present at highway speed and may increase or decrease with vehicle speed. Distinct from U-joint vibration by its consistent, non-rhythmic character.

**Swerve test:**
Drive at the speed where the noise is loudest. Gently swerve the vehicle left and right (within your lane). If the noise gets louder when swerving in one direction and quieter in the other, the wheel bearing on the loaded side (the side taking more weight during the swerve) is likely failed.
- Noise louder swerving left → right wheel bearing is suspect (weight transfers to the right side)
- Noise louder swerving right → left wheel bearing is suspect

**Jack and wiggle test:**
With the wheel off the ground, grasp the tire at 12 and 6 o'clock and rock it top-to-bottom. Any movement beyond expected flex indicates wheel bearing play.

**1995+ unit bearings:** The sealed unit bearing is the most frequently replaced front axle component on later XJs. The unit bearing also carries the ABS tone ring — a failed bearing can trigger ABS fault codes and an ABS warning light before audible symptoms develop. See [`../../vehicle/systems/axles/dana30-front.md`](../../vehicle/systems/axles/dana30-front.md).

**Rear wheel bearings:** The rear axle uses pressed-in bearings on the axle shaft ends (on the Dana 35 and Chrysler 8.25). Bearing failure here produces a hum at the rear that responds to the swerve test. Inspect for play at the wheel before removing the axle shaft.

---

### Pinion bearing branch

**Sound:** A sustained hum, rumble, or rough-sounding noise at highway speed that does not clearly originate from a wheel end. Pitch may vary with vehicle speed but is less directional than a wheel bearing.

**Load test:**
Drive at a steady highway speed and alternate between light throttle (under light load), coast (foot off throttle, engine braking), and deceleration. Pinion bearing noise typically changes with load — it may be louder under power, louder on coast, or consistent under both, depending on which bearing is failing.

This behavior is distinct from wheel bearing hum, which responds to steering input rather than throttle.

---

### Ring and pinion whine branch

**Sound:** A high-pitched whine or howl that is clearly speed-dependent and load-sensitive. Often described as a "singing" or carrier noise.

**Accel vs. decel pattern:**
- Whine loudest under acceleration (throttle applied) and quieter on coast → drive-side gear wear or incorrect backlash
- Whine loudest on coast (decel) → coast-side gear wear
- Whine at steady cruise, quieter under hard acceleration or hard decel → typically a pinion bearing condition

This pattern is most useful for understanding the nature of ring and pinion wear; an accurate backlash measurement on the axle requires disassembly.

**Distinguishing from wheel bearings:** Ring and pinion whine is usually present across a range of speeds and does not respond to swerving the vehicle. Wheel bearing hum changes with steering input.

---

### Dana 35 rear axle note

The Dana 35 was used as the rear axle on many XJs. It is the smaller of the two rear axle options (the other being the Chrysler 8.25).

The Dana 35 has a known weakness: the axle shafts are smaller and less robust than those in the Chrysler 8.25. Under aggressive use or large tires, the axle shafts are a common failure point. Metal debris from a broken shaft can contaminate the wheel bearing. If a Dana 35 is producing grinding or abnormal noise, inspect not only the bearing but the shaft condition before assuming the bearing alone is the cause.

See [`../../vehicle/systems/axles/dana35-rear.md`](../../vehicle/systems/axles/dana35-rear.md) and [`../../vehicle/systems/axles/identification.md`](../../vehicle/systems/axles/identification.md) to confirm rear axle family.

---

## Exit criteria

- **Wheel bearing:** replace bearing; 1995+ front = unit bearing replacement; rear = axle shaft removal and bearing press service
- **Pinion bearing:** differential disassembly; pinion bearing replacement requires bearing driver and setup experience
- **Ring and pinion:** requires differential rebuild with correct preload and backlash setup
- **Axle shaft failure (Dana 35):** inspect bearing and carrier for debris before deciding between shaft-only and full rebuild

## Related stock reference
- Dana 30 front axle detail: [`../../vehicle/systems/axles/dana30-front.md`](../../vehicle/systems/axles/dana30-front.md)
- Dana 35 rear axle: [`../../vehicle/systems/axles/dana35-rear.md`](../../vehicle/systems/axles/dana35-rear.md)
- Axle identification: [`../../vehicle/systems/axles/identification.md`](../../vehicle/systems/axles/identification.md)
- Axle stock specs: [`../../vehicle/systems/axles/stock-specs.md`](../../vehicle/systems/axles/stock-specs.md)
- Driveshaft vibration: [`driveshaft-vibration.md`](driveshaft-vibration.md)
