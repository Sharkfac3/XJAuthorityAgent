# Era 2: Trigger System

## Crank position sensor (CPS)
- Type: Variable Reluctance (VR) — passive magnetic, sine wave output
- Location: Driver's side bellhousing
- Reads: Toothed ring on flywheel (manual) or flexplate (automatic)
- Pattern: **Jeep 18-2-2-2** — 18 base teeth with three evenly-spaced gaps at 120° apart
- Connector: Round-pin Packard (1991–1992) / Flat-pin Packard (1993–1995)
- See: `swap/wiring/connectors/packard-56/cps.md`

## Cam position sensor
- Type: Hall effect — active, square wave output (0V / 5V)
- Location: Inside the distributor body (sync pulse generator / stator)
- Purpose: Required — 18-2-2-2 crank pattern is radially symmetrical and cannot determine engine phase alone
- See: `swap/wiring/connectors/packard-56/cam.md`

## Distributor
- Conventional cap-and-rotor unit
- Houses the cam sensor
- PCM triggers coil via ASD relay — no external ICM

## Open source ECU configuration
- rusEFI trigger name: **Jeep 18-2-2-2**
- Speeduino trigger name: **Jeep 2000** — natively supported; see https://wiki.speeduino.com/en/decoders/Jeep_2000
- Input type: VR (not Hall) for crank; Hall for cam
- Cam sync: Required for sequential injection and accurate ignition timing

## Swap notes
- 18-2-2-2 is natively supported in both rusEFI and Speeduino
- Era 2 is the most straightforward trigger setup in the book — well-documented, widely supported
- CPS connector differs 1991–92 vs 1993–95 — verify before ordering pigtail
- Cam sensor inside distributor remains in place — wire directly to open source ECU cam input
