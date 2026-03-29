# Body Electrical Diagnostics Index

## Purpose
Route XJ body wiring, switches, accessories, and cabin-electrical fault isolation.

## Scope
Body wiring, switches, accessories, and cabin-electrical fault isolation.

## What belongs here
- symptom-based leaves for this system or symptom family
- component-specific subfolders when one problem area grows into multiple test paths
- verification logic and follow-up checks after a likely fault is identified
- local compatibility notes only when year, transmission, ABS, or configuration changes diagnosis materially

## What does not belong here
- full replacement or upgrade procedures
- stock-only reference material with no symptom context
- donor or buying guidance as the primary topic
- unrelated system diagnostics

## Child branches

### Live
- [`ground-faults.md`](ground-faults.md) — XJ ground strap locations, common failure points, symptoms of bad grounds
- [`gauge-cluster.md`](gauge-cluster.md) — common gauge failures, temp sender vs. ECU sensor, cluster contacts

### Expected
- `door-lock-failure.md` for lock circuit and actuator faults
- `window-failure.md` for power-window diagnosis
- `lighting-faults.md` for interior or exterior body-electrical lighting issues
