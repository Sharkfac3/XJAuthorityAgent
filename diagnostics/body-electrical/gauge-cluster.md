# Gauge Cluster

## Purpose
Fault-isolate XJ gauge cluster failures: distinguish ground faults from sender/sensor problems, identify the temperature sender vs. ECU sensor confusion, and address cluster contact issues.

## Symptom definition
Use this leaf when one or more gauges in the instrument cluster is reading incorrectly, erratically, or not at all.

## Do not use this leaf when
- No electrical issue is present — gauge reads correctly but you suspect the vehicle is actually running hotter or cooler than indicated → confirm with a mechanical or infrared thermometer, then route to the appropriate diagnostic branch
- A warning light (check engine, ABS, oil pressure) is on without gauge issues → route to the appropriate system diagnostic

---

## Critical: multiple gauges failing together vs. single gauge failing alone

**Multiple gauges fail together → suspect a ground fault first.**

The speedometer, tachometer, and fuel gauge share a common ground circuit. If all three fail simultaneously, the cluster's common ground connection is degraded before any individual sender or component is at fault.

See [`ground-faults.md`](ground-faults.md) before replacing parts when multiple gauges are involved.

**Single gauge fails alone → suspect that gauge's sender or sensor.**

---

## Temperature gauge: sender vs. ECU sensor

This is one of the most common XJ diagnostic mistakes. The XJ has **two separate temperature-sensing components** located near the thermostat housing. They are not interchangeable and they serve different functions.

| Component | Connector type | Function | Failure symptom |
|-----------|---------------|----------|-----------------|
| Temperature gauge sender | Single-pin connector | Sends variable resistance signal to the instrument cluster gauge | Gauge reads cold, pegged high, or erratic |
| ECU coolant temperature sensor (CTS) | Multi-pin connector (typically 2-pin) | Sends temperature data to the PCM for fuel and spark management | Check engine light; rough running; no effect on gauge |

Replacing the multi-pin CTS when the gauge is wrong does nothing. Replacing the single-pin sender when the engine is running rough does nothing. Identify which component is the correct one before replacement.

**Visual identification:** Both are threaded sensors near the thermostat housing. The gauge sender has a single wire. The ECU sensor has a multi-pin connector. On some XJ configurations they may be at slightly different locations on the housing or intake manifold — confirm with a wiring diagram for the specific year before replacement.

---

## Common branches

### Temperature gauge — reads cold or no movement

**Most likely:** failed gauge sender (single-pin connector)

**Test:** Disconnect the sender wire and briefly ground it to the engine block with the ignition on. If the gauge swings to hot (or pegs high), the gauge and its circuit are functional — the sender is the fault. If the gauge does not respond when the wire is grounded, the fault is in the gauge circuit or the cluster itself.

### Temperature gauge — pegged hot or reads hot continuously

**Most likely:** open circuit (broken wire, disconnected connector) OR failed sender that has gone open

**Test:** Disconnect the sender wire with the ignition on. A gauge that reads full hot with the wire disconnected indicates an open-circuit reading behavior — the sender wire may be broken or the connector is off. A gauge that drops to cold when the wire is disconnected confirms the circuit is intact and the sender itself is reading high.

### Fuel gauge inaccurate or stuck

**Most likely:** sending unit in the fuel tank

The fuel sending unit is mounted in the fuel pump module inside the tank. It uses a float arm and variable resistor — expected resistance range approximately 0–88–90 ohms (empty to full, varies slightly by year). A sending unit that drifts out of calibration or has a worn resistor track will read inaccurately across the range or stick at a fixed reading.

**Test:** With a wiring diagram for the specific year, measure resistance at the gauge cluster connector on the sender signal wire. Compare to expected range for the fuel level. If resistance is out of range, the sender unit is failed. If resistance is correct but the gauge reads wrong, the gauge or its circuit is suspect.

### Speedometer and tachometer failure

**If both fail together:** almost always a cluster common ground fault. See [`ground-faults.md`](ground-faults.md).

**If speedometer fails alone (1996+ OBD-II XJs):** the speedometer is driven by a vehicle speed sensor (VSS) signal from the transmission output shaft. Check for VSS-related diagnostic codes.

### Cluster contacts backing out

The instrument cluster connector contacts are press-fit into plastic housings. On high-mileage XJs, individual pins can back out of their sockets, causing intermittent or complete gauge loss.

**Symptom pattern:** Gauges work, then fail, then work again — sometimes corresponding to hitting a bump or jarring the dash.

**Fix:** Pull the instrument cluster, inspect the connector housing on the back of the cluster, and press any backed-out contacts firmly back into their sockets. Cleaning the contacts with electrical contact cleaner and reseating them resolves most intermittent cluster issues without cluster replacement.

---

## Exit criteria

- **Multiple gauges failed together:** ground fault diagnosis first; see [`ground-faults.md`](ground-faults.md)
- **Temperature gauge wrong:** identify sender (single-pin) vs. sensor (multi-pin) before purchasing replacement
- **Fuel gauge inaccurate:** sending unit in-tank test; sender replacement requires tank drop or access through cargo floor area
- **Intermittent cluster behavior:** cluster contact inspection and reseating before any part replacement

## Related stock reference
- Electrical system overview: [`../../vehicle/systems/electrical/overview.md`](../../vehicle/systems/electrical/overview.md)
- Ground strap locations and common ground faults: [`ground-faults.md`](ground-faults.md)
- Era-specific wiring context: [`../../vehicle/years/index.md`](../../vehicle/years/index.md)
