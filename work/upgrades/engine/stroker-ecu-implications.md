# Stroker ECU Implications — Jeep 4.0L

Stroking the 4.0L changes the engine's displacement, which directly affects the Required Fuel calculation — the baseline injector pulse width the ECU derives from engine volume, injector flow rate, and target air/fuel ratio. Understanding what the stock ECU can and cannot handle is a prerequisite for planning any stroker build.

---

## Stock injector flow rates by ECU era

| ECU | Years | Injector | Flow rate |
|-----|-------|----------|-----------|
| SBEC | 1991–1995 | Brown / Tan | ~21 lb/hr @ 39 psi |
| JTEC | 1996–1999 | Grey (53030778) | ~23 lb/hr @ 49 psi |
| JTEC | 1999–2001 | Blue tip (04854181) | ~22.5 lb/hr @ 49 psi |

Note: 1996+ engines run higher fuel pressure (49 psi vs. 39 psi). Injector flow rate scales with the square root of the pressure differential — do not compare lb/hr figures from different test pressures directly.

---

## What the stock ECU can handle

The SBEC and JTEC ECUs run closed-loop fueling referenced to the upstream O2 sensor. They calculate injection pulse width from MAP, IAT, RPM, and injector flow rate, then trim in real time. This gives them limited self-correction ability when engine displacement changes.

The stock ECU's closed-loop O2 trims have finite authority. With correctly sized injectors installed, the ECU can compensate for some additional displacement demand at light load and idle — but at WOT the engine runs open-loop and the ECU relies entirely on its calibrated tables, which were not written for a stroked engine. At WOT on a stroked engine with a stock ECU, fueling accuracy is not guaranteed and leaning out under load is a real risk.

The practical community consensus from JeepStrokers.com and NAXJA is: a stock ECU is a liability on a real stroker build. It may idle and cruise acceptably, but full-throttle fueling accuracy and any meaningful ignition tuning require a standalone ECU or a properly reflashed OEM ECU.

**JTEC-specific limitations:**
- 1998+ JTEC Jeeps route gauge signals through the PCM on the CAN bus. Replacing the PCM outright with a standalone ECU requires replacing or adapting gauges.
- Automatics: The JTEC sends the VSS signal to the TCU via the bus. A full ECU swap requires addressing TCU communication.
- OBD-II port: Required for emissions testing in many states. A standalone ECU eliminates native OBD-II compliance.

These are real integration costs, not just fuel map concerns. They are part of the build decision.

---

## Injector sizing for a stroker

A larger-displacement engine at the same power-per-liter produces proportionally more fuel demand. Use this formula to verify injector sizing:

```
Required injector flow (lb/hr) = (Target HP × BSFC) / (cylinders × max duty cycle)
```

Where BSFC ≈ 0.50 for a naturally aspirated engine, cylinders = 6, max duty cycle ≈ 0.80 (80%).

Example for 240 hp target:
```
(240 × 0.50) / (6 × 0.80) = 120 / 4.8 = 25 lb/hr per injector
```

Stock 22–23 lb/hr injectors are marginal at 240 hp. **Ford 24 lb/hr injectors** are a well-documented community upgrade for the 4.6L stroker — they fit the stock fuel rail and have been used successfully with stock and aftermarket ECUs. Verify compatibility with the specific rail and ECU.

For forced induction or aggressive NA builds, calculate at the expected peak HP and size injectors with headroom to stay below 80% duty cycle.

---

## Aftermarket ECU options

For any stroker build that exceeds the stock ECU's correction range, or for forced induction, a standalone ECU is the correct path. These are the options with documented Jeep 4.0L community use:

**MegaSquirt (MS-I, MS-II, MS3Pro):**
- Well-documented on the 4.0L, particularly on distributor-based engines (1991–1999)
- MS-II with MSD box and coil is a popular approach for pre-DIS engines
- Does not support drive-by-wire
- MS3Pro does not natively support Jeep's crank trigger pattern on all versions — verify before purchase
- Sequential fuel injection not available on all variants

**Speeduino:**
- Arduino Mega-based, documented community support for 1991–1998 4.0L
- Lower cost than MegaSquirt; capable for basic stroker builds
- Active open-source development — check current compatibility documentation

**rusEFI:**
- Open-source; less Jeep-specific documentation than MegaSquirt but capable hardware
- Tuneable for displacement, VE table, ignition advance

For all standalone ECUs, the following parameters must be set correctly for a stroker:
- Engine displacement (cc or ci)
- Injector flow rate (lb/hr or cc/min at test pressure)
- VE (volumetric efficiency) table — requires dyno tuning or a good base map and road tuning
- Ignition timing table

See `work/swaps/ecu/` for ECU swap execution guidance and wiring details.

---

## Summary

| Scenario | ECU path |
|----------|----------|
| Mild stroker, stock compression, not pushing WOT hard | Stock ECU may idle and cruise acceptably with correctly sized injectors; WOT accuracy is not guaranteed |
| Any stroker build where WOT fueling accuracy matters | Standalone ECU or reflashed OEM ECU strongly preferred |
| Any forced induction on a stroked engine | Standalone ECU required |

---

## See also

- `work/upgrades/engine/stroker-overview.md` — what changes in a stroker build
- `work/upgrades/engine/stroker-combinations.md` — parts and displacement specs
- `work/swaps/ecu/` — standalone ECU swap execution

## Sources

JeepStrokers.com (Pottenger); NAXJA ECU and injector threads; JeepForum; CherokeeForum aftermarket ECU discussion; HPTuners forum JTEC injector scaling thread; injector flow data from jeep4.0performance.4mg.com tech specs.
