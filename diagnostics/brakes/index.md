# Brakes Diagnostics Index

## Purpose
Route XJ brake feel, pull, vibration, and braking-performance diagnosis.

## Scope
Brake feel, pull, vibration, and braking-performance diagnosis.

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
- [`pedal-feel.md`](pedal-feel.md) — spongy, sinking, hard, and fading pedal; master cylinder vs. air vs. booster
- [`rear-drum-issues.md`](rear-drum-issues.md) — seized adjusters, wheel cylinder leaks, contaminated shoes

### Expected
- `soft-pedal.md` for hydraulic feel and air-in-system paths
- `pull-under-braking.md` for side-to-side brake imbalance
- `brake-vibration.md` for pulsation, shimmy, or vibration during braking
