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

## Engine variants in scope
- **Renix 4.0L (1988–1990)** — 177 hp / 224 lb-ft. Flat-tappet rockers, Renix ECU + ICM, proprietary oil filter thread.
- **HO 4.0L (1991–2001)** — 190 hp / 225 lb-ft. Roller rockers, revised head and intake, standard oil filter thread. See `vehicle/era2/ho-engine.md` for full HO identity and mechanical profile.

## Character
Peak torque at 2,500–3,000 RPM (Renix) or 4,000 RPM (HO). Tuning priority is low-to-mid range torque. VE is strong and flat from 1,500–3,500 RPM, falls off above 4,000 RPM.

## Known strengths
Extremely robust bottom end. Simple architecture. Responds well to open source ECU tuning.

## Known weaknesses
- Head cracking near coolant passage at cylinder #3 — 0331 casting (2000–mid-2001) is most vulnerable; see [`vehicle/systems/cooling/head-cracking.md`](systems/cooling/head-cracking.md)
- Exhaust manifold cracking (common, especially with heat cycling) — see [`vehicle/systems/engine/exhaust-manifold.md`](systems/engine/exhaust-manifold.md)
- Aging ECU and wiring on all years in scope

## Ignition note
All three eras use an external coil driver — the ECU does not fire the coil directly in any era. The mechanism differs by era; see each era's `vehicle/eraX/power-relay.md`.
