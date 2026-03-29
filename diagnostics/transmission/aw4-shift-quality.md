# AW4 Shift Quality

## Purpose
Fault-isolate harsh shifts, soft/slipping shifts, and torque converter lockup problems on the AW4 automatic transmission (1987–2001 XJ).

## Symptom definition
Use this leaf when the AW4's shift behavior has changed from its baseline: shifts that feel too hard or too soft, noticeable TCC lockup shudder, or the transmission holding a gear it should have left.

## Do not use this leaf when
- The transmission will not upshift or holds one gear regardless of throttle → a gear-selection fault, not a shift-quality fault
- Slipping under load with dark/burnt fluid → start with [`aw4-fluid-condition.md`](aw4-fluid-condition.md) first; mechanical damage from fluid neglect changes the diagnostic path
- No-crank or no-start → route to [`../charging-and-starting/no-crank.md`](../charging-and-starting/no-crank.md)

---

## First checks

1. Check fluid condition before chasing electronics — dark, burnt, or low fluid changes everything. See [`aw4-fluid-condition.md`](aw4-fluid-condition.md).
2. Confirm the throttle valve (TV) cable moves freely through its full travel. A misadjusted or sticking TV cable is a mechanical cause that mimics solenoid faults.
3. Check for stored transmission codes. The TCM stores DTC codes; P0700 (transmission control system) or P0758 (solenoid B electrical) narrow the path quickly.

---

## Common branches

### Throttle valve cable branch
The AW4 uses a TV cable (throttle pressure cable) that runs from the throttle body to the transmission. This cable directly controls line pressure and shift feel.

- **Harsh shifts:** Cable adjusted too tight → excessive line pressure at all throttle positions
- **Soft or late shifts:** Cable too loose → insufficient pressure
- **Test:** With engine off, manually move the cable end at the throttle body through full travel. It should move smoothly with no binding and return crisply. Check the cable at the transmission end for fraying near the bracket.

Adjustment is a common first fix before chasing electronics.

### TPS voltage branch
The AW4 TCM reads the TPS signal from the engine harness to determine shift aggressiveness and kickdown behavior. A faulty or out-of-range TPS will cause erratic or incorrect shift behavior.

Expected TPS range at TCM:
- Closed throttle: ~0.5 V
- Wide open throttle: ~4.5 V

See [`../../vehicle/systems/transmission/aw4/overview.md`](../../vehicle/systems/transmission/aw4/overview.md) for stock control relationships.

### Shift solenoid branch
The AW4 has three solenoids:
- Solenoids 1 and 2 (shift solenoids A and B): control gear selection
- Solenoid 3 (TCC solenoid): locks the torque converter clutch in 3rd and overdrive

**Test method:** Disconnect the solenoid connector at the transmission pan. Measure resistance between the solenoid terminal and the mounting bracket (ground).

- Expected resistance: **11–15 ohms** at operating temperature
- A solenoid reading open (OL) or shorted (near 0 ohm) is failed
- A solenoid can read correct cold but fail warm — if intermittent, an analog meter sweep is more revealing than a single DMM reading

Relevant codes:
- P0758 — Shift Solenoid B Electrical
- P0740 — Torque Converter Clutch Circuit Malfunction
- P0700 — Transmission Control System (general TCM fault)

### TCC lockup shudder branch
Shudder or roughness on converter lockup engagement (typically 35–45 mph, light throttle) points to solenoid 3 or converter condition.

- Test solenoid 3 resistance at the pan connector (same 11–15 ohm spec)
- TCC shudder can also result from fluid friction modifier depletion — a full fluid change with fresh Dexron III sometimes resolves shudder without further diagnosis
- If shudder persists after fresh fluid and solenoid tests clean, suspect torque converter internal wear (a rebuild/replacement decision)

---

## Exit criteria

Route out of this leaf when evidence points to:
- **TV cable misadjustment** → adjustment or cable replacement; no further electrical diagnosis needed
- **TPS fault** → engine management branch; see era-specific triage in `diagnostics/engine/`
- **Solenoid fault** → solenoid replacement; accessible via pan drop without transmission removal
- **Converter shudder after solenoid and fluid checks** → torque converter mechanical condition; repair decision point

## Related stock reference
- AW4 stock baseline: [`../../vehicle/systems/transmission/aw4/overview.md`](../../vehicle/systems/transmission/aw4/overview.md)
- Fluid type and pan drop: [`aw4-fluid-condition.md`](aw4-fluid-condition.md)
