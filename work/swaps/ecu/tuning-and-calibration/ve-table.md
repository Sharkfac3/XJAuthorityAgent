# Tuning: VE Table (Volumetric Efficiency)

## What it is
The VE table is the core fuel map. It tells the ECU how much air the engine is actually ingesting at any given RPM and load combination. The ECU uses this number, plus injector size and fuel pressure, to calculate pulse width (how long to open the injector).

A VE value of 80% at 2,000 RPM / 60 kPa MAP means the engine is ingesting 80% of the air it theoretically could at that condition. The table is a grid: RPM on one axis, MAP pressure on the other.

## 4.0L VE characteristics
- Strong, relatively flat VE from 1,500–3,500 RPM — this is the engine's torque range
- VE falls off noticeably above 4,000 RPM — these cells matter less for a trail XJ
- Idle cells (low RPM, low MAP / high vacuum) need careful tuning for stable idle
- Peak VE: 80–88% in the mid-range torque band

## Base map starting values
| Region | Starting VE % |
|---|---|
| Idle (600–900 RPM, 20–40 kPa) | 35–50% |
| Light cruise (1,500–2,500 RPM, 40–60 kPa) | 65–75% |
| Part throttle (2,000–3,500 RPM, 60–80 kPa) | 75–85% |
| WOT (all RPM, 95–101 kPa) | 80–90% |

Start slightly rich — a rich base map is safer than a lean one on first start.

## Tuning process
1. Get the engine running on the base map
2. Enable closed-loop O2 correction with ±10% limit
3. Datalog at steady cruise — watch short-term fuel trim (STFT)
4. If ECU is consistently adding fuel (positive STFT), VE cells are too low — increase them
5. If ECU is consistently removing fuel (negative STFT), VE cells are too high — decrease them
6. Goal: STFT hovering near 0% across cruise conditions
7. Use wideband O2 for WOT cells — target 12.5–13.0:1 AFR at WOT
