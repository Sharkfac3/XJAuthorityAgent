# Era 1: Wiring Specifics

## ECU location
Renix ECU is located behind the glovebox. The ICM (Ignition Control Module) is mounted on or near the firewall on the driver's side.

## Firewall connectors
The engine harness passes through a multi-pin firewall connector — a known corrosion point on all XJs but especially Era 1 vehicles. Disassemble, clean, and apply dielectric grease to every pin before the swap.

## Key wiring differences from Era 2/3
- Two ECU boxes (fuel ECU + ICM) — both must be addressed in the swap
- Fuel pump relay supplies injector feed voltage through the ECU board (terminals C11 and D10) — the relay circuit is part of the injector power path, not separate
- No ASD relay — ignition and fuel are on separate power paths
- All sensor connectors are Renix-native proprietary — see `work/swaps/ecu/wiring/connectors/renix-native/`
- CPS shield wire must be grounded separately to the block — do not omit
- B+ latch relay keeps IAC powered at key-off for reset — replicate this behavior if using stock stepper IAC

## Grounds on Era 1
Era 1 grounds are the oldest in scope and the most likely to be compromised. Run new dedicated grounds before attempting diagnosis of any electrical problem.

- Full factory ground refresh procedure: `work/maintenance/electrical/renix-ground-refresh.md`
- Supplemental ground cable upgrades: `work/upgrades/electrical/renix-ground-upgrades.md`
- Grounds in the context of ECU swaps: `work/swaps/ecu/wiring/grounds.md`

## Fuse box
Under-dash fuse block on all Era 1 vehicles. No under-hood PDC.

## Adapter harness notes
When building an adapter harness for Era 1:
- Source the Renix ECU connector body — these are salvage-only at this point
- Confirm pin assignments against the FSM — pin assignments vary between 1988, 1989, and 1990
- The ICM connector must also be addressed — open source ECU coil trigger replaces the ICM's role
- Plan to replace all Renix-native sensor connectors with modern equivalents at swap time — this simplifies the harness significantly
