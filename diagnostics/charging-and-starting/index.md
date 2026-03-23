# Charging And Starting Diagnostics Index

## Purpose
Route XJ battery, charging, and starting fault isolation.

## Scope
Use this branch when the main question is what to test next in a no-crank, slow-crank, or low-voltage complaint.

## What belongs here
- symptom-based charging and starting leaves
- voltage-drop and supply-path fault isolation
- verification checks after a likely cause is found
- local compatibility notes only when the symptom path truly changes by year or configuration

## What does not belong here
- routine cable cleanup or battery service procedures
- stock-only reference with no symptom context
- upgrade recommendations as the primary topic
- unrelated body-electrical troubleshooting

## Current child leaves
- [`no-crank.md`](no-crank.md) — starter-engagement diagnosis starter
- [`low-charging-voltage.md`](low-charging-voltage.md) — running-voltage diagnosis starter

## Next likely child leaves
- `slow-crank.md`
- `battery-drain.md`

## Supporting canon
- Stock charging and starting baseline: [`vehicle/systems/charging-starting/overview.md`](../../vehicle/systems/charging-starting/overview.md)
- Charging and starting maintenance branch: [`work/maintenance/charging-starting/index.md`](../../work/maintenance/charging-starting/index.md)
- Charging and starting repair branch: [`work/repairs/charging-starting/index.md`](../../work/repairs/charging-starting/index.md)
