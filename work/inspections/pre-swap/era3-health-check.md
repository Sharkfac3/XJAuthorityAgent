# Era 3 Pre-Swap Health Check

## Purpose
Capture the baseline inspection checks worth documenting before an ECU or engine-management swap on a 1996–2001 XJ.

## Scope
This is not a symptom tree. It is an inspection checklist for deciding whether the existing vehicle state is healthy enough to convert without hiding pre-existing faults.

## Checklist
- [ ] Scan and record all stored codes.
- [ ] Clear codes, complete a drive cycle, and rescan so current faults are separated from history codes.
- [ ] Verify crank-sensor function; no active P0335.
- [ ] Verify cam-sensor/distributor-sync function; no active P0340.
- [ ] Verify TPS sweep is smooth; no active P0121, P0122, or P0123.
- [ ] Verify MAP reads barometric pressure key-on engine-off.
- [ ] Verify both O2 sensors are present and reporting plausibly.
- [ ] Confirm no active misfire codes P0300 through P0306.
- [ ] Verify fuel pressure at key-on: 49 psi on most Era 3 years, 39 psi on 1996.
- [ ] Note EVAP faults before the swap even if they are not immediate blockers.
- [ ] Inspect sensor connectors for corrosion, spread terminals, and broken locks.
- [ ] Inspect and clean engine and body ground paths.

## If the vehicle fails this check
Do not treat the swap as the fix.

First route to diagnostics using `diagnostics/engine/era3-control-system-triage.md` or a narrower system diagnostic branch.

## Transition note
This file is the inspection destination split out of `vehicle/era3/diagnostics.md`.
