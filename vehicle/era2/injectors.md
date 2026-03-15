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
See `swap/wiring/connectors/ev1-bosch/injectors.md` for release procedure.

## Swap compatibility
- Era 2 injectors are physically identical to Era 1 (same EV1 connector, same 39 psi fuel pressure)
- Not directly compatible with Era 3 (49 psi fuel pressure, EV6 connector on 1997+)
- Aftermarket drop-in replacements with EV1 connectors are widely available
- If upgrading injector size at swap time, recalculate dead time and flow rate for the new injector
