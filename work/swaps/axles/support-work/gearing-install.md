# Ring-and-Pinion and Locker Installation

Setup overview for ring-and-pinion installation and locker/differential selection in the Dana 60 and Sterling 10.50 for XJ Cherokee one-ton builds.

For ratio selection and locker options, see: [`../../../../sourcing/interchange/axles/one-ton-gearing.md`](../../../../sourcing/interchange/axles/one-ton-gearing.md)

---

## When to do this work

Gear installation can happen at different points in the build:

- **Before axle installation** — easier access, can work on a bench with the housing on stands. Preferred if you already know the housing will not need further disassembly.
- **After axle installation** — required if the housing was narrowed after gears were installed, or if the build is being done in stages.

**Either way, gears and lockers must be installed and properly set up before the vehicle is driven.**

## Ring-and-pinion setup overview

This is precision work. If you have not set up gears before, consider having a professional gear shop do the installation. Incorrect setup causes noise, premature wear, and potential catastrophic failure.

### Critical setup parameters

| Parameter | What it controls | Consequence if wrong |
|-----------|-----------------|---------------------|
| Backlash | Clearance between ring and pinion teeth | Too tight: overheating, binding. Too loose: gear whine, clunking. |
| Pinion depth | How deep the pinion sits in the carrier | Wrong contact pattern — accelerated wear, noise, possible tooth breakage |
| Pinion bearing preload | Resistance of the pinion bearings | Too loose: pinion wanders, kills pattern. Too tight: bearing overheating. |
| Carrier bearing preload | Resistance of the carrier bearings | Too loose: backlash wanders. Too tight: bearing overheating. |
| Contact pattern | Shape of the tooth contact on the ring gear | The ultimate verification — tells you if depth and backlash are correct |

### Setup procedure summary

1. **Install the pinion** — set the pinion depth using shims behind the pinion head bearing (inner bearing). Install the pinion nut and set bearing preload to spec (typically 15–25 in-lb for new bearings).
2. **Install the ring gear on the carrier** — torque ring gear bolts to spec with thread locker. Install the carrier in the housing with carrier bearing caps.
3. **Set backlash** — adjust the carrier shim packs (or adjuster rings) to achieve the specified backlash range (typically 0.006–0.010" for both Dana 60 and Sterling 10.50, but verify against the gear manufacturer's spec sheet).
4. **Check the contact pattern** — paint the ring gear teeth with gear marking compound, rotate the ring gear against the pinion under light load. The pattern should show:
   - **Drive side:** contact centered on the tooth face, slightly toward the toe
   - **Coast side:** contact centered, slightly toward the heel
5. **Adjust if needed** — if the pattern is too deep or too shallow, adjust pinion depth shims. If the pattern is too close to the toe or heel, adjust backlash.
6. **Final torque and check** — re-torque all fasteners, re-check backlash and preload, run a final pattern check.

## Carrier break points

### Dana 60
- **Break point: ~4.10**
- Ratios 4.10 and numerically lower (3.73, 3.55, etc.) → standard carrier
- Ratios steeper than 4.10 (4.56, 4.88, 5.13, 5.38) → thick/deep carrier
- If re-gearing from a stock 3.73 or 4.10 to 4.88, you likely need a new carrier

### Sterling 10.50
- **Break point: ~3.73**
- Ratios 3.73 and numerically lower → standard carrier
- Ratios steeper than 3.73 (4.10, 4.56, 4.88, etc.) → thick/deep carrier
- Since virtually all one-ton XJ builds use 4.56 or steeper, you will need the high-ratio carrier

**Always verify the carrier break with the gear manufacturer.** Some manufacturers have slightly different break points.

## Locker installation

### Types

**Selectable lockers** (ARB, Eaton E-Locker):
- Install in place of the carrier side gears and spider gears
- Require an actuation system (air lines for ARB, wiring for E-Locker)
- Route the actuation lines/wires from the differential through the axle vent or a dedicated port, along the frame to the cab
- ARB requires an onboard air compressor and switch
- E-Locker requires a switch and wiring to the differential

**Automatic lockers** (Detroit Truetrac):
- Drop-in replacement for the carrier's internal gears
- No external actuation — the differential locks automatically under torque
- Simplest installation of all locker types

**Full-case lockers** (Detroit Locker):
- Replace the entire carrier assembly
- Always locked — both axle shafts turn together at all times
- Tire chirp on paved turns (normal)
- No setup required beyond installing the carrier with correct shims/preload

**Lunchbox lockers** (Spartan, Aussie):
- Replace only the spider gears inside the stock open carrier
- Cheapest locker option
- Not as strong as full-case or selectable lockers — generally not recommended for one-ton builds with 37"+ tires

### Recommended combinations for one-ton XJ

| Use case | Front | Rear |
|----------|-------|------|
| Street/trail dual-use | ARB or E-Locker (selectable) | ARB or Detroit Truetrac |
| Trail-focused | ARB (selectable) | Detroit Locker or ARB |
| Budget trail | Open or lunchbox | Detroit Locker |

## Professional vs DIY

Gear setup is one of the most precision-critical jobs in a one-ton build. The tools required include:
- Dial indicator with magnetic base
- Inch-pound torque wrench (for preload measurement)
- Bearing puller and press
- Gear marking compound
- Pinion depth gauge (or careful measurement with calipers)

If you do not have these tools and experience reading contact patterns, **strongly consider professional installation**. A poorly set-up gear set will destroy itself quickly and take the carrier with it.

---

## Related
- Gearing and locker selection: [`../../../../sourcing/interchange/axles/one-ton-gearing.md`](../../../../sourcing/interchange/axles/one-ton-gearing.md)
- Driveshaft work (pinion angle): [`driveshaft-work.md`](driveshaft-work.md)
