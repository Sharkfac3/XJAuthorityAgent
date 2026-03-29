# Death Wobble

## Purpose
Fault-isolate and systematically diagnose death wobble on the XJ Cherokee — violent front-end oscillation triggered by a road input.

## Symptom definition
Death wobble is a violent, self-sustaining front-end oscillation that typically occurs at highway speeds (roughly 45–65 mph) and is triggered by hitting a bump, expansion joint, or uneven pavement. Once started, the oscillation does not immediately dampen out on its own and requires slowing down to stop it.

**Death wobble is not:**
- Normal road wander or loose steering feel
- A shimmy that occurs only under braking
- Vibration felt through the seat or floor at all speeds (a driveline vibration)

## Do not use this leaf when
- There is only vague steering wander with no violent oscillation → `wander-or-loose-steering.md`
- The vehicle shakes at all speeds above a threshold without requiring a bump to start → likely wheel balance or tire issue first

---

## Why it happens

The XJ's front axle is a solid beam axle located laterally by a single track bar. When any component in the steering or suspension has enough play, a road input can set the axle moving laterally. As it moves, the play in other worn components allows the motion to amplify rather than dampen — the result is violent self-sustaining oscillation.

Death wobble is almost never caused by a single bad component. It is a **compound fault** — the combination of play in multiple components that allows oscillation to amplify. Fixing only one worn part often fails to cure the wobble if other components still have play.

---

## Likely causes in order of probability

1. **Track bar** — worn bushings, loose end bolts, or elongated bolt holes at the frame mount
2. **Drag link / tie rod ends** — worn ball joints at the drag link or tie rod allow axle oscillation to be transmitted into the steering linkage
3. **Ball joints** — worn upper or lower ball joints on the Dana 30 allow steering knuckle movement that feeds back into the wobble
4. **Front wheel bearings** — loose unit bearings (1995+) or adjusted-out roller bearings (pre-1995) allow lateral wheel movement
5. **Tire balance or inflation** — an out-of-balance tire provides the initiating input; wobble may disappear or become intermittent with tire work

---

## Diagnostic sequence

### Step 1: Tires first
Check tire pressures and inspect tires for irregular wear, cupping, or obvious imbalance. An out-of-balance tire is the trigger; fixing the trigger may make death wobble uncommon enough to live with — but if slop exists in the steering/suspension, it will return. Get the tires balanced correctly before the more involved inspection.

### Step 2: Track bar inspection

The track bar is the single most common component implicated in XJ death wobble. It connects the axle to the frame and prevents lateral axle movement.

**Track bar frame-side bolt:**
- The frame-side mount on the XJ is known to elongate the bolt hole over time, especially on high-mileage vehicles
- A loose or wallowed-out frame mount allows the axle to move laterally under load
- Torque spec for the track bar frame mount bolt: **125 ft-lbs**; check with a torque wrench before assuming the bushing is worn

**Bushing condition:**
- Inspect both ends of the track bar for cracked, compressed, or extruded rubber bushings
- A worn bushing allows movement that a new bushing with proper torque would prevent

**Two-person test:** Have an assistant sit in the driver's seat and slowly turn the steering wheel no more than ¼ turn in each direction while you observe the track bar connection at the passenger-side axle mount. The track bar end should not move relative to the axle bracket before the bracket itself starts to move. If the bushing compresses and the bar end moves before the axle moves, the bushing is shot.

### Step 3: Drag link and tie rod ends

With the vehicle on a lift or on jack stands, grasp the drag link near each end and attempt to push/pull it side-to-side while watching the ball joint stud. Any movement of the stud in the socket indicates a worn joint.

Repeat for the tie rod ends.

### Step 4: Ball joints

Ball joint wear contributes to oscillation by allowing the steering knuckle to move unpredictably. For Dana 30 inspection:
- Grasp the tire at 9 and 3 o'clock and attempt to shake it side-to-side (steering play check — tie rods vs. steering box)
- Grasp the tire at 12 and 6 o'clock and attempt to rock it top-to-bottom (wheel bearing vs. ball joint check)
- For ball joints specifically: place a pry bar under the tire and watch the upper and lower ball joint studs for movement while rocking the tire up

See [`../../vehicle/systems/axles/dana30-front.md`](../../vehicle/systems/axles/dana30-front.md) for Dana 30 ball joint and hub details by year.

### Step 5: Wheel bearings

On 1995+ XJs with unit bearings: check for wheel bearing lateral play with the tire on the ground. A worn unit bearing can introduce enough lateral slop to sustain oscillation.

On earlier XJs with serviceable roller bearings: check adjustment.

---

## Important: compound faults

In most death wobble cases on high-mileage XJs, more than one component is worn. Fixing the track bar bushings alone when the tie rod ends and ball joints are also worn will often reduce but not cure the wobble. A thorough inspection of all steering and suspension components is the right approach — not chasing one part at a time.

---

## Exit criteria

- **All components inspect clean but wobble persists:** return to tire balance and suspension angles; consider whether a suspension lift has introduced unfavorable geometry
- **Track bar mount elongated:** the frame-side mount plate may need drilling to oversize and a larger bolt, or a replacement bracket weld
- **Multiple worn components:** replace all worn items in the same service to avoid incremental repairs that still leave the problem present

## Related stock reference
- Dana 30 front axle detail (ball joints, unit bearings): [`../../vehicle/systems/axles/dana30-front.md`](../../vehicle/systems/axles/dana30-front.md)
- Steering system overview: [`../../vehicle/systems/steering/overview.md`](../../vehicle/systems/steering/overview.md)
- Steering box sector adjustment: [`steering-box.md`](steering-box.md)
