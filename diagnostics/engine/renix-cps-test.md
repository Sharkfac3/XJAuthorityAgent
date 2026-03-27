# Renix CPS Test

## Purpose
Verify the Crankshaft Position Sensor (CPS) is generating adequate voltage to trigger the ECU on Renix-era (1987–1990) XJ and MJ vehicles.

## Why ohms testing is insufficient
A CPS can read correct resistance and still fail to produce enough voltage to trigger the ECU for spark delivery. Resistance testing alone will miss a failing or substandard sensor. The only reliable test is AC voltage output while cranking.

---

## AC voltage test

### Tools
- Multimeter capable of reading AC volts (true-RMS preferred for accuracy on irregular waveforms — cheap meters may give misleading readings)

### Setup
- Unplug the CPS harness connector

### Steps
1. Set multimeter to **AC volts**.
2. Probe both wires in the connector going to the CPS (harness side).
3. Crank the engine.
4. Read the AC voltage output.

### Interpreting results

| Reading | Interpretation |
|---------|---------------|
| 0.5 AC volts or higher | Acceptable |
| 0.35 AC volts or lower | Risk of intermittent crank/no-start |
| 0.2 AC volts | Definite no-start condition |

---

## Known failure patterns

### New parts-store sensors
New CPSs from big-box parts stores have been documented at 0.1–0.3 AC volts while reading correct resistance. Do not trust resistance alone. Source CPSs from NAPA or the dealership.

### Manual transmission — clutch debris
Manual transmission Jeeps accumulate clutch material on the CPS magnetic tip. This reduces voltage output. Clean the tip and retest before condemning the sensor.

### Non-Renix flywheel incompatibility
Non-Renix flywheels (e.g., 1993+ units installed on 1987–1989 engines) generate inadequate CPS signal — as low as 0.1 volts — regardless of sensor condition or mounting. Confirm the correct Renix flywheel is installed if voltage is low and a drivetrain swap has been performed.

### Aftermarket flexplate quality
Aftermarket flexplates have been documented with quality control issues affecting CPS signal. Inspect the reluctor ring for damage or incorrect tooth spacing if voltage is borderline.

---

## Interdependent failures to rule out
Low CPS voltage often appears alongside other Renix electrical faults. If voltage is adequate but no-start persists:
- Check C101 connector condition (1987–1988): `work/maintenance/electrical/renix-connector-and-relay-refresh.md`
- Check ICU/coil contact condition: `work/maintenance/electrical/renix-icu-coil-contact-refresh.md`
- Check sensor ground circuit: `diagnostics/engine/renix-sensor-ground-test.md`

---

## See also
- `work/upgrades/electrical/renix-cps-drill-mod.md` — increase CPS output by optimizing sensor position
- `vehicle/era1/wiring.md` — Era 1 wiring overview
- `work/swaps/ecu/wiring/connectors/renix-native/` — CPS connector specs

## Source
Cruiser54 — cruiser54.com, "Renix CPS Testing and Adjusting"
