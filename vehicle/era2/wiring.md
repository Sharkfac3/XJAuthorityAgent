# Era 2: Wiring Specifics

## ECU location
SBEC is behind the glovebox. Single black rectangular box with cooling fins on the housing.

## Firewall connectors
Same multi-pin firewall connector as Era 1 — inspect and clean all pins before the swap.

## Key wiring features
- Single ECU — one adapter harness covers everything
- ASD relay in the under-dash fuse block controls coil, injectors, and fuel pump together
- All sensor connectors are Metri-Pack 150 (2-pin and 3-pin) — widely available, easy to service
- CPS connector split: round-pin on 1991–1992, flat-pin on 1993–1995 — see `swap/wiring/connectors/packard-56/cps.md`
- TPS signal wire branches to AW4 TCM — must remain intact through the swap

## Injector harness
Separate sub-harness with EV1 connectors. Inspect all 6 connectors — replace any with cracked housing or broken locking tabs. A full 6-injector pigtail harness is available from XJ suppliers and is worth installing at swap time.

## Fuse box
Under-dash fuse block on 1991–1995. No under-hood PDC.

## SBEC connector and adapter harness
The SBEC uses two connectors (C1 primary, C2 secondary). Both must be addressed. The SBEC pinout is the most thoroughly documented of all three eras — multiple verified community pinouts exist. Cross-reference at least two sources before building the adapter harness. See `swap/wiring/connectors/ecu-body/sbec.md`.

## Grounds
Run new dedicated grounds before the swap. Head-to-firewall ground is particularly important and frequently missing or corroded on Era 2 vehicles. See `swap/wiring/grounds.md`.
