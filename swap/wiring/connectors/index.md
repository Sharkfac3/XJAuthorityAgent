# Connectors: Index

## How to use this folder
Identify the connector family first, then load the specific file. Every connector file contains: physical description, pin count, terminal part number, seal part number, release tool, and sourcing notes.

## Connector families

| Family | Folder | Used on |
|---|---|---|
| EV1 / Bosch Jetronic | `ev1-bosch/` | Injectors — Era 1, Era 2, Era 3 (1996–1998) |
| EV6 / USCAR | `ev6-uscar/` | Injectors — Era 3 (1999–2001) |
| Metri-Pack | `metri-pack/` | TPS, MAP, CTS, IAT, O2, IAC — Era 2 and Era 3 |
| Packard 56 | `packard-56/` | CPS, cam sensor — Era 2 and Era 3 |
| Renix-native | `renix-native/` | All sensors — Era 1 only |
| ECU body | `ecu-body/` | Main ECU harness connector — all eras |

## Quick lookup by sensor

| Sensor | Era 1 | Era 2 | Era 3 (1996) | Era 3 (1997+) |
|---|---|---|---|---|
| Injectors | `ev1-bosch/` | `ev1-bosch/` | `ev1-bosch/` | `ev1-bosch/` (to 1998) / `ev6-uscar/` (1999+) |
| MAP | `renix-native/map.md` | `metri-pack/mp150-3pin.md` | `metri-pack/mp150-3pin.md` | `metri-pack/mp150-3pin.md` |
| TPS | `renix-native/tps.md` | `metri-pack/mp150-3pin.md` | `metri-pack/mp150-3pin.md` | `metri-pack/mp150-3pin.md` |
| CTS | `renix-native/cts.md` | `metri-pack/mp150-2pin.md` | `metri-pack/mp150-2pin.md` | `metri-pack/mp150-2pin.md` |
| IAT | `renix-native/cts.md` | `metri-pack/mp150-2pin.md` | `metri-pack/mp150-2pin.md` | `metri-pack/mp150-2pin.md` |
| CPS | `renix-native/cps.md` | `packard-56/cps.md` | `packard-56/cps.md` | `packard-56/cps.md` |
| Cam sensor | — | `packard-56/cam.md` | `packard-56/cam.md` | `packard-56/cam.md` |
| ECU body | `ecu-body/renix.md` | `ecu-body/sbec.md` | `ecu-body/jtec.md` | `ecu-body/jtec.md` |
