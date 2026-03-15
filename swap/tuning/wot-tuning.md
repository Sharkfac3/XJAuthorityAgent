# Tuning: WOT Tuning

## Safety first
⚠️ Do not perform WOT tuning runs on public roads where it is not safe or legal to do so. WOT pulls require a safe, legal environment — a closed course, a track, or private property with adequate runout. Never tune at WOT in traffic or on public streets.

## What WOT tuning involves
At wide open throttle the engine is in open loop — the ECU ignores the narrowband O2 sensor and runs purely from the VE table and ignition table. The goal is to hit the target AFR (12.5–13.0:1) consistently across all WOT RPM cells.

## Required equipment
A wideband O2 sensor and controller is mandatory for WOT tuning. The narrowband sensor cannot measure AFR at WOT. See `swap/ecu-selection/wideband.md`.

## Process
1. Verify the engine is fully warmed up and idle/cruise tuning is complete
2. Enable wideband input logging in ECU software
3. Perform a full-throttle pull from ~2,000 RPM to redline (or target shift point)
4. Review the datalog — plot wideband AFR against RPM through the pull
5. Identify cells that are lean (AFR above 13.2:1) — increase VE value in those cells
6. Identify cells that are excessively rich (AFR below 12.0:1) — decrease VE value
7. Repeat until AFR is consistent at 12.5–13.0:1 through the entire RPM range
8. After fuel is dialed in, verify ignition timing under WOT load — watch for knock

## 4.0L WOT characteristics
The 4.0L is a torque engine — it does not make significantly more power above 4,500 RPM. Most real-world WOT use for a trail XJ is at 2,000–3,500 RPM during hill climbs. Prioritize tuning accuracy in that range over peak RPM cells.

## Ignition at WOT
Start conservative — 14–16° BTDC at WOT. Advance in 1° increments with datalogging to confirm no knock. The 4.0L is not sensitive to timing at WOT the way a high-compression engine is, but detonation on old iron is still worth avoiding.
