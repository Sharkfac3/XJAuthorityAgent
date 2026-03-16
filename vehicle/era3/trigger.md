# Era 3: Trigger System

## Crank position sensor (CPS)
- Type: Variable Reluctance (VR) — passive magnetic, sine wave output
- Location: Driver's side bellhousing
- Reads: Toothed ring on flywheel (manual) or flexplate (automatic)
- Pattern: **Jeep 18-2-2-2** — confirmed same as Era 2 across all sub-years (1996–2001)
- Connector: Flat-pin Packard — see `swap/wiring/connectors/packard-56/cps.md`

## Cam position sensor — 1996–1999 (distributor)
- Type: Hall effect — active, square wave (0V / 5V)
- Location: Inside the distributor body
- Purpose: Required — 18-2-2-2 is symmetrical, cam sync needed for phase detection
- See: `swap/wiring/connectors/packard-56/cam.md`

## Cam position sensor — 2000–2001 (coil rail)
- Type: Hall effect
- Location: Front of engine at camshaft gear — no longer inside a distributor
- Purpose: Same as above — required for sequential injection and ignition timing
- Connector: Verify against FSM for 2000–2001 specific connector

## Open source ECU configuration
- rusEFI trigger name: **Jeep 18-2-2-2** — same decoder as Era 2; applies to all sub-years including 2000–2001
- Speeduino trigger name: **Jeep 2000** — natively supported; see https://wiki.speeduino.com/en/decoders/Jeep_2000
- Input type: VR for crank, Hall for cam
- Cam sync: Required

## Swap notes
- 1996–1999 swap follows identical trigger strategy to Era 2 — distributor cam sensor stays in place
- 2000–2001 coil rail: cam sensor moves to front of engine — wire to ECU cam input from new location
- 2000–2001 coil rail: open source ECU must support wasted spark (3 paired outputs for 6 cylinders), or retrofit a distributor from a 1991–1999 donor
- Wasted spark is simpler and preferred — 3 ignition outputs fire cylinders in pairs (1&6, 2&5, 3&4)
