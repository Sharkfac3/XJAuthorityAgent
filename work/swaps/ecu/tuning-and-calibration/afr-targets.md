# Tuning: AFR Targets

## What AFR means
AFR (Air/Fuel Ratio) is the ratio of air mass to fuel mass in the combustion mixture. Stoichiometric (perfect combustion) for gasoline is 14.7:1. Below 14.7 is rich (more fuel). Above 14.7 is lean (less fuel).

## Target AFR by operating condition

| Condition | Target AFR | Notes |
|---|---|---|
| Cold start | 8.0–11.0:1 | Rich for cold combustion — ECU handles via cranking enrichment |
| Cold idle (warming up) | 12.0–14.0:1 | Richer until coolant temp reaches ~160°F |
| Warm idle | 14.0–14.7:1 | Near stoich — stable, clean idle |
| Light cruise | 14.7–15.5:1 | Slightly lean of stoich — fuel economy |
| Part throttle | 13.5–14.7:1 | Transition region |
| WOT (full power) | 12.5–13.0:1 | Rich for power and heat management |
| Decel / overrun | N/A | Fuel cut active — no target |

## Trail use considerations
For a wheeled XJ running technical terrain at low speed:
- Do not tune the low-RPM, part-throttle cells lean — a lean stumble at 2 mph on a rock is dangerous
- Target 14.0–14.5:1 in the low-speed trail zone rather than going for maximum economy
- Hot restart enrichment is important — fuel in the lines vaporizes after a hard run on a hot day

## Measurement
AFR targets are only meaningful with a calibrated wideband O2 sensor. The stock narrowband sensor cannot measure actual AFR — it only indicates rich or lean of stoichiometric. See `work/swaps/ecu/sensors-and-inputs/wideband-o2.md`.
