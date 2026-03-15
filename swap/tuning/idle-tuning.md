# Tuning: Idle Tuning

## Target idle speed
- In gear (automatic, drive): 650–750 RPM
- Out of gear / neutral / manual: 750–850 RPM
- Cold idle (below 160°F): 900–1,100 RPM — higher idle compensates for cold friction
- A/C on (if controlled): Add ~100–150 RPM via idle-up table

## IAC (Idle Air Control) setup
The IAC stepper motor bleeds air past the throttle blade to control idle speed. The ECU steps the IAC open or closed to hit the target RPM.

### Initial setup sequence
1. With engine off, command IAC to a known position (typically 50% open) via ECU software
2. Set base idle screw on throttle body so engine idles at ~600 RPM with IAC fully closed
3. Start engine — IAC should open automatically to reach target RPM
4. If idle is too high with IAC closed, back off the idle screw slightly
5. If idle is too low even with IAC fully open, open the idle screw slightly

### IAC open-loop vs closed-loop idle
- **Open loop idle:** ECU holds IAC at a fixed position based on coolant temp — simple, stable, less responsive to load changes
- **Closed loop idle:** ECU actively adjusts IAC position to hit target RPM — handles A/C, alternator load, and other variables better

Start with open loop until idle is stable, then enable closed loop idle control.

## Idle VE cells
Low RPM / low MAP cells in the VE table directly affect idle quality. If the engine hunts (RPM surging up and down):
- Check for vacuum leaks first — a leak makes the mixture lean at idle and causes hunting regardless of the VE table
- If no vacuum leak, richen the idle VE cells incrementally (2–3% at a time)
- Watch AFR at idle with wideband — target 14.0–14.7:1

## Common idle problems
| Symptom | Most likely cause |
|---|---|
| High idle, IAC fully closed | Vacuum leak — find and fix before adjusting anything else |
| Hunting / surging idle | Lean idle cells, vacuum leak, or IAC not responding |
| Idle drops when in gear (auto) | IAC not compensating for torque converter load — adjust idle-up in gear table |
| Cold idle too low | Cold idle enrichment or cold IAC position table needs adjustment |
| IAC not stepping at key-on | IAC wiring issue or stepper driver not functioning |
