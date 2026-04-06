# Cooling System Index

## Purpose
Route stock XJ and MJ cooling-system content.

## Use this branch when
The main question is about factory cooling architecture, component specifications, failure modes of specific cooling components, or overheating diagnosis.

## First-hop loading path

- Stock cooling baseline and system specs → [overview.md](overview.md)
- Year and configuration split points → [year-changes.md](year-changes.md)

## Component and failure leaves

- Head cracking — 4.0L casting vulnerability → [head-cracking.md](head-cracking.md)
- Water pump — inspection and failure modes → [water-pump.md](water-pump.md)
- Overheating diagnosis sequence → [overheating-diagnosis.md](overheating-diagnosis.md)

## What belongs here
- stock cooling-system architecture and specs
- factory fan, radiator, thermostat, and water-pump baselines
- known failure modes tied to specific cooling components
- year or configuration splits that change cooling answers
- cross-links to maintenance, diagnostics, and sourcing branches

## What does not belong here
- flush or replacement procedures → `work/maintenance/cooling/`
- exhaust manifold cracking → `vehicle/systems/engine/exhaust-manifold.md`
- symptom-first overheating diagnosis → `diagnostics/cooling/`
- part-brand recommendations → `sourcing/`

## Boundary links

- Vehicle systems hub → [`../index.md`](../index.md)
- Cooling diagnostics → [`../../../diagnostics/cooling/index.md`](../../../diagnostics/cooling/index.md)
- Cooling maintenance work → [`../../../work/maintenance/cooling/index.md`](../../../work/maintenance/cooling/index.md)
- Cooling sourcing → [`../../../sourcing/oem-vs-aftermarket/cooling/index.md`](../../../sourcing/oem-vs-aftermarket/cooling/index.md)
