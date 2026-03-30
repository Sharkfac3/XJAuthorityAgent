# Sourcing Index

## Purpose
Route parts-selection, donor, kit, connector, and interchange decision support.

## Use this branch when
The main question is what to buy, what donor to pull from, which option to prefer, or what practical interchange route makes sense.

## First-hop loading path
- Practical fitment and interchange choice → [`interchange/index.md`](interchange/index.md)
- Which donor vehicle or donor family to target → [`donor-vehicles/index.md`](donor-vehicles/index.md)
- OEM vs aftermarket tradeoff → [`oem-vs-aftermarket/index.md`](oem-vs-aftermarket/index.md)
- Connector or pigtail selection → [`connectors/index.md`](connectors/index.md)
- Swap-related kit selection → [`swap-kits/index.md`](swap-kits/index.md)
- Routine wear-item selection → [`wear-items/index.md`](wear-items/index.md)

## Current live sourcing leaves

### Swap kits
- Lift kit types and brand fitment: [`swap-kits/lift-kits.md`](swap-kits/lift-kits.md)
- SYE kit selection for NP231: [`swap-kits/sye-kits.md`](swap-kits/sye-kits.md)
- CAD delete kit for Dana 30: [`swap-kits/cad-delete.md`](swap-kits/cad-delete.md)

### OEM vs. aftermarket
- Radiator (Mishimoto vs. stock vs. cheap eBay): [`oem-vs-aftermarket/cooling/radiator.md`](oem-vs-aftermarket/cooling/radiator.md)
- Engine gaskets (Fel-Pro MLS, Remflex): [`oem-vs-aftermarket/engine/gaskets.md`](oem-vs-aftermarket/engine/gaskets.md)
- Brake pads and rotors: [`oem-vs-aftermarket/brakes/pads-and-rotors.md`](oem-vs-aftermarket/brakes/pads-and-rotors.md)
- Engine sensors (CPS, TPS, O2): [`oem-vs-aftermarket/electrical/sensors.md`](oem-vs-aftermarket/electrical/sensors.md)

### Interchange
- Battery, alternator, and starter: [`interchange/electrical/battery-alternator-starter.md`](interchange/electrical/battery-alternator-starter.md)
- Driveshafts and u-joints (Tom Woods, Dana Spicer): [`interchange/drivetrain/driveshafts-and-ujoints.md`](interchange/drivetrain/driveshafts-and-ujoints.md)
- Junkyard electrical upgrades (high-output alternator, etc.): [`interchange/electrical/junkyard-upgrades.md`](interchange/electrical/junkyard-upgrades.md)
- Junkyard drivetrain upgrades (NV241-OR, hack-n-tap SYE, etc.): [`interchange/drivetrain/junkyard-upgrades.md`](interchange/drivetrain/junkyard-upgrades.md)

### Donor vehicles
- ECU, alternator, and instrument cluster donors: [`donor-vehicles/electrical/ecu-and-electrical.md`](donor-vehicles/electrical/ecu-and-electrical.md)
- AW4, AX-15, and NP231 donors: [`donor-vehicles/drivetrain/transmissions.md`](donor-vehicles/drivetrain/transmissions.md)

### Connectors
- Connector repair strategy: [`connectors/pigtail-vs-rehousing.md`](connectors/pigtail-vs-rehousing.md)

## What belongs here
- donor comparisons
- practical interchange guidance
- OEM vs aftermarket tradeoffs
- kit, connector, and wear-item selection guidance

## What does not belong here
- full installation procedures
- symptom-first diagnostics trees
- pure stock platform reference with no decision context
- agent behavior or repo governance

## Boundary links
- Stock fit and baseline facts: [`../vehicle/index.md`](../vehicle/index.md)
- Job execution after the part is chosen: [`../work/index.md`](../work/index.md)
- Diagnosis before parts selection: [`../diagnostics/index.md`](../diagnostics/index.md)
- ECU conversion workflow: [`../work/swaps/ecu/index.md`](../work/swaps/ecu/index.md)
