# Era 2: Throttle Position Sensor (TPS)

## Specs
- Type: Potentiometer
- Output: 0.5V closed throttle → 4.5V WOT
- Reference voltage: 5V
- Connector: Metri-Pack 150 3-pin — see `swap/wiring/connectors/metri-pack/mp150-3pin.md`
- Location: Throttle body, driver's side

## Testing
Sweep throttle slowly from closed to WOT while monitoring signal voltage with a DVOM. Must be smooth and linear with no dead spots, dropouts, or jumps. Any irregularity = replace.

## AW4 interaction
The TPS signal wire is tapped by the AW4 automatic transmission TCM. The AW4 uses TPS voltage to determine shift aggressiveness and torque converter lockup timing. See `swap/wiring/aw4-tps.md` for full details.

## Swap notes
- TPS output range (0.5V–4.5V) is standard and compatible with all open source ECUs
- Calibrate closed throttle and WOT endpoints in ECU software after installation
- Do not cut or re-route the TPS signal wire going to the AW4 — it must remain intact
- Era 2 TPS uses the same Metri-Pack 150 3-pin connector as the MAP sensor — connectors are physically identical, label them during removal
