# Swap Folder

Legacy-but-current canonical ECU swap execution knowledge during migration.

Use this folder for current aftermarket ECU conversion work on the Jeep XJ: ECU selection, wiring integration, first-start setup, tuning, and related execution detail.

This is no longer the repo's primary identity or the default entrypoint for every technical question. It is the active compatibility branch for ECU swap work while the broader architecture grows around `vehicle/`, `work/`, `diagnostics/`, and `sourcing/`.

## Routing
- For repo-wide routing, start in `AGENTS.md`.
- For general job-oriented work, start in `work/index.md`.
- For current ECU swap execution work, use `swap/index.md`.
- For stock Jeep baseline facts needed to support a swap decision, load the relevant files under `vehicle/`.

## Current branch map
- `index.md` — ECU swap workflow router
- `ecu-selection/` — platform requirements and tradeoffs
- `wiring/` — wiring strategy, grounds, harness, connectors
- `tuning/` — first start, calibration, and tuning workflow

## Important rule
`swap/` is for ECU swap procedures, choices, and implementation details.
Stock Jeep XJ facts belong in `vehicle/`.
Broader non-ECU work belongs under `work/`, `diagnostics/`, or `sourcing/` as appropriate.
