# Charging And Starting Diagnostics Index

## Purpose
Route XJ battery, charging, and starting fault isolation.

## Scope
Battery, charging, and starting fault isolation.

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

## Expected child branches
- `no-crank.md` for dead-start-command or starter-engagement faults
- `slow-crank.md` for weak-cranking and voltage-drop diagnosis
- `low-charging-voltage.md` for alternator, regulator, or wiring faults
