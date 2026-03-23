# Era 2: Injectors

## Specs
- Flow rate: ~21 lb/hr at 39 psi
- Fuel pressure: 39 psi
- Impedance: High — ~12–16 ohm (saturated drive)
- Drive type: Saturated — standard low-side ground switching, no peak-and-hold needed
- Connector: EV1 (Bosch Jetronic) — 2-pin wide-body
- Spray pattern: Single hole, top-feed

## Part numbers
- 1991–1993: 33007127 (brown)
- 1994–1995: 53030343 (tan)

## Connector note
EV1 connectors age poorly. Locking tabs become brittle. Inspect all 6 before reuse.
See `work/swaps/ecu/wiring/connectors/ev1-bosch/injectors.md` for release procedure.

## TunerStudio / ECU swap reference
- Enter flow rate as **~21 lb/hr** at 39 psi for Required Fuel calculation
- Fuel pressure: 39 psi
- Injector dead time (open time): 0.9–1.5 ms typical starting point — calibrate against actual injector spec sheet if available

## Upgrade options
All upgrades must retain EV1 (Bosch Jetronic) connector or use an adapter harness. Same connector and pressure as Era 1 — upgrade options are identical.

### Ford Motorsport cross-reference (EV1 compatible)
| Part number | Flow rate @ 39 psi |
|---|---|
| FMS-M9593-C302 | ~19 lb/hr |
| FMS-M9593-A302 | ~24 lb/hr |
| FMS-M9593-B302 | ~30 lb/hr |

### Bosch EV14 series (Jetronic/EV1 connector)
Catalog numbers for EV1/Jetronic connector: 62385, 62687, 62203
Status: `needs verification` — confirm connector type before ordering.

### Sizing guidance
Stock-displacement 4.0L at street power levels stays well within the stock 21 lb/hr injectors. Upgrade only if supporting forced induction or a significant stroker build. Keep duty cycle below 80% at max power.

## Swap compatibility
- Era 2 injectors are physically identical to Era 1 (same EV1 connector, same 39 psi fuel pressure)
- Not directly compatible with Era 3 (49 psi fuel pressure, EV6 connector on 1997+)
- Aftermarket drop-in replacements with EV1 connectors are widely available
- If upgrading injector size at swap time, recalculate dead time and flow rate for the new injector
