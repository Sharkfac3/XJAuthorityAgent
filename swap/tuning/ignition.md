# Tuning: Ignition Timing

## Base timing
Set base timing to 8–10° BTDC as a conservative starting point. Verify with a timing light after initial configuration — do not trust software display alone until it has been confirmed against physical timing marks.

## Timing table targets for 4.0L
| Condition | Timing (° BTDC) |
|---|---|
| Idle (vacuum, ~20 kPa) | 12–18° |
| Light cruise (~40–60 kPa) | 28–36° |
| Part throttle (~70–80 kPa) | 22–28° |
| WOT (~101 kPa) | 14–18° |

These are starting points. Advance carefully — verify with datalogging.

## Advance cautiously
Add timing in small increments (2° at a time). After each change, datalog the condition and watch for:
- Knock sensor activity (if equipped)
- Unusual combustion sounds (pinging, rattling under load)
- Any AFR changes that suggest detonation-induced rich condition

## Knock threshold for 4.0L
The cast iron head is relatively knock-resistant on 87 octane. However, the engine is old — carbon deposits raise effective compression. If running 87 octane, err conservative on timing at high load.

## Vacuum advance equivalent
The stock system used vacuum advance to add timing at light load (high vacuum / low kPa). Replicate this in the ECU timing table by advancing timing at low MAP values. This is important for fuel economy at highway cruise.

## Verifying with timing light
1. Warm engine to operating temperature
2. Connect timing light to cylinder 1 plug wire
3. Note ECU-commanded timing at idle
4. Compare to timing marks on harmonic balancer
5. If physical timing differs from ECU display, adjust trigger offset in ECU software until they match
6. This verification step is mandatory before any road tuning
