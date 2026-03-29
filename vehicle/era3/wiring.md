# Era 3: Wiring Specifics

## ECU location
JTEC is in the **engine compartment on the passenger-side inner fender**, behind the battery and coolant reservoir tank. Slim silver/gray box — physically different from the black SBEC.

Note: ZJ/WJ Grand Cherokee PCMs are behind the glovebox. XJ Cherokee is under hood — a common cross-platform confusion.

## Fuse box
- 1996: Under-dash fuse block (same as Era 2)
- 1997–2001: Under-hood PDC (Power Distribution Center) — ASD relay and fuel pump relay move to PDC

## ⚡ 1996 wiring
1996 uses JTEC ECU with Era 2 harness architecture. Sensor connectors are Metri-Pack 150 (same as Era 2). Firewall connector routing is the same as Era 2. Treat as an Era 2 harness with a JTEC ECU connector. See `vehicle/era3/1996-notes.md`.

## 1997–2001 wiring changes from Era 2
- Under-hood PDC replaces under-dash relay locations — ASD relay is in the PDC
- EV6 injector connectors replace EV1 on 1999–2001 vehicles
- Downstream O2 sensor adds a second O2 circuit (post-cat)
- EVAP purge solenoid adds a new switched output circuit
- Additional diagnostic circuits for OBD-II compliance

## 2000–2001 coil rail wiring
- Three ignition output wires replace the single coil trigger wire
- Coil 1 (cylinders 1&6), Coil 2 (cylinders 2&5), Coil 3 (cylinders 3&4)
- Cam sensor wiring re-routes from distributor area to front of engine
- All three coil trigger wires must be routed to the open source ECU ignition outputs

## JTEC connector and adapter harness
JTEC uses **three connectors** (Black, White, Grey) — not two. The SBEC uses two connectors; do not use an SBEC pinout for a JTEC vehicle. Mopar connector pigtail P/Ns: Grey 05014011AA, White 05014012AA, Black 05014013AA. See `work/swaps/ecu/wiring/connectors/ecu-body/jtec.md`.

## Grounds
Same ground refresh requirements as all eras. See `work/swaps/ecu/wiring/grounds.md`. Head-to-firewall ground is a common failure point on all XJ years.
