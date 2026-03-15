# Era 3: Ignition — Coil Rail / Waste Spark (2000–2001)

## System overview
No distributor. A single coil rail assembly spans all 6 cylinders and mounts along the valve cover. Each coil in the rail fires two cylinders simultaneously — one on compression stroke (useful spark), one on exhaust stroke (wasted spark). No cap, rotor, or plug wires.

## Waste spark pairing
| Coil output | Cylinders fired | Notes |
|---|---|---|
| Output 1 | 1 & 6 | Fire simultaneously |
| Output 2 | 2 & 5 | Fire simultaneously |
| Output 3 | 3 & 4 | Fire simultaneously |

## Components
- Coil rail: Single assembly with 6 individual coil towers, one per cylinder
- Spark plug boots: Short boots directly on plug — no separate plug wires
- Cam sensor: Hall effect, relocated to front of engine at camshaft gear

## Open source ECU requirements
- 3 ignition outputs minimum (one per coil pair)
- Cam sensor input still required for sequential injection phase detection
- Cam sensor location changes — wire from front of engine, not from distributor area

## Swap options
1. **Keep coil rail** — wire 3 ignition outputs to coil rail. Simpler electrically, requires ECU with 3+ ignition outputs. Preferred.
2. **Retrofit distributor** — install distributor from 1991–1999 donor. Requires matching the distributor drive gear and verifying fitment. Allows use of simpler single-output ECU configuration.

## Swap notes
- Option 1 (keep coil rail) is recommended — less hardware change, more reliable
- Verify open source ECU has 3 configurable ignition outputs before purchasing
- Cam sensor pigtail location is different from 1996–1999 — plan wiring routing accordingly
