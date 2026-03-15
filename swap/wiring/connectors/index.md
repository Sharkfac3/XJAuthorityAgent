# Connector Index

Canonical landing page for connector-specific wiring notes.

## Family folders
- `swap/wiring/connectors/ecu-body/` — ECU/PCM body connectors by controller family
- `swap/wiring/connectors/ev1-bosch/` — EV1 injector connectors
- `swap/wiring/connectors/ev6-uscar/` — EV6 / USCAR injector connectors
- `swap/wiring/connectors/metri-pack/` — Delphi/Packard Metri-Pack connector variants
- `swap/wiring/connectors/packard-56/` — Packard 56 connector variants
- `swap/wiring/connectors/renix-native/` — Renix-era OEM connector shapes and equivalents

## Load strategy
- Start with the family `overview.md` when it exists
- Then load the specific connector leaf file for the circuit in question
- Use era wiring files under `vehicle/era1/`, `vehicle/era2/`, or `vehicle/era3/` for stock harness context

## Scope rule
This folder is for connector family identification, pin count, physical compatibility, and replacement guidance.
Stock harness architecture belongs in era wiring files.
