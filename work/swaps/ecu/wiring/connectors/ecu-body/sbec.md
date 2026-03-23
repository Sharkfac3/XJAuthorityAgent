# ECU Body Connector: SBEC

## Used on
- Chrysler SBEC — Era 2 (1991–1995)
- Located behind the glovebox, black rectangular box with cooling fins

## Physical description
- Two connectors: a large primary (C1) and smaller secondary (C2)
- Delphi/Packard multi-pin bodies
- C1: ~60 pin, C2: ~20 pin (varies by year)
- Secondary lock: Sliding bar — must be released before terminal removal

## Key circuits for open source ECU swap

| Function | Connector | Notes |
|---|---|---|
| Battery 12V | C1 | Constant power |
| Ignition 12V | C1 | Switched |
| Power ground (×2) | C1 | Both pins must be used |
| Sensor ground | C1 | Separate from power ground |
| Injector 1–6 outputs | C1 | Low-side, one per cylinder |
| Coil negative (trigger) | C1 | PCM-driven coil primary |
| ASD relay output | C1 | Controls ASD relay coil |
| Fuel pump relay output | C1 | Some years combined with ASD |
| CPS signal + | C1 | From bellhousing sensor |
| CPS signal − | C1 | |
| Cam sensor signal | C1 | From distributor |
| Cam sensor supply | C1 | 8V or 5V — check FSM |
| TPS signal | C1 | |
| TPS reference (5V) | C1 | |
| TPS ground | C1 | |
| MAP signal | C1 | |
| MAP reference (5V) | C1 | |
| MAP ground | C1 | |
| CTS signal | C1 | |
| IAT signal | C1 | |
| O2 signal | C1 | |
| IAC coil 1A, 1B, 2A, 2B | C1 | 4-wire stepper |
| Tachometer output | C2 | To cluster |
| A/C request input | C2 | Optional idle-up |
| TPS output to AW4 | C2 | Must remain connected |

## Full pinout
Confirm pin assignments against the factory service manual (FSM) for the specific year. Pin assignments changed between 1991–1992 and 1993–1995.

## Adapter harness strategy
Same as Renix: build an adapter harness with SBEC connectors on one end and the open source ECU connector on the other. SBEC connector bodies and terminals are available from Mopar and aftermarket suppliers. The SBEC pinout is well-documented in the XJ community.
