# Renix TPS Adjustment

## Purpose
Set the Throttle Position Sensor (TPS) output voltage to factory specification on Renix-era (1987–1990) XJ and MJ vehicles for correct engine and transmission behavior.

---

## Prerequisites — do these first

### 1. Clean the throttle body
Ensure the throttle body has been recently cleaned, with particular attention to carbon buildup around the edges of the throttle butterfly.

### 2. Test the sensor ground circuit
With the **key off**, set an ohmmeter to its lowest scale. Place the red lead on the **B terminal** of the flat 3-wire TPS connector and the black lead on the negative battery post. Wiggle the harness along the valve cover and near the MAP sensor at the firewall.

- If resistance exceeds **1 ohm** or fluctuates during wiggling: repair the sensor ground harness before adjusting the TPS. See `work/upgrades/electrical/renix-sensor-ground-upgrade.md`.

---

## Tools
- Multimeter or voltmeter
- T20 Torx screwdriver
- Back-probing leads

**Do not unplug any connectors during this procedure.**

---

## Connector identification

### Flat 3-wire connector (all vehicles — engine management)
Terminals are embossed on the connector body:
- **A** — positive (reference voltage)
- **B** — ground
- **C** — output signal

### Square 4-wire connector (automatic transmission vehicles only — transmission control)
Terminals are embossed on the connector body:
- **A** — reference voltage
- **B** — output signal
- **C** — unused
- **D** — ground

Only three of the four terminals are used.

---

## Engine management adjustment (all vehicles)

1. Key **ON**.
2. Back-probe terminals **A** and **B**. Record this as the **reference voltage**.
3. Back-probe terminals **B** and **C**. Record this as the **output voltage**.
4. Calculate the target output: **output = reference × 0.17**
   - Example: 4.82V × 0.17 = **0.82V target**
5. Loosen both T20 Torx screws securing the TPS to the throttle body.
6. Rotate the TPS until the output voltage reaches the target.
7. Carefully tighten the screws while watching the output voltage — confirm it holds at target.
8. If the target voltage cannot be reached: replace the TPS and repeat.

### High idle correction after adjustment
If a high idle develops after adjustment:
1. Shut the engine off.
2. Back-probe terminals **B** and **C**.
3. Start the engine while watching the meter.
4. Rotate the TPS **clockwise** until idle normalizes.
5. Rotate **counterclockwise** back to the target output voltage.

---

## Transmission control adjustment (automatic transmission vehicles only)

1. Key **ON**.
2. Back-probe terminals **A** and **D** on the square 4-wire connector. Record as the **reference voltage**.
3. Back-probe terminals **B** and **D**. Record as the **output voltage**.
4. Calculate the target output: **output = reference × 0.83**
   - Example: 4.8V × 0.83 = **3.98V target**
5. Rotate the TPS until the output reaches the target.
6. If the target cannot be reached: replace the TPS.

---

## Specification summary

| Circuit | Connector | Terminals measured | Target output |
|---------|-----------|-------------------|---------------|
| Engine management | Flat 3-wire | B & C (output), A & B (reference) | 17% of reference |
| Transmission control | Square 4-wire | B & D (output), A & D (reference) | 83% of reference |

---

## Parts note
Manual transmission TPS units are more expensive. The automatic transmission TPS can be substituted on manual transmission applications — the square 4-wire connector simply goes unused.

---

## See also
- `diagnostics/engine/renix-sensor-ground-test.md` — test sensor ground before adjusting
- `work/upgrades/electrical/renix-sensor-ground-upgrade.md` — fix sensor ground if resistance is high
- `vehicle/era1/sensors/tps.md` — TPS connector and wiring reference

## Source
Cruiser54 — cruiser54.com, "Renix TPS Adjustment"
