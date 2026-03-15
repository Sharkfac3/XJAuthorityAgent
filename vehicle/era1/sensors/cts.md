# Era 1: Coolant Temperature Sensor (CTS)

## Specs
- Type: NTC (Negative Temperature Coefficient) thermistor — resistance decreases as temp increases
- Connector: Renix-native 2-pin — see `swap/wiring/connectors/renix-native/cts.md`
- Location: Intake manifold, near thermostat housing

## Resistance curve (Renix-specific)
| Temp °F | Temp °C | Resistance (Ω) |
|---|---|---|
| 32 | 0 | ~29,000 |
| 68 | 20 | ~14,700 |
| 104 | 40 | ~7,600 |
| 140 | 60 | ~4,200 |
| 176 | 80 | ~2,500 |
| 212 | 100 | ~1,500 |

## Swap notes
- Renix CTS uses a different resistance curve than Era 2/3 — do not substitute without updating the calibration table in ECU software
- Open circuit (very high resistance) = ECU reads cold = runs rich, retards timing
- Most open source ECU installs retain the stock sensor and enter the Renix curve into the calibration table
- Alternatively, replace with a GM CTS (widely available, well-documented curve in rusEFI/Speeduino) and use the GM calibration instead
