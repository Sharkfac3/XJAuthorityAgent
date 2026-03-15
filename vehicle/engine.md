# Vehicle: 4.0L AMC/Chrysler Inline Six

## Identity
- Configuration: Inline 6, iron block, iron head
- Displacement: 242 cu in / 3,964 cc
- Bore x Stroke: 3.88" x 3.41"
- Firing order: 1-5-3-6-2-4
- Compression: ~8.8:1 (varies slightly by year)
- Redline: ~5,200 RPM
- Fuel system: Sequential multi-port fuel injection (SMPI) all years in scope
- Ignition: Distributor 1988–1999 / coil rail (waste spark) 2000–2001

## Character
Peak torque (~220 lb-ft) at 2,500–3,000 RPM. Tuning priority is low-to-mid range torque. VE is strong and flat from 1,500–3,500 RPM, falls off above 4,000 RPM.

## Known strengths
Extremely robust bottom end. Simple architecture. Responds well to open source ECU tuning.

## Known weaknesses
- Head cracking near coolant passage at cylinder #3
- Exhaust manifold cracking (common, especially with heat cycling)
- Aging ECU and wiring on all years in scope

## Ignition note
All three eras use an external coil driver — the ECU does not fire the coil directly in any era. The mechanism differs by era; see each era's `vehicle/eraX/power-relay.md`.
