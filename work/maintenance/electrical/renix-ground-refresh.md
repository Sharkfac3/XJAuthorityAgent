# Renix Ground Refresh

## Purpose
Restore all factory ground connections on Renix-era (1987–1990) XJ and MJ vehicles to reliable working condition.

## Why this matters
The Renix grounding system is under-engineered. Multiple critical engine and transmission electronics share a small number of ground points. Corroded, loose, or poorly crimped grounds cause driveability problems, failed emissions, and unnecessary part replacement. Refreshing grounds should be the first step before any Renix electrical diagnosis.

## General principles
- Every contact surface must be scraped to bare, shiny metal — no paint, oil, grease, or corrosion.
- Apply OxGard (antioxidant compound, available at Lowe's) to every cleaned surface before reassembly.
- Inspect all wire terminals for crimps over insulation instead of bare wire. Re-crimp as a preventive measure.
- Sand and polish both sides of every terminal until clean and shiny.

---

## Dipstick tube stud ground

This is the primary engine/transmission electronics ground. All of the following share this single stud:

- Distributor sync sensor
- TCU main ground
- TCU shift-point logic
- Ignition Control Module (ICM)
- Fuel injectors
- ECU main ground (which feeds grounds to: oxygen sensor, knock sensor, cruise control, transmission sync signal)

Typically four wires total.

### Procedure
1. Remove the nut holding wire terminals to the stud.
2. Verify the stud is tight in the block. If it turns, hold with a 7/32″ six-point socket or wrench.
3. Scrape all paint from the stud mounting surface where the wires attach.
4. Inspect each wire terminal:
   - Confirm crimp is over bare wire, not insulation.
   - Re-crimp if suspect.
   - Sand and polish both sides until clean and shiny.
5. Apply OxGard to stud surface and all terminals.
6. Reinstall all wires and tighten nut securely.

**Worst case:** If terminals are beyond recovery, cut wires, remove stud and nut, and install new terminal eyelets.

---

## Battery negative cable ground

Located on the engine block just forward of the dipstick stud.

### Procedure
1. Remove the bolt.
2. Scrape the block mounting surface to bare metal.
3. Clean and polish the cable terminal.
4. Apply OxGard.
5. Reattach and torque securely.

---

## Engine-to-chassis ground strap

Braided cable running from the rear of the cylinder head to the driver's side firewall. This cable is undersized for its intended use and prone to corrosion at both ends.

### Firewall end
1. Remove cable end (15mm wrench or socket).
2. Scrape firewall paint to bare metal at mounting area.
3. Clean and polish wire terminal.
4. Apply OxGard.
5. Reattach securely.

### Cylinder head end
1. Remove cable end (3/4″ socket).
2. Clean all oil, paint, and crud from the stud.
3. Clean and polish wire terminal.
4. Apply OxGard liberally.
5. Reattach securely.

---

## Comanche (MJ) fuel pump ground

Specific to the MJ Comanche.

### Access
Remove the driver's side tail lamp assembly to access the fuel pump ground. Remove the screw holding the black ground wire.

### Procedure
1. Scrape paint from the body at the grounding point.
2. Clean corrosion from the wire terminal.
3. Add a 10-gauge wire with an eyelet on each end, running from the grounding point to a bolt on the frame (provides a more reliable secondary path).
4. Scrape all mounting points to bare metal.
5. Apply OxGard to all connections.

---

## Verification

After completing all refresh work, measure ground resistance at the TPS ground wire as a representative check. One documented result showed TPS ground resistance drop from 1.7 Ω to 0.8 Ω after refresh and upgrade — confirming a much more direct ground path for sensors.

---

## See also
- `vehicle/era1/wiring.md` — Era 1 wiring overview and ground locations
- `work/upgrades/electrical/renix-ground-upgrades.md` — supplemental ground cables beyond factory
- `work/swaps/ecu/wiring/grounds.md` — grounds in the context of ECU swaps
- `diagnostics/charging-and-starting/` — if ground issues present as no-crank or charging faults

## Source
Cruiser54 — cruiser54.com, "Renix Ground Refreshing"
