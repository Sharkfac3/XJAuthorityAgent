# Era 1: Injectors

## Specs
- Part number: 53003956
- Flow rate: ~19–21 lb/hr at 39 psi (sources vary; treat as ~19 lb/hr for base map)
- Fuel pressure: 39 psi
- Impedance: High — ~14–16 ohm (saturated drive)
- Drive type: Saturated — standard low-side ground switching, no peak-and-hold needed
- Connector: EV1 (Bosch Jetronic) — 2-pin wide-body
- Spray pattern: Single hole, top-feed

## Connector note
EV1 connectors on 1988–1990 vehicles are 30+ years old. The plastic becomes brittle and the locking tab often breaks on removal. Inspect before reusing. See `work/swaps/ecu/wiring/connectors/ev1-bosch/injectors.md` for release procedure and sourcing.

## TunerStudio / ECU swap reference
- Enter flow rate as **~19 lb/hr** at 39 psi for Required Fuel calculation (conservative end of the source range)
- Fuel pressure: 39 psi
- Injector dead time (open time): 0.9–1.5 ms typical starting point — calibrate against actual injector spec sheet if available

## Upgrade options
All upgrades must retain EV1 (Bosch Jetronic) connector or use an adapter harness. All XJ injectors are High-Z — any High-Z replacement is compatible with the Ocelot and other aftermarket ECUs without resistors.

### Direct-fit community-verified options
- **Lincoln Town Car 4.6L** (1990–1991): ~19 lb/hr @ 36 psi, 4-hole spray pattern, EV1 connector — confirmed direct fit for Renix. Status: `confirmed` — source: community (Cherokee Talk)

### Ford Motorsport cross-reference (EV1 compatible)
| Part number | Flow rate @ 39 psi |
|---|---|
| FMS-M9593-C302 | ~19 lb/hr |
| FMS-M9593-A302 | ~24 lb/hr |
| FMS-M9593-B302 | ~30 lb/hr |

### Bosch EV14 series (Jetronic/EV1 connector)
EV14 injectors are preferred for upgrade builds — faster armature response allows a larger flow rate injector to still idle cleanly.
Catalog numbers for EV1/Jetronic connector: 62385, 62687, 62203
Status: `needs verification` — sourced from community reference; confirm connector type before ordering.

### Sizing guidance
Size injectors to keep duty cycle below 80% at max power. Most stock-displacement 4.0L builds do not need to exceed 24 lb/hr. Larger injectors can make idle tuning harder.

## Swap compatibility
- Era 1 injectors are compatible with Era 2 physically (same EV1 connector, same fuel pressure)
- Not directly compatible with Era 3 (different fuel pressure — 49 psi vs 39 psi — and EV6 connector on 1997+)
- Many builders upgrade to newer injectors at swap time — if doing so, note connector change and recalculate flow rate for new fuel pressure
- Aftermarket injectors with EV1 connectors are widely available and drop straight in
