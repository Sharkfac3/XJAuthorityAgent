# NP231 Shift Issues

## Purpose
Fault-isolate NP231 (and NP242) engagement and range-selection problems: difficulty engaging 4WD, binding on pavement, and popping out of range.

## Symptom definition
Use this leaf when the transfer case will not shift into a range, pops out of a range, or causes driveline binding while engaged.

## Do not use this leaf when
- The main complaint is a noise from the transfer case with no shift problem → [`np231-noise.md`](np231-noise.md)
- The 4WD problem is at the front axle only and the transfer case shifts normally → route to `vehicle/systems/4wd/front-axle-disconnect.md` for CAD diagnosis

---

## Background: what the NP231 is and is not

The NP231 is a **part-time** transfer case. It has no center differential. In 4WD High or Low, the front and rear output shafts are locked together at a fixed ratio.

This means:
- **4WD is only correct on loose traction surfaces** (dirt, gravel, snow, mud)
- **4WD on high-traction pavement causes driveline binding** — this is normal, not a fault

The NP242 (Selec-Trac) adds a full-time 4WD mode with an open center differential. NP242-equipped XJs can use 4WD on pavement in the full-time mode without binding.

See [`../../vehicle/systems/transfer-case/overview.md`](../../vehicle/systems/transfer-case/overview.md) for identification and year matrix.

---

## Common branches

### Binding on pavement branch

**What it feels like:** The vehicle feels like it is fighting itself during turns — a strong push-back or hopping sensation, especially in tight turns.

**Cause:** This is not a fault. Part-time 4WD on high-traction pavement causes torsional wind-up between the front and rear axles because the drivetrain cannot accommodate the speed difference between inside and outside wheels during turns.

**Correct action:** Return the transfer case to 2WD before driving on dry pavement. If the vehicle was recently driven in 4WD on pavement, the wind-up may make shifting back to 2WD difficult — find a loose surface (dirt, grass, wet pavement), back up slightly, and try the shift again. This releases the torsional load.

---

### Difficulty engaging 4WD branch

**First: confirm whether the problem is the transfer case or the front axle.**
On pre-~1991 Command-Trac XJs, a Central Axle Disconnect (CAD) uses a vacuum actuator to engage the passenger-side inner axle shaft. If the CAD system fails, the transfer case may shift correctly but the front axle does not engage. The vehicle will act as if it is in 2WD even with the transfer case in 4H.

See [`../../vehicle/systems/4wd/front-axle-disconnect.md`](../../vehicle/systems/4wd/front-axle-disconnect.md) for CAD vacuum system diagnosis.

**Linkage adjustment:**
The floor shifter connects to the transfer case via a rod or cable linkage. If the linkage is out of adjustment or the bushings are worn, the internal detent positions may not fully engage.

- Check for worn or torn shifter linkage bushings — a common failure on high-mileage XJs
- Basic adjustment: place the transfer case in 4H, loosen the linkage adjustment point (varies by year — typically under the vehicle near the case), ensure the internal detent is fully seated, then retighten
- If the case pops out of gear after adjustment, the internal cam or detent plate may be worn

**Detent ball and spring:**
The NP231 uses a detent ball and spring to hold range positions. A weak spring or worn detent can cause the case to pop out of 4H or 4L. This is an internal repair.

**Vacuum switch (CAD-equipped models):**
On CAD-equipped XJs (~1984–1991 Command-Trac), a vacuum switch on the transfer case signals the CAD actuator when 4WD is selected. This switch and the vacuum lines serving it are 30+ years old on any surviving vehicle. Common failures: cracked vacuum lines, deteriorated fittings, failed switch.

Inspect:
- All vacuum hoses from the switch to the reservoir and actuator for cracks and collapsed connectors
- The vacuum switch itself — disconnect the hose at the switch and check for vacuum with the case in 4H

---

### Popping out of range branch

The most common cause is linkage that is not fully seating the detent, followed by worn internal detent components.

1. Verify linkage adjustment first (see above)
2. If the case was recently rebuilt or the SYE kit was installed, confirm the detent plate and ball were reinstalled correctly
3. Persistent pop-out after correct linkage adjustment indicates internal cam wear — rebuild or case replacement

---

## Exit criteria

- **Binding on pavement:** operator correction; no repair needed
- **Difficulty engaging / CAD vacuum fault:** vacuum system service in `work/`; see `vehicle/systems/4wd/`
- **Linkage issue:** adjustment or bushing replacement; `work/maintenance/`
- **Internal detent or cam wear:** transfer case rebuild or replacement decision

## Related stock reference
- Transfer case identification and specs: [`../../vehicle/systems/transfer-case/overview.md`](../../vehicle/systems/transfer-case/overview.md)
- 4WD engagement system and CAD: [`../../vehicle/systems/4wd/overview.md`](../../vehicle/systems/4wd/overview.md)
- Front axle disconnect detail: [`../../vehicle/systems/4wd/front-axle-disconnect.md`](../../vehicle/systems/4wd/front-axle-disconnect.md)
- Noise from the transfer case: [`np231-noise.md`](np231-noise.md)
