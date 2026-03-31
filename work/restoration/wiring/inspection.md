# Wiring Harness Inspection

## Purpose
Identify degraded or damaged wiring on high-mileage XJs before it causes electrical gremlins, hard starts, or fire risk. Run an inspection before any major electrical repair or ECU swap.

---

## What to look for

### Brittle and cracked insulation
Factory insulation on 1984–2001 XJs is 25–40 years old. Heat cycling causes the outer jacket to harden and crack. Check the engine bay harness first — loom sections running near the exhaust manifold deteriorate fastest. Brittle insulation may still conduct normally but will fail under flex or vibration.

### Rodent damage
Wiring harnesses are a known nesting material target. Look for:
- Chewed-through insulation exposing bare copper
- Nesting material (foam, leaves, hair) packed around harness bundles
- Clusters of damage concentrated in one area (rodents work in one spot)

Rodent damage is common in the engine bay, behind the dashboard, and along the floor harness under the carpet.

### Splice corrosion
Previous repair splices using crimp connectors, scotchlok T-taps, or posi-taps are common on high-mileage XJs. Each one is a potential corrosion point. Look for:
- Green or white oxidation on exposed metal inside crimp connectors
- Brittle or delaminated heat shrink over old repairs
- T-tap / scotchlok connectors (common failure source — see `harness-repair.md`)

### Melted insulation near exhaust
The engine bay harness runs close to the exhaust manifold on the passenger side. Heat damage presents as:
- Melted, shrunken, or fused loom sections
- Multiple wires stuck together where insulation has flowed
- Discolored or blackened harness loom

This is a common failure zone, especially on the injector sub-harness and any wiring looped over or near the manifold.

### Chafed ground wires
Ground straps and wires that contact metal edges develop chafe wear — insulation wears through and the wire either shorts to chassis or loses contact with its ring terminal. Common locations:
- Where the harness passes through firewall grommets
- Along the frame rail under the floor
- Anywhere the loom contacts a sharp sheet-metal edge without a grommet

### Connector corrosion
Inspect the face of each connector for:
- Green or white oxidation on pins
- Corroded or pushed-back terminal pins
- Broken or missing secondary locks
- Cracked or split connector housings

The firewall multi-pin connectors and the injector sub-harness connectors are the highest-priority inspection points. See `firewall-connector.md` and `connector-rehab.md`.

---

## Where the XJ harness is most vulnerable

### Firewall pass-throughs
The rubber grommets where harness bundles enter the cab dry out and crack with age. A cracked grommet lets water track down the wires into the firewall connector cavity. Also, routing wire additions through the firewall without proper grommets is common on modified XJs — check for bare wires contacting sheet-metal edges at firewall holes.

### Engine bay near the exhaust manifold
The injector sub-harness and the main engine harness route along the passenger-side of the engine bay, close to the exhaust manifold. This is the hottest sustained-heat zone in the engine bay. Inspect carefully for melted loom, fused wires, and insulation that crumbles when flexed.

### Floor harness under carpet near drain areas
Water accumulates under the XJ carpet from:
- Missing or clogged floorpan drain plugs
- Failed A/C condensate drain (drain tube exits under the carpet behind the dash)
- Leaking door or window seals

The floor harness runs along the transmission tunnel and along the sill plates under the carpet. Prolonged moisture exposure corrodes the wire insulation and connector pins from the outside in. Pull back carpet near the drain plugs (driver and passenger footwell corners) and inspect the floor harness condition.

### Dipstick area / engine block ground cluster
Multiple chassis grounds terminate at the engine block near the dipstick tube stud. Corrosion at this location causes compounding electrical problems. See `ground-straps.md`.

### Behind the dashboard (instrument cluster area)
Dash wiring is rarely inspected but rodent damage and splice corrosion collect here. The under-dash fuse block connections (Era 1 and Era 2) are also a corrosion point.

---

## Tools for inspection

| Tool | Use |
|------|-----|
| Inspection light or headlamp | Illuminate behind dash, under carpet, inside engine bay |
| Dental pick or scribe | Flex-test brittle insulation, probe connector cavities |
| Multimeter (continuity and resistance) | Check for open circuits, high-resistance paths in ground circuits |
| Terminal release tool set (Metri-Pack, EV1) | Unplug connectors without breaking tabs |
| Compressed air or soft brush | Clear debris from connector faces before inspection |
| Mirror on a stick | Inspect hard-to-reach areas near the firewall |

---

## Cross-references
- Ground strap locations and replacement: `ground-straps.md`
- Connector cleaning and re-pin: `connector-rehab.md`
- Firewall multi-pin connector: `firewall-connector.md`
- Splice and harness repair: `harness-repair.md`
- Era-specific wiring notes: `vehicle/era1/wiring.md`, `vehicle/era2/wiring.md`, `vehicle/era3/wiring.md`
