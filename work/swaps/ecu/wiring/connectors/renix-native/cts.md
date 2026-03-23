# Renix-Native: CTS and IAT Connector

## Used on
- Coolant temperature sensor (CTS) — Era 1 (1988–1990)
- Intake air temperature sensor (IAT) — Era 1 (1988–1990)
- Both sensors use the same Renix-native 2-pin connector body

## Physical description
- 2-pin proprietary Renix body
- Small rectangular housing, ~12mm wide
- Push-on locking tab
- Connector bodies for CTS and IAT are physically identical — label during removal

## Pinout
| Pin | Circuit |
|---|---|
| A | Sensor signal (NTC thermistor) |
| B | Sensor ground |

## Sourcing
2-pin Renix pigtails are nearly impossible to source new. Check XJ salvage yards for donor harnesses.

## Recommended modern substitute
Replace with a GM coolant temp sensor (also used as IAT) — widely available, standard Chrysler/GM NTC curve, uses a standard Metri-Pack 150 2-pin connector. See `work/swaps/ecu/wiring/connectors/metri-pack/mp150-2pin.md`.

When substituting:
- CTS: Thread-in bung replacement — confirm thread pitch matches Renix housing (typically 3/8"-18 NPT)
- IAT: Install a bung in the intake tube or air cleaner housing
- Update calibration table in ECU software to the GM NTC curve
