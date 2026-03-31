# Lift Geometry — Jeep Cherokee XJ

When the XJ is lifted, the entire suspension geometry shifts simultaneously. The stock components were designed for stock ride height. Lifting without addressing geometry produces predictable problems: steering instability, death wobble, driveline vibration, and accelerated component wear.

This page covers what changes and the standard correction approaches. It is a vehicle-facts document — for installation procedures, see `work/upgrades/suspension/`.

---

## What changes when you lift an XJ

### Track bar angle

The front track bar connects the driver-side frame to the passenger-side axle. At stock height it runs nearly horizontal. When lifted, the frame-side mount rises while the axle-side mount stays at axle height — the bar angles down from frame to axle.

Effects of a steepened track bar:
- Reduced lateral axle control
- Ball joint approaches range-of-motion limit (binding at sufficient lift)
- Under suspension travel, the angled bar creates lateral axle movement — felt as bump steer or vagueness over rough surfaces

Track bar correction is generally recommended at 3"+ of lift.

### Caster

Lifting the front end causes the front axle to rotate: the pinion tips down, and the top of the knuckle tips forward. Positive caster decreases. At 3"+ of lift, caster loss is significant enough to cause wandering, reduced return-to-center, and increased susceptibility to death wobble.

Caster also interacts with driveshaft angle — more caster means more pinion-up rotation, which affects the front driveshaft angle into the transfer case.

### Rear driveshaft angle

The rear driveshaft runs from the transfer case output (slip yoke on stock XJ) to the rear axle pinion. Lifting the body moves the transfer case up relative to the axle, increasing the operating angle of the slip yoke into the transfer case output shaft.

At mild lifts (1"–2") this is typically not a problem. At 3"+ of lift, driveline vibration from excessive slip yoke angle becomes common. At higher lifts, the slip yoke can travel far enough during articulation to pull partially out of the transfer case output — causing catastrophic failure.

### Front driveshaft angle

The front driveshaft angle also changes at lift, but is typically less problematic than the rear at moderate lifts because the front driveshaft is shorter and the Dana 30 pinion sits closer to the transfer case. At very high lifts (5"+), front driveshaft angle can become a concern.

### Axle centering

Control arm geometry changes with lift affect where the axle sits fore-aft and side-to-side in the wheel wells. An axle that is off-center will cause unequal tire clearance side-to-side and affect handling.

---

## Track bar correction

Two approaches are in common use:

### Drop bracket (relocation bracket)

A bracket mounts below the factory frame-side track bar mount, lowering it to restore the track bar to a more horizontal angle. Lower cost than an adjustable bar.

**Limitations:**
- If the drag link is not also lowered to match, bump steer results — the track bar and drag link must run in the same plane
- Adds leverage load on the frame-side mount
- Less adjustable than an aftermarket bar; future height changes may require a different bracket

### Adjustable track bar

Replaces the stock track bar with a length-adjustable unit. Length is dialed in to keep the axle centered in the wheel well while maintaining acceptable bar angle.

**Community preference:** The adjustable track bar is the stronger recommendation across NAXJA, CherokeeForum, and JeepForum. It is more flexible for future height changes, works correctly with pinion angle changes from an SYE install, and avoids the additional frame-mount stress of a drop bracket. When budget allows, the adjustable bar is the correct long-term choice.

At any lift, the drag link and track bar should be as parallel to each other as possible. If they run at different angles, suspension travel produces bump steer. Track bar correction addresses the track bar side of this; the drag link angle is a related but separate concern.

---

## Caster correction

Caster is not adjustable on a stock XJ. The control arms are fixed-length and the mounting points are fixed geometry. When the XJ is lifted, caster decreases and cannot be restored without aftermarket adjustable control arms. This is an upgrade decision, not a stock adjustment.

The consequence of uncorrected caster loss is real: wandering, reduced return-to-center, and increased susceptibility to death wobble. It is worth understanding as a geometry problem even if correction is addressed in `work/upgrades/`.

---

## SYE (Slip Yoke Eliminator)

The SYE replaces the rear transfer case slip yoke output with a fixed yoke. A new rear driveshaft with a double-cardan (CV) joint at the transfer case end replaces the stock shaft.

**Why it matters for lift geometry:**
- Eliminates the slip yoke travel problem at high lifts
- The fixed yoke requires the rear pinion angle to be set correctly — the pinion must point at the transfer case output within the operating range of the double-cardan joint
- Setting pinion angle after an SYE requires adjustable rear control arms — cam bolts are a community-disputed alternative with mixed results
- An SYE install and adjustable rear control arms are typically done together

The SYE is a widely documented XJ upgrade. It is a modification, not stock hardware — detailed procedures belong in `work/upgrades/`.

---

## Bump stop extensions

At lift, the factory bump stops (which limit maximum suspension compression) may allow the coil spring, shock, or driveshaft to reach component-damaging positions before the stop engages. Extended bump stops restore the correct compression limit at the new ride height.

Bump stop extensions are a small but often overlooked part of a complete lift kit. Most quality lift kit packages include them; budget or partial lift kits may not.

---

## Summary: what a complete lift correction involves

| Problem | What addresses it |
|---------|------------------|
| Track bar angle | Adjustable track bar (preferred) or drop bracket |
| Caster loss | Aftermarket adjustable control arms (not a stock fix) |
| Rear driveline vibration at 3"+ | SYE + CV driveshaft (aftermarket upgrade) |
| Bump stop gaps | Extended bump stops |
| Alignment | Professional alignment after any geometry change |

Each of these is a real problem that manifests if the lift is done without addressing it.

---

## See also

- `vehicle/systems/suspension/front.md` — caster spec, track bar, control arm dimensions
- `vehicle/systems/suspension/rear.md` — rear spring geometry and lift options
- `vehicle/systems/steering/overview.md` — drag link and track bar relationship
- `vehicle/systems/steering/death-wobble.md` — how geometry failures produce death wobble

## Sources

JeepForum (adjustable track bar vs. drop bracket threads); NAXJA (track bar, caster, SYE discussions); CherokeeForum; JKS Manufacturing product documentation; Synergy Manufacturing steering kit fitment notes; community-compiled caster correction guidance.
