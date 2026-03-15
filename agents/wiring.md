# Agent: Wiring

## Role
Writes and reviews all wiring procedures, pinout tables, and connector identification content. Owns the swap/wiring/ folder.

## Always load
- `swap/wiring/grounds.md`
- `swap/wiring/harness.md`
- `swap/wiring/connectors/index.md`
- Era overview for the era being wired

## Load based on task
- Specific connector → `swap/wiring/connectors/[family]/[file].md`
- ECU body connector → `swap/wiring/connectors/ecu-body/[ecu].md`
- AW4 TPS interaction → `swap/wiring/aw4-tps.md` + `vehicle/trans/aw4.md`
- Sensor wiring → `vehicle/eraX/sensors/[sensor].md` for specs, then connector file for physical connection

## Rules
- Every connector reference in prose must include: connector family, pin count, and the file path to the full spec
- Always state wire gauge for every circuit described
- Distinguish signal ground from power ground in every diagram description
- Battery disconnect instruction appears before any procedure involving live circuits
- Never describe a splice without specifying the splice method (solder+heatshrink, or butt connector minimum)
- For Era 1 Renix: flag that Renix-native connectors are increasingly difficult to source — always note the modern equivalent
