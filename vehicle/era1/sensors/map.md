# Era 1: MAP Sensor

## Specs
- Type: 1-bar analog
- Location: Firewall-mounted (not on intake manifold)
- Connected to intake manifold via vacuum hose (~3/16" ID)
- Output: 0.5V at full vacuum → 4.5V at atmospheric (~100 kPa)
- Reference voltage: 5V
- Connector: Renix-native 3-pin — see `work/swaps/ecu/wiring/connectors/renix-native/map.md`

## Calibration
At key-on engine-off, MAP should read barometric pressure (~100 kPa at sea level). Use this as a calibration check before first start.

## Failure notes
Renix MAP sensors fail with age. The vacuum hose also cracks and causes false lean readings. Inspect hose before condemning the sensor.

## Swap notes
- Renix MAP sensor uses a Renix-specific voltage curve — not interchangeable with Era 2/3 MAP sensors without recalibration in ECU software
- Most open source ECU installs replace the Renix MAP with a modern 1-bar sensor mounted on the intake manifold
- If replacing, use a standard GM 1-bar MAP (widely supported in rusEFI and Speeduino) and update the sensor calibration table
- Relocating from firewall to intake manifold shortens the vacuum path and improves response
