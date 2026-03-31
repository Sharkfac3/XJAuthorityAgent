# AW4 Automatic Transmission

## Identity
- Manufacturer: Aisin Warner (Japan)
- Full designation: Aisin Warner 4 (AW4)
- Type: 4-speed automatic overdrive with torque converter lockup
- XJ years: 1987–2001 (all 4.0L automatics; also used with 2.5L through 1990)
- Also used in: MJ Comanche, some Toyota applications
- Drain plug marking: "DII" (original Dexron II spec, now superseded — see fluid section)

---

## Gear ratios

| Gear | Ratio (1987–1990) | Ratio (1991–2001) |
|------|--------------------|-------------------|
| 1st | 2.804:1 | 2.804:1 |
| 2nd | 1.531:1 | 1.531:1 |
| 3rd | 1.000:1 | 1.000:1 |
| OD (4th) | 0.705:1 | 0.753:1 |
| Reverse | 2.393:1 | 2.393:1 |

The overdrive ratio change coincides with the 4.0L HO upgrade and the output shaft spline change (21-spline pre-1991, 23-spline 1991+).

---

## Fluid specification

**Use: Dexron III/Mercon or Dexron VI (modern equivalent)**

Do NOT use ATF+4. A Chrysler TSB specifically states ATF+4 does not apply to the AW-4. Community experience on NAXJA and JeepForum documents cases where ATF+4 caused torque converter clutch chatter and lockup failure. Dexron III is no longer produced; Dexron VI is its backwards-compatible replacement and is the correct modern fluid.

The drain plug is stamped "DII" (Dexron II) — this is an artifact of the original spec, not a current recommendation.

---

## Shift solenoids

Gear selection is electronically controlled via two on/off solenoids and hydraulically assisted via throttle valve cable pressure.

| Gear | Solenoid 1 | Solenoid 2 |
|------|-----------|-----------|
| 1st | ON | OFF |
| 2nd | ON | ON |
| 3rd | OFF | ON |
| OD | OFF | OFF |

A third solenoid (TCC solenoid) locks the torque converter clutch. It activates in 3rd or OD only.

**Solenoid resistance:** 11–15 ohms at operating temperature. Measure at the TCM harness to rule out wiring faults before pulling the pan.

Common fault codes:
- P0700 — Transmission Control System Malfunction
- P0758 — Shift Solenoid B Electrical (Solenoid 2)

Solenoids can be replaced with a pan drop — no full transmission removal required.

---

## TPS interaction

The AW4's TCM reads throttle position sensor voltage from the engine harness.

- Expected range: ~0.5 V (closed throttle) to ~4.5 V (wide open throttle)
- Reference supply: 5 V
- Signal type: continuous analog voltage

TPS voltage affects:
- shift aggressiveness and kickdown behavior
- torque converter lockup timing

A failing or miscalibrated TPS can cause delayed shifts, harsh kickdown, or early lockup clutch engagement. This is one of the most common external causes of AW4 shift complaints.

Cross-references:
- [`../../era1/sensors/tps.md`](../../era1/sensors/tps.md) — Renix-era TPS baseline
- [`../../era2/sensors/tps.md`](../../era2/sensors/tps.md) — SBEC-era TPS baseline
- `work/swaps/ecu/integration/aw4-tps.md` — TPS wiring in ECU-swap context

---

## Common failures

**Shift solenoids** — Most AW4 shift complaints trace back to solenoids or the TPS signal rather than internal mechanical failure. Check solenoid resistance and TPS voltage before condemning the transmission.

**Heat buildup** — The AW4 is a light-to-medium-duty transmission that generates heat under load. Towing, off-road low-speed work, or a failing torque converter lockup clutch (which runs the fluid hotter) accelerates wear. An auxiliary cooler is a common preventative addition on working XJs.

**Torque converter lockup clutch** — The lockup clutch can fail or chatter if wrong fluid is used (see ATF+4 warning above) or if TCC solenoid function is degraded. Symptoms: high RPM at highway speed, transmission heat.

---

## Output shaft spline count

- 1987–1990: 21-spline output shaft
- 1991–2001: 23-spline output shaft

This affects transfer case input shaft compatibility. Most NP231 and NP242 transfer cases from 1992+ have 23-spline inputs.

---

## Boundary links
- AW4 TCM/TPS wiring context: [`aw4/overview.md`](aw4/overview.md)
- Transfer case overview: [`../transfer-case/overview.md`](../transfer-case/overview.md)
- ECU-swap TPS integration: `work/swaps/ecu/integration/aw4-tps.md`

## Sources
Community-verified via NAXJA ("Everything you ever wanted to know about the AW4"), JeepForum AW4 fluid and solenoid threads, CherokeeTalk fluid discussions; Chrysler TSB on ATF+4 incompatibility; Novak Conversions AW4 guide.
