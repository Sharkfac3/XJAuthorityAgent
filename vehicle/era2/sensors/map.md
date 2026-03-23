# Era 2: MAP Sensor

## Specs
- Type: 1-bar analog
- Location: Intake manifold (directly mounted)
- Output: ~1.0V at high vacuum (idle) → ~4.5V at atmospheric (WOT)
- Reference voltage: 5V
- Connector: Metri-Pack 150 3-pin — see `work/swaps/ecu/wiring/connectors/metri-pack/mp150-3pin.md`

## Voltage reference points
| Condition | MAP kPa | Approx voltage |
|---|---|---|
| High vacuum / idle | ~20 kPa | ~1.0V |
| Part throttle | ~60 kPa | ~2.5V |
| Atmospheric / WOT | ~101 kPa | ~4.5V |

## Calibration check
At key-on engine-off, MAP should read barometric pressure (~100 kPa at sea level). Deviation indicates a failed sensor or vacuum leak at the sensor port.

## Swap notes
- Era 2 MAP sensor is directly compatible with most open source ECU installs
- The Chrysler 1-bar MAP calibration curve is supported in rusEFI and Speeduino
- Alternatively, swap to a GM 1-bar MAP — same mounting, widely supported, easy to source
- Vacuum hose condition is critical — a cracked hose causes false lean readings at idle
