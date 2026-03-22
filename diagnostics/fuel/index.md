# Fuel Diagnostics Index

## Purpose
Route XJ fuel-delivery symptom trees and test-path troubleshooting.

## Scope
Use this branch when the main question is whether fuel delivery is missing, weak, or otherwise contributing to a no-start or poor-running complaint.

## What belongs here
- symptom-based fuel leaves
- relay, power, pressure, and delivery fault isolation
- verification logic after a likely fuel-side cause is found
- local compatibility notes only when the fuel diagnostic path truly changes

## What does not belong here
- full replacement procedures
- stock-only reference with no symptom context
- donor or part-brand recommendations as the primary topic
- unrelated ignition or mechanical diagnosis

## Current child leaves
- [`no-prime.md`](no-prime.md) — starter leaf for pump-command and prime-path faults

## Next likely child leaves
- `low-fuel-pressure.md`
- `rich-or-lean-running.md`
- `fuel-leak-or-odor.md`

## Supporting canon
- Fuel maintenance branch: [`work/maintenance/fuel/index.md`](../../work/maintenance/fuel/index.md)
- Fuel repair branch: [`work/repairs/fuel/index.md`](../../work/repairs/fuel/index.md)
- Engine diagnostics branch: [`diagnostics/engine/index.md`](../engine/index.md)
