# Renix Sensor Ground Upgrade

## Purpose
Replace the factory crimp splices in the Renix sensor ground circuit with soldered connections to eliminate the most common source of sensor ground resistance on 1987–1990 XJ and MJ vehicles.

## Why this matters
The sensor ground circuit feeds the CTS, TPS, IAT, MAP, ECU, and diagnostic connector. The factory splices in this circuit are crimped and covered with duct tape — a known failure point that causes high resistance across all downstream sensors simultaneously. This upgrade eliminates those splices permanently.

Perform `diagnostics/engine/renix-sensor-ground-test.md` first to confirm this circuit is the fault before cutting into the harness.

---

## Tools and materials
- Wire stripper
- Soldering iron and solder
- Heat-shrink tubing or electrical tape
- Split-loom sheathing
- Zip ties

---

## Procedure

### Step 1: Locate the IAT sensor
The Intake Air Temperature (IAT) sensor is positioned just to the rear of the throttle body. It has 2 wires and screws into the intake manifold.

### Step 2: Trace the brown/white wire from the IAT
Remove split-loom sheathing from the IAT connector and follow the **brown/white striped wire** back through the harness.

### Step 3: Find the first splice
You will find a splice joining **3 wires** to a single wire:
- **1987–1988 models:** The single wire runs toward the C101 connector mounted above the brake booster.
- **1989–1990 models:** The single wire runs along the firewall toward the engine (no C101).

The factory splice is crimped and wrapped in duct tape.

### Step 4: Trace the MAP sensor ground
Follow the brown/white wire from the MAP sensor. It leads to a second splice joining **2 more brown/white wires**, also covered in duct tape.

### Step 5: Consolidate and solder
1. Cut out both factory splices, removing the single wire that connected them between the two splice points.
2. Bring both sets of wires together (the 3-wire set and the 2-wire set).
3. Solder all wires together into one consolidated joint.
4. Insulate with heat-shrink tubing or electrical tape.

### Step 6: Secure the new loom
1. Zip-tie the new sensor ground loom to allow for engine movement.
2. Cover with new split-loom sheathing or wrap neatly with electrical tape.

---

## Year-specific notes
| Model year | C101 connector | Splice wire routing |
|------------|---------------|---------------------|
| 1987–1988 | Yes (above brake booster) | Splice runs to C101 |
| 1989–1990 | No | Splice runs along firewall toward engine; may have additional wires involved |

---

## See also
- `diagnostics/engine/renix-sensor-ground-test.md` — verify the circuit has high resistance before cutting
- `work/maintenance/electrical/renix-ground-refresh.md` — restore factory grounds first
- `vehicle/era1/wiring.md` — Era 1 wiring overview
- `vehicle/era1/sensors/iat.md` — IAT sensor location and connector details
- `vehicle/era1/sensors/map.md` — MAP sensor details

## Source
Cruiser54 — cruiser54.com, "Sensor Ground Upgrade"
