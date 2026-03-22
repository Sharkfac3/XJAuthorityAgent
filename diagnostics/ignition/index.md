# Ignition Diagnostics Index

## Purpose
Route XJ ignition trigger, spark-delivery, and timing-related fault isolation.

## Scope
Ignition trigger, spark-delivery, and timing-related fault isolation.

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
- `crank-no-start.md` for spark-present-versus-spark-missing routing
- `misfire-under-load.md` for coil, wire, cap, or trigger faults that appear under demand
- `spark-loss.md` for complete or intermittent loss-of-spark diagnosis
