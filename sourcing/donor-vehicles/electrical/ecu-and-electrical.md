# ECU and Electrical Donors — XJ Cherokee

## What this covers
Which donor vehicles are valid sources for ECU, alternator, and instrument cluster on the XJ Cherokee.

---

## ECU (Engine Control Unit)

**Best donor: Same-era XJ Cherokee or ZJ Grand Cherokee**

The XJ uses two distinct ECU eras that are not interchangeable with each other:

| Era | Years | Compatible donors |
|-----|-------|-------------------|
| Renix | 1987–1990 | Same-year XJ, MJ Comanche |
| HO (High Output) | 1991–2001 | Same-era XJ, ZJ Grand Cherokee (1993–1998), YJ Wrangler (1991–1995), TJ Wrangler (1997+) |

**Transmission caveat (Renix era):** An automatic-transmission ECU can be used in a manual-transmission vehicle, but a manual-transmission ECU cannot be used in an automatic-transmission vehicle. Match the ECU to the transmission type within the Renix era.

Do not mix Renix and HO ECUs. The harness connectors, sensor locations, and calibrations differ.

For ECU swap execution details, see: [`../../../work/swaps/ecu/index.md`](../../../work/swaps/ecu/index.md)

---

## Alternator

**Best donors:** Same-year XJ Cherokee, ZJ Grand Cherokee, MJ Comanche (1987–1990 era)

- MJ Comanche alternators are confirmed cross-compatible with XJ for the 1987–1990 era
- ZJ and same-era XJ are interchangeable for 1991+ HO alternators

For high-output alternator donor details (136A from ZJ or Dodge truck), see: [`../../interchange/electrical/junkyard-upgrades.md`](../../interchange/electrical/junkyard-upgrades.md)

Remanufactured alternator quality is inconsistent. A used OEM Denso unit pulled from a same-era donor is often more reliable than a shelf reman.

---

## Instrument cluster

**Match year range only — do not cross generation boundaries**

XJ instrument clusters are generation-specific. The gauge calibrations and speedometer drive differ between generations:

| Generation | Years | Notes |
|-----------|-------|-------|
| First gen | 1984–1990 | Mechanical speedometer (cable-driven) |
| Second gen | 1991–1996 | Electronic speedometer; full-gauge vs. idiot-light versions |
| Third gen | 1997–2001 | Electronic; revised gauge layout |

A cluster from the same generation will swap in and calibrate correctly. Crossing a generation boundary results in incorrect gauge readings. The odometer reading is specific to the cluster PCB and will reflect the donor vehicle's mileage after a swap.

For upgrading from idiot-light to full-gauge cluster within the same generation, see: [`../../interchange/electrical/junkyard-upgrades.md`](../../interchange/electrical/junkyard-upgrades.md)

---

## Boundary links
- Charging and starting system: [`../../../vehicle/systems/charging-starting/overview.md`](../../../vehicle/systems/charging-starting/overview.md)
- Electrical system overview: [`../../../vehicle/systems/electrical/overview.md`](../../../vehicle/systems/electrical/overview.md)
- Instrument cluster details: [`../../../vehicle/systems/electrical/instrument-cluster.md`](../../../vehicle/systems/electrical/instrument-cluster.md)
- ECU swap execution: [`../../../work/swaps/ecu/index.md`](../../../work/swaps/ecu/index.md)
