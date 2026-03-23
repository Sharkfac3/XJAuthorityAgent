# Era 1: Intake Air Temperature Sensor (IAT)

## Specs
- Type: NTC thermistor (same family as CTS, similar curve)
- Location: Air cleaner housing or intake tube
- Connector: Renix-native 2-pin — see `work/swaps/ecu/wiring/connectors/renix-native/cts.md` (same connector as CTS)
- Resistance curve: Similar to Renix CTS curve — verify against FSM

## Swap notes
- Same calibration considerations as CTS — Renix curve differs from Era 2/3
- Can be replaced with a GM IAT sensor with appropriate calibration update
