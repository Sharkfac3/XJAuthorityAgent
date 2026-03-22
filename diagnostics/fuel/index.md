# Fuel Diagnostics Index

## Purpose
Route XJ fuel-delivery symptom trees and test-path troubleshooting.

## Scope
Fuel-delivery symptom trees and test-path troubleshooting.

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
- `no-prime.md` for pump-command and prime-path diagnosis
- `low-fuel-pressure.md` for supply, regulator, or restriction faults
- `rich-or-lean-running.md` for mixture-related fuel-side isolation
