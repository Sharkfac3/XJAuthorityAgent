# Cooling System Overview

**Branch router:** [index.md](index.md)

## Purpose
Stock 4.0L cooling system baseline — architecture, component specs, and normal operating parameters.

## Scope
Factory cooling configuration for the 4.0L inline-six in the 1988–2001 Jeep Cherokee XJ. This covers what the system looks like from the factory, not service procedures or diagnostics.

---

## System type

Pressurized closed-loop with overflow reservoir. The system is sealed under pressure (cap-rated at ~16 PSI on most years) to raise the boiling point of coolant above 212°F. An overflow bottle captures coolant expelled when hot and draws it back as the system cools.

---

## Major components

### Radiator
- **Earlier years (pre-1995):** Crossflow copper/brass core with plastic end tanks
- **Later years (1995+):** Crossflow aluminum core with plastic end tanks
- Automatic-equipped XJs have a transmission fluid cooler integrated into one end tank

### Fan
- **Mechanical clutch fan** (engine-driven via fan clutch on water pump nose): primary cooling at idle and low speed
- **Electric auxiliary fan**: equipped on A/C models; controlled by the A/C system to pull additional air through condenser and radiator when A/C compressor is engaged. Not a replacement for the mechanical fan — both are needed on A/C vehicles.
- Fan shroud is required for both fans to work efficiently; missing or cracked shrouds impair low-speed cooling

### Water pump
- Belt-driven off the serpentine belt
- Impeller-style — cast iron or stamped impeller depending on year
- Failure is condition-based; see [`water-pump.md`](water-pump.md) for failure modes and inspection

### Thermostat
- **Stock rating: 195°F**
- A 180°F thermostat is a common community swap; it lowers the minimum operating temp but does not address an overheating condition — the thermostat sets the lower operating limit, not the upper limit
- Never run without a thermostat: the coolant flows too fast to transfer heat effectively, causing erratic temp readings and poor cabin heat
- Housing: bolts to front of cylinder head; seals with a gasket or O-ring depending on year

### Overflow reservoir
- Plastic bottle mounted near radiator
- Must hold a small coolant volume; a cracked or missing bottle will cause the system to vent coolant instead of recovering it

---

## Coolant capacity

Approximately **11–12 quarts** for the 4.0L. Exact capacity varies slightly by configuration (automatic vs. manual, with or without heater core volume variation). When refilling, fill to the cold fill line on the overflow bottle after the system is bled.

Coolant type:
- **1988–2000:** IAT (Inorganic Acid Technology) green antifreeze — 50/50 mix with distilled water
- **2001:** HOAT (Hybrid Organic Acid Technology) — verify before mixing; IAT and HOAT are not compatible without a full flush

---

## Normal operating temperature

| Condition | Expected gauge reading |
|-----------|----------------------|
| Cold start | Low; rises to normal within ~5 minutes of driving |
| Steady highway cruise | Near gauge center (~210–215°F) |
| Idle in traffic, A/C on, hot day | May approach upper third of gauge; normal unless gauge climbs continuously |
| Concern threshold | Gauge approaching red or climbing without stabilizing |

The XJ temperature gauge is a damped indicator, not a precision instrument. It will not respond instantly to rapid temperature spikes. Trust a rising gauge; never ignore it.

---

## Configuration and year splits

Before cooling work or parts ordering, confirm:
1. Engine family (4.0L vs. 2.5L)
2. Transmission (auto = trans cooler in radiator)
3. A/C presence (determines auxiliary fan configuration)
4. Year (affects radiator core material, thermostat housing design, coolant type)

See [`year-changes.md`](year-changes.md) for the full split-point reference.

---

## Known failure modes

The 4.0L has two well-documented thermal failure modes that go beyond routine maintenance:

- **Head cracking** — the HO-era 0331 casting (2000–mid-2001) is particularly prone to cracking between cylinders 3–4. Caused by chronic overheating or coolant neglect. See [`head-cracking.md`](head-cracking.md).
- **Exhaust manifold cracking** — thermal cycling cracks the iron manifold at the collector or between ports, all years. Not a cooling system failure, but often noticed during cooling-related work. See [`vehicle/systems/engine/exhaust-manifold.md`](../engine/exhaust-manifold.md).

---

## Sources
Community-verified via NAXJA, CherokeeForum, JeepForum, BobIsTheOilGuy forums; cross-referenced against Allpar Jeep 4.0 documentation and XJ service manual specifications.
