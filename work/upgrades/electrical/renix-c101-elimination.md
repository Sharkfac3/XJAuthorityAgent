# Renix C101 Connector Elimination

## Purpose
Permanently bypass the C101 bulkhead connector on 1987–1988 Renix XJ and MJ vehicles by splicing the harness wires directly together, eliminating the connector as a future fault point.

## Applies to
1987–1988 XJ and MJ only. Jeep removed the C101 from the factory harness in 1989.

## Why this matters
The C101 is a multi-pin firewall bulkhead connector above the brake booster on the driver's side. It is prone to pin corrosion, loosening, and continuity loss over decades. Refreshing it (see `work/maintenance/electrical/renix-connector-and-relay-refresh.md`) buys time; elimination removes the problem permanently.

---

## Tools and materials
- 1/4″ socket
- Soldering iron
- Solder
- Heat-shrink tubing
- 3/4″ split loom
- Electrical tape
- Ohmmeter (if wire colors are faded)

---

## Procedure

### Step 1 — Disassemble the C101
1. Unbolt the two halves of the C101 using a 1/4″ socket.
2. Remove the plastic covers where wires enter each half (these typically break during removal — that's fine).
3. Lightly bolt the connector back together away from the firewall to keep the halves organized during the splice process.

### Step 2 — Expose the harnesses
1. Peel back the split-loom covering on the **body side** down to where the harness splits toward the firewall (approximately below the MAP sensor).
2. Remove split loom on the **engine side** the same distance.

### Step 3 — Splice the wires — one pair at a time
**Cut and solder one matching pair at a time.** Do not cut multiple pairs before soldering — wires are difficult to match once separated from the connector.

Approximately 22 connections total.

For each pair:
1. Cut the matching wires to approximately 1/2″ on each side of the connector.
2. Slide heat-shrink tubing over one wire.
3. Solder the two wires together.
4. Slide the shrink tubing over the solder joint and heat to seal.

**If wire colors are faded:** Use an ohmmeter to confirm matching wires before cutting. Reference connector pin positions if needed.

**Wires with no match:** Leave unconnected but insulate the end with heat-shrink or tape.

### Step 4 — Sensor ground treatment
Both C101 halves contain a **brown wire with white tracer**. These are part of the sensor ground circuit and require special handling — do not simply solder them together with the other pairs.

1. Follow each brown/white wire back until you find where **three wires are crimped together**.
2. Cut out the factory crimp from each set of three wires.
3. Bring both sets of three wires together (6 wires total).
4. Solder all 6 wires into one consolidated joint.
5. Insulate with heat-shrink tubing.

This procedure mirrors the sensor ground upgrade: `work/upgrades/electrical/renix-sensor-ground-upgrade.md`.

### Step 5 — Final assembly
1. Bundle all completed wires in new 3/4″ split loom.
2. Tape and secure to the C101's original bolt hole on the firewall, or another secure firewall location.

---

## Notes
- Work in a well-ventilated area when soldering.
- A gas-powered soldering iron is useful if working under the dash without access to an outlet.
- This is a permanent modification — there is no reversal without rebuilding the harness.

---

## See also
- `work/maintenance/electrical/renix-connector-and-relay-refresh.md` — temporary refresh if not eliminating
- `work/upgrades/electrical/renix-sensor-ground-upgrade.md` — sensor ground splice details
- `vehicle/era1/wiring.md` — Era 1 wiring overview

## Source
Cruiser54 — cruiser54.com, "C101 Elimination"
