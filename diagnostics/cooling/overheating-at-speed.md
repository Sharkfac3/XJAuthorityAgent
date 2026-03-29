# Overheating at Highway Speed

## Purpose
Provide a fault-isolation path for XJs that run hot or overheat at highway speed, particularly when idle or low-speed temperatures are normal.

## Symptom definition
Use this leaf when:
- The temperature problem is strongest at sustained highway speeds
- The vehicle is normal or acceptable at idle or in slow traffic
- The problem worsens with load (hills, towing, headwinds)

This is the **inverse pattern** of idle-only overheating. If the vehicle overheats equally at all speeds, start with [`overheating-at-idle.md`](overheating-at-idle.md) first and escalate here if airflow and fan checks are clean.

## Do not use this leaf when
- The vehicle overheats at idle but cools down at speed
- The main symptom is coolant loss with no temperature problem → [`coolant-loss.md`](coolant-loss.md)
- White exhaust is the primary complaint → [`white-exhaust.md`](white-exhaust.md)

## Why this symptom pattern matters

At highway speed, ram air provides strong forced airflow through the radiator — the mechanical fan is nearly irrelevant at 60+ MPH. If the vehicle overheats under these conditions, the cause is almost always a **restriction or capacity problem**, not an airflow problem:

- The cooling circuit cannot move or reject heat fast enough under load
- Something is limiting coolant flow, reducing the coolant-to-air heat transfer surface, or introducing additional heat the system cannot handle

## First checks

1. Confirm coolant level is full and the overflow bottle is at the correct level cold
2. Confirm the radiator cap seals properly and holds rated pressure (test with a cooling system pressure tester)
3. Confirm the thermostat is opening fully — a partially opening or high-restriction thermostat reduces flow under high load

## Common branches

### Radiator restriction branch
At highway speed under load, a partially clogged radiator core becomes the limiting factor.
- Inspect the radiator face for packed debris, bent fins, bug accumulation, or physical damage
- Check for cold spots across the radiator face with an infrared thermometer after warmup — cold zones = blocked tubes
- A badly scaled or sediment-filled core requires a professional flush or replacement
- On high-mileage XJs: a radiator that looks clean externally may be internally restricted with decades of scale

### Coolant flow restriction branch
If the radiator checks out, look for restrictions in the circuit:
- **Collapsed radiator hose:** the internal liner can delaminate and partially block flow under suction; inspect upper and lower hoses for softness, deformation at the ends, or a hose that collapses when pinched
- **Thermostat partially open:** a thermostat that opens but does not open fully creates a flow restriction under high load; replace with a known-good unit
- **Water pump degradation:** an impeller that has lost material due to erosion will move less coolant; this is a teardown finding

### Head gasket or internal combustion leak branch
Exhaust gas entering the cooling circuit from a failed head gasket or cracked head will:
- Pressurize the system beyond cap rating, causing coolant loss
- Displace coolant with compressible gas, reducing effective coolant volume
- Cause temperature spikes under load when combustion pressure is highest

This branch becomes more likely when:
- A radiator flush and component inspection have not resolved the problem
- The vehicle is a 2000–2001 XJ with an original 0331 head
- Coolant loss accompanies the overheating (see [`coolant-loss.md`](coolant-loss.md))

Test: combustion leak test on the coolant reservoir. See [`vehicle/systems/cooling/head-cracking.md`](../../vehicle/systems/cooling/head-cracking.md).

## Split points to confirm
- If the vehicle is a 2000 or 2001 XJ, move the combustion leak test earlier in the sequence
- If the vehicle tows or carries extra load regularly, consider whether the stock cooling system is undersized for the use case — this is a separate conversation from fault isolation

## Exit criteria
Route out of this leaf when you have enough evidence to say the problem is mainly:
- Maintenance-related → [`work/maintenance/cooling/`](../../work/maintenance/cooling/)
- Repair-related → `work/repairs/cooling/`
- Head/gasket failure → [`vehicle/systems/cooling/head-cracking.md`](../../vehicle/systems/cooling/head-cracking.md)
