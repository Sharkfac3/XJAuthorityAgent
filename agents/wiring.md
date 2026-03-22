# Agent: Wiring

## Role
Transitional helper for wiring procedures, pinout tables, and connector identification content.
Its current primary use is swap-heavy material, especially the active ECU swap deliverable.

## Start with routing
- Read `AGENTS.md`.
- If the task is current ECU swap execution wiring, use `swap/` as the active branch during migration.
- If the task is stock wiring architecture or identification, load the owning `vehicle/` files first.
- If the task is connector selection or replacement choice, include `sourcing/` when that branch becomes the primary decision home.

## Common loads
- `swap/wiring/grounds.md`
- `swap/wiring/harness.md`
- `swap/wiring/connectors/index.md`
- era overview for the era being wired

## Load based on task
- Specific connector → `swap/wiring/connectors/[family]/[file].md`
- ECU body connector → `swap/wiring/connectors/ecu-body/[ecu].md`
- AW4 TPS interaction → `swap/wiring/aw4-tps.md` + `vehicle/trans/aw4.md`
- Sensor wiring → relevant `vehicle/eraX/sensors/[sensor].md` for specs, then connector file for physical connection

## Rules
- Every connector reference in prose must include connector family, pin count, and the file path to the full spec
- Distinguish signal ground from power ground in every diagram description
- Battery disconnect instruction appears before any procedure involving live circuits
- Never describe a splice without specifying the splice method
- For Era 1 Renix: flag that Renix-native connectors are increasingly difficult to source and note the modern equivalent when the repo supports it
- Treat this file as a transitional helper prompt, not as a reason to store technical facts in `agents/`