# Instrument Cluster

## Overview

All XJs in scope (1988–2001) use **analog gauges** throughout the production run. There was no digital instrument cluster option on the XJ. The cluster contains a printed circuit board (PCB) behind the gauge faces that routes signals and power to each gauge and indicator light. Both the individual gauges and the PCB itself are common failure points on high-mileage vehicles.

For fault isolation on gauge-related symptoms, see [`../../../diagnostics/body-electrical/gauge-cluster.md`](../../../diagnostics/body-electrical/gauge-cluster.md).

---

## Speedometer: mechanical cable vs. electronic VSS

The speedometer drive transitioned from mechanical cable to fully electronic VSS partway through the XJ production run.

| Years | Speedometer drive | Notes |
|-------|------------------|-------|
| 1987–1990 | Mechanical cable only | No VSS output; cable runs from transfer case output |
| 1991 | Hybrid — mechanical cable + VSS | Cable still drives the speedometer needle; separate 2-wire reed-switch VSS outputs to the ECU. 1991 is sometimes called the "orphan year" because of this unique dual-output configuration. |
| 1992–1993 | Fully electronic VSS (2-wire, hall-effect) | No mechanical cable; VSS signal drives both the speedometer and the ECU |
| 1993–2001 | Fully electronic VSS (3-wire, dead-end) | Function same as 1992; different connector type from ~1993 onward |

**Parts and repair note:** The 1991 hybrid configuration means the speedometer cable and the VSS are separate components — both can fail independently. On 1992+ fully-electronic XJs, a dead speedometer with no other symptoms points to the VSS sensor, the cluster PCB, or the gauge itself. On 1987–1990 XJs, a bouncy or dead speedometer is almost always the cable (replacement cable quality is notoriously poor; conversion kits to the 1991–1996 electronic system are available and solve the bounce problem permanently).

---

## Temperature gauge

**The temperature gauge sender is in a different location depending on year.** This causes confusion when swapping heads, diagnosing gauge faults, or interpreting gauge behavior after engine work.

| Years | Gauge sender location |
|-------|----------------------|
| 1987–1990 (Renix) | Rear of cylinder head, driver's side |
| 1991–1995 (SBEC) | Two devices: PCM coolant temperature sensor at thermostat housing; separate gauge sender at rear of head |
| 1997–2001 (JTEC) | Single coolant sensor at thermostat housing drives both PCM and gauge |

See `vehicle/era2/ho-engine.md` — temperature sender location table — for the full breakdown including the 1996 mid-year transition period.

**Common diagnostic confusion:** On 1997+ XJs, the PCM uses the single sensor to drive the dash gauge through the cluster. A PCM fault, wiring fault, or failed sensor will affect both the temperature gauge reading and the PCM's coolant temperature data simultaneously. Do not assume the gauge has failed independently before checking the sensor signal.

---

## Fuel gauge

**Failure mode: float-arm sender in the fuel tank.** The fuel gauge sending unit is a variable-resistance float arm inside the tank. On high-mileage XJs, the sender fails in several patterns:

- **Float arm stuck:** Gauge reads constant (often full or a fixed incorrect level); wiggling the sender wire or driving over bumps may temporarily change the reading
- **Sender wiper worn:** Gauge reads erratically or pegs to full or empty
- **Resistor wire corroded or broken:** Gauge reads empty regardless of actual fuel level

The sender is accessed through an access panel under the rear cargo area floor. The tank does not need to be dropped to replace the sender on most XJ configurations.

**Wiring note:** The fuel gauge sender circuit is low-current and susceptible to ground path issues. A poor body or chassis ground can cause the gauge to read incorrectly even with a functional sender.

---

## Printed circuit board (PCB)

The instrument cluster uses a **printed circuit board** behind the gauge faces to route power, grounds, and signals. The PCB is a flat laminated board with conductive traces — it does not use traditional wiring harness connections internally.

**Failure mode: trace cracking.** With age and thermal cycling, the conductive traces on the PCB crack. Individual cracks cause specific gauges or indicator lights to go dead or become intermittent, depending on which trace is affected.

**Symptoms:**
- One or more gauges dead with no corresponding sensor or wiring fault
- Indicator lamps (oil pressure, battery, seatbelt) intermittently dark
- Gauge comes back to life temporarily after pressing on the cluster face or after a cold start that warms the cluster

**Diagnosis:** Remove the cluster and inspect the PCB under good lighting. Cracks often appear as dark lines or separations in the copper traces, sometimes visible to the naked eye. Conductive silver epoxy pen repairs are a documented community repair technique and are effective on clean, accessible cracks.

**Full cluster replacement** from the salvage yard is the alternative, but used clusters have often accumulated the same trace-cracking failures. Inspect the PCB of any donor cluster before installing it.

---

## See also

- System overview: [`overview.md`](overview.md)
- Gauge cluster fault isolation: [`../../../diagnostics/body-electrical/gauge-cluster.md`](../../../diagnostics/body-electrical/gauge-cluster.md)
- Temperature sender location detail: `vehicle/era2/ho-engine.md` — Temperature sender location section
- Body electrical index: [`../../../diagnostics/body-electrical/index.md`](../../../diagnostics/body-electrical/index.md)

## Sources
Speedometer transition years: BoxyJeep electronic speedometer conversion article (1987–1990 cable); JeepForum "Mechanical to Electric Speedometer" thread; JeepForum "Electronic speedometer in a 91?" thread; NAXJA "Electronic speed sensor (VSS) Specs." thread. Fuel gauge sender: JeepForum and NAXJA community threads. PCB trace cracking: JeepForum and NAXJA cluster repair threads. Temperature sender location: vehicle/era2/ho-engine.md (community-verified via NAXJA, JeepForum, CherokeeTalk).
