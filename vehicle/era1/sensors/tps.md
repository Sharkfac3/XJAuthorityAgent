# Era 1: Throttle Position Sensor (TPS)

## Specs
- Type: Potentiometer
- Output: 0.5V closed throttle → 4.5V wide open throttle (WOT)
- Reference voltage: 5V
- Connector: Renix-native — see `swap/wiring/connectors/renix-native/tps.md`
- Note: Some Renix TPS units have an additional idle switch contact (4-pin). Confirm with FSM for specific year.

## Testing
Use a DVOM on the signal wire while sweeping throttle slowly from closed to WOT. Signal must be smooth with no dead spots, jumps, or dropouts. Any irregularity = replace the TPS.

## Swap notes
- TPS output range (0.5V–4.5V) is compatible with open source ECU input expectations
- Calibrate closed throttle and WOT positions in ECU software after installation
- Renix TPS connector is not shared with Era 2/3 — if replacing the TPS with a modern unit, verify connector compatibility or plan a pigtail adapter
