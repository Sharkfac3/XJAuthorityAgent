# Renix Sensor Ground Test

## Purpose
Test the sensor ground circuit on Renix-era (1987–1990) XJ and MJ vehicles to isolate poor grounds as a cause of driveability faults.

## Why this matters
The sensor ground circuit feeds the CTS, TPS, IAT, MAP, ECU, and diagnostic connector grounds. A poor crimp anywhere in the harness degrades the ground for all of them simultaneously. This test should be performed early in any Renix driveability diagnosis — before replacing sensors.

---

## Test procedure

### Tools
- Digital ohmmeter

### Setup
- Ignition: OFF

### Steps
1. Set the ohmmeter to measure resistance (ohms).
2. Place the **red (positive) lead** on the **B terminal** of the flat 3-wire TPS connector. Terminal letters are embossed on the connector body.
3. Place the **black (negative) lead** on the **negative battery post**.
4. Read the resistance.
5. While watching the meter, wiggle the wiring harness that runs parallel to the valve cover and near the MAP sensor at the firewall.
6. **1987–1988 models only:** Also wiggle the C101 connector mounted above the brake booster.

### Expected result
- Resistance should be as close to **0 ohms** as possible.
- Resistance should **remain low and stable** while wiggling harnesses and connectors.

### Failed result
- Any elevated resistance reading.
- Resistance that **changes while wiggling** — indicates a poor crimp or bad connection somewhere in the circuit.

---

## Interpreting the results

Variance during wiggling points to the engine dipstick tube stud ground as the most likely fault. That stud is the shared ground point for the sensor ground circuit.

### Next steps on failure
- Refresh the dipstick tube stud and all engine grounds: `work/maintenance/electrical/renix-ground-refresh.md`
- If still elevated after refresh, check for a broken or poorly crimped wire in the harness between the TPS connector and the stud.

---

## See also
- `work/maintenance/electrical/renix-ground-refresh.md` — restore factory grounds
- `work/upgrades/electrical/renix-ground-upgrades.md` — supplemental ground cables
- `vehicle/era1/wiring.md` — Era 1 wiring overview
- `vehicle/era1/sensors/tps.md` — TPS connector pin details

## Source
Cruiser54 — cruiser54.com, "Renix Sensor Ground Test"
