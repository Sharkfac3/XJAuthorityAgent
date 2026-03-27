# Renix CPS Drill Mod

## Purpose
Increase CPS voltage output on Renix-era (1987–1990) XJ and MJ vehicles by optimizing sensor-to-flywheel/flexplate proximity.

## Why this helps
CPS output voltage is determined in part by how close the sensor tip sits to the reluctor ring. The factory upper mounting hole limits how far the sensor can be positioned. Enlarging or slotting the hole allows the sensor to be pushed closer, increasing signal strength.

Perform `diagnostics/engine/renix-cps-test.md` first to confirm low voltage output before modifying.

---

## Procedure

### Modify the mounting hole
- Drill the **upper mounting hole** from the stock **5/16"** to **3/8"**.
- Alternatively, slot the upper hole in the bracket.

### Install and position
1. Use an 11mm socket wrapped in electrical tape to hold the mounting bolt during installation — this prevents dropping the bolt into the bell housing.
2. Insert the CPS into the modified hole.
3. Push the sensor **as close to the flywheel/flexplate as possible**.
4. Tighten the bolts while holding the sensor at maximum depth.

### Verify
Retest AC voltage output per `diagnostics/engine/renix-cps-test.md`. Target 0.5 AC volts or higher while cranking.

---

## Notes
- This mod is additive — it does not replace the need for a quality sensor. If the sensor itself is defective, the mod will not compensate.
- Confirm the correct Renix flywheel or flexplate is installed before performing this mod. Non-Renix units produce inadequate signal regardless of sensor position.

## See also
- `diagnostics/engine/renix-cps-test.md` — test before and after this mod
- `vehicle/era1/wiring.md` — Era 1 wiring overview

## Source
Cruiser54 — cruiser54.com, "Renix CPS Testing and Adjusting"
