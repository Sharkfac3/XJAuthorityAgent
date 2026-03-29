# Fuel System Overview

## System type
All XJ years in scope use **Sequential Multi-Port Injection (SMPI)** — one injector per cylinder, fired in sequence. The fuel system delivers pressurized fuel from the tank to the fuel rail, where injectors meter it directly into each intake port.

## Era split — return vs. returnless

### Era 1/2 (1988–1995): Return-style
The fuel pump sends fuel from the tank through the filter to the fuel rail. A vacuum-referenced pressure regulator mounted on the fuel rail controls rail pressure by bleeding excess fuel back to the tank through a dedicated return line.

- Rail pressure: **39 psi** with vacuum line disconnected; drops to approximately **31 psi** at idle with vacuum applied
- The regulator is an engine-bay component — visible and serviceable without dropping the tank
- Two fuel lines run between tank and engine: supply and return
- Source: community-verified (NAXJA, JeepForum, Cherokee Forum — see `vehicle/systems/fuel/fuel-pressure-regulator.md`)

### Era 3 (1996–2001): Returnless
The pressure regulator moved inside the tank as part of the fuel pump module. Excess fuel recirculates inside the tank rather than through an external return line. There is no return line at the fuel rail.

- Rail pressure: **49 psi** (±2 psi) — held constant regardless of engine vacuum
- The regulator is not serviceable without dropping the tank
- Only one fuel line runs from tank to engine: supply only
- Source: community-verified (NAXJA, JeepForum, Cherokee Forum — see `vehicle/systems/fuel/fuel-pressure-regulator.md`)

**Note on 1996:** The 1996 XJ is a transitional year. It uses OBD-II (JTEC) electronics and a returnless fuel system, but carries over some tank and frame-line components from the pre-1996 era. The pump/regulator assembly for 1996 is unique and not interchangeable with 1997–2001. See `vehicle/era3/1996-notes.md`.

## Why the era split matters for injectors

Rail pressure directly affects injector effective flow rate. Injectors are calibrated by the manufacturer at a specific reference pressure — when installed at a different pressure, their actual output changes.

| Era | Rail pressure | Injector connector | Flow rate |
|-----|-------------|-------------------|-----------|
| 1 (1988–1990) | 39 psi | EV1 | ~19 lb/hr |
| 2 (1991–1995) | 39 psi | EV1 | ~21 lb/hr |
| 3 (1996–1998) | 49 psi | EV1 | ~23.2 lb/hr |
| 3 (1999–2001) | 49 psi | EV6/USCAR | ~22.5 lb/hr |

**Era 1/2 and Era 3 injectors are not directly interchangeable** without accounting for the pressure difference. An Era 1/2 injector installed in an Era 3 system will flow more fuel than intended at 49 psi. An Era 3 injector installed in an Era 1/2 system will flow less than intended at 39 psi.

For full injector specs and upgrade options, see:
- `vehicle/era1/injectors.md`
- `vehicle/era2/injectors.md`
- `vehicle/era3/injectors.md`

## Leaf files in this branch

| Topic | File |
|-------|------|
| Fuel pump | `vehicle/systems/fuel/fuel-pump.md` |
| Fuel pressure regulator | `vehicle/systems/fuel/fuel-pressure-regulator.md` |
| Fuel tank and sending unit | `vehicle/systems/fuel/fuel-tank-and-sending-unit.md` |
| Return vs. returnless architecture | `vehicle/systems/fuel/return-vs-returnless.md` |
