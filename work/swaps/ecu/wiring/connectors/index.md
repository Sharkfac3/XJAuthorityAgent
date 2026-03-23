# Connector Index

## Purpose
Route ECU-swap connector-family identification and replacement guidance.

## Family folders
- `ecu-body/` — ECU/PCM body connectors by controller family
- `ev1-bosch/` — EV1 injector connectors
- `ev6-uscar/` — EV6 / USCAR injector connectors
- `metri-pack/` — Delphi/Packard Metri-Pack connector variants
- `packard-56/` — Packard 56 connector variants
- `renix-native/` — Renix-era OEM connector shapes and equivalents

## Load strategy
- Start with the family `overview.md` when it exists.
- Then load the specific connector leaf file for the circuit in question.
- Use era wiring files under `vehicle/era1/`, `vehicle/era2/`, or `vehicle/era3/` for stock harness context.

## Scope rule
This folder is for connector family identification, pin count, physical compatibility, and replacement guidance.
Stock harness architecture belongs in era wiring files.
