# Front Suspension — Jeep Cherokee XJ

## System layout

The XJ front suspension is a solid-axle coil spring four-link system:

- **Two lower control arms** — locate the axle, control longitudinal movement
- **Two upper control arms** — control axle rotation (pinion angle) and longitudinal location
- **Track bar** — single lateral link, prevents side-to-side axle movement
- **Coil springs** — one per side, carry vertical load
- **Shocks** — mounted separately from the springs

The axle itself is the Dana 30 on every 4WD XJ. See `vehicle/systems/axles/dana30-front.md` for axle architecture.

---

## Control arms

### Function

The lower control arms handle the majority of braking and acceleration load. The upper control arms primarily control pinion angle (axle rotation). Both sets locate the axle fore-aft in the chassis.

### Stock dimensions (center-to-center)

| Arm | Stock length |
|-----|-------------|
| Lower | 15.75" |
| Upper | 15.00" |

The stock arms are fixed length — there is no factory adjustment. Arm length changes only with aftermarket replacements.

### Hardware

Stock control arm hardware is metric Grade 10.9:
- Upper arms: M10 × 1.5 × 80mm bolts
- Lower arms: M14 × 2.0 × 120mm bolts

The factory design uses flag bolts at the arm ends — this makes removal difficult, especially on corroded examples. Plan for penetrating oil soak before disassembly.

---

## Track bar

### What it does

The track bar is a single lateral link connecting the driver-side frame rail to the passenger-side axle tube. It prevents the front axle from moving left or right relative to the chassis. Without it (or with a loose or failed one), the axle slides laterally — producing death wobble at speed.

### Why angle matters at lift

At stock ride height, the track bar runs nearly horizontal. When the vehicle is lifted, the frame-side mount rises while the axle-side mount stays at the same height — causing the track bar to angle downward from frame to axle. As lift increases, this angle steepens.

Two problems result:
1. **Reduced lateral control** — a steeply angled track bar is less effective at resisting lateral load
2. **Range-of-motion limit** — at sufficient angle, the track bar ball joint reaches its travel limit and binds

At approximately 3"+ of lift, track bar correction becomes important. See `vehicle/systems/suspension/lift-geometry.md` for correction options.

### Track bar bolt

M10 × 1.5 × 70mm at the axle-side mount.

---

## Caster

### What caster is

Caster is the forward or rearward tilt of the front axle's steering axis. Positive caster means the top of the ball joint axis tilts rearward. More positive caster increases straight-line stability and steering return-to-center. Too little causes wandering and vagueness.

### Stock caster

The XJ's caster is set by the fixed geometry of the control arms and their frame mounting points. It is not adjustable on a stock vehicle. Caster changes when the vehicle is lifted — the axle rotates as it drops relative to the frame, reducing positive caster.

Caster correction after a lift requires aftermarket adjustable control arms. That is an upgrade, not a stock adjustment. See `vehicle/systems/suspension/lift-geometry.md` for what changes at lift.

---

## Ball joints

The Dana 30 uses upper and lower ball joints at each knuckle. Both are greaseable on most years.

**Wear threshold:** Jack the front wheel off the ground and grab the tire at 12 and 6 o'clock positions and attempt to rock it. Any perceptible play in the ball joints is grounds for replacement. A smooth return-to-center when steering out of a turn is also a check — stiff or sticky return can indicate worn or binding ball joints.

Bad ball joints are a known contributor to death wobble. See `vehicle/systems/steering/death-wobble.md`.

---

## Coil springs

The front coil springs are a single unit per side, seated in a pocket on the axle and a cup on the frame. Stock springs vary by trim and load package.

| Spec | Value |
|------|-------|
| Approximate free height | ~18.75" (varies by year/package) |
| Spring type | Coil, compression only |
| UpCountry package | Higher spring rate, ~1" additional ride height |

At lift, coil springs are replaced with taller units — either a dedicated lift spring or a spacer stack on top of the stock spring (budget approach with known drawbacks). Spring replacement is the correct path for lifts of 2.5" and above.

Excessively long control arms cause the coil spring to bow sideways in its pocket. A bowed spring that contacts nothing is acceptable; one that contacts the axle housing or frame is not.

---

## See also

- `vehicle/systems/suspension/overview.md` — system layout and axle identification
- `vehicle/systems/suspension/lift-geometry.md` — what changes at lift
- `vehicle/systems/axles/dana30-front.md` — Dana 30 front axle architecture
- `vehicle/systems/steering/death-wobble.md` — track bar, ball joint, and alignment's role in death wobble

## Sources

NAXJA forums (control arm bolt specs, caster discussion); CherokeeForum; CherokeeTalk; JeepForum; gojeep.willyshotrod.com alignment guide; community-compiled control arm length chart.
