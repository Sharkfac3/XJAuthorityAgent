# Era 2: Coolant Temperature Sensor (CTS)

## Specs
- Type: NTC thermistor
- Connector: Metri-Pack 150 2-pin — see `swap/wiring/connectors/metri-pack/mp150-2pin.md`
- Location: Intake manifold coolant passage

## Resistance curve (Chrysler — different from Renix)
| Temp °F | Temp °C | Resistance (Ω) |
|---|---|---|
| 32 | 0 | ~29,330 |
| 86 | 30 | ~10,970 |
| 140 | 60 | ~3,840 |
| 194 | 90 | ~1,552 |
| 248 | 120 | ~700 |

## Swap notes
- Chrysler CTS curve is supported in rusEFI and Speeduino
- Open circuit = ECU reads cold = runs rich, retards timing
- Can be replaced with a GM CTS with appropriate calibration update
