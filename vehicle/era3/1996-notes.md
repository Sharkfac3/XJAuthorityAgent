# Era 3: 1996 Transition Year Notes

## The problem
OBD-II compliance was federally mandated for all U.S. vehicles from January 1, 1996. Chrysler was required to implement it before the broader 1997 harness and sensor refresh was ready. The result: the 1996 XJ has a JTEC OBD-II ECU running on an OBD-I era harness with OBD-I era sensors.

## What is OBD-II on a 1996
- JTEC ECU (silver/gray box — same as 1997–2001)
- OBD-II 16-pin DLC diagnostic port
- Generic OBD-II scanner reads codes

## What is still OBD-I era on a 1996
- Sensor connectors: Metri-Pack 150 from Era 2, not updated
- Sensor calibration curves: Same as Era 2 CTS, MAP, TPS
- Engine harness routing and connector locations: Same as Era 2
- Injector connectors: EV1 (same physical plug as Era 1 and Era 2) — EV6 did not arrive until 1999
- Injectors themselves: **not** Era 2 holdovers — 1996 uses new grey 53030778 at 49 psi (same part as 1997–1998); not the tan 53030343 Era 2 part at 39 psi
- Fuel pressure: 49 psi (returnless system) — same as all other Era 3 years

## Practical effect on the swap
- When sourcing replacement **sensors** for a 1996, use Era 2 part numbers — connectors and calibration curves are Era 2
- When sourcing **injectors** for a 1996, use Era 3 part numbers (53030778) — not Era 2 tan injectors
- When sourcing connector pigtails, use Era 2 connector families
- ECU connector itself is JTEC — use `work/swaps/ecu/wiring/connectors/ecu-body/jtec.md`
- Treat the 1996 as an Era 2 harness with an Era 3 ECU

## ⚠️ Parts sourcing trap
Many parts stores and online listings treat 1996 as a clean break to the new era. The ECU is new-era; most of the harness is not. Always confirm the actual connector and sensor type on the vehicle before ordering.
