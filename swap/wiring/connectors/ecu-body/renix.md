# ECU Body Connector: Renix

## Used on
- Renix fuel ECU — Era 1 (1988–1990)
- Located behind the glovebox

## Physical description
- Single large multi-pin connector
- Proprietary Renix body — not a standard industry connector family
- Pin count: ~35–40 pins (varies by year)
- Locking: Sliding secondary lock bar across the connector face

## Key pins for open source ECU swap
When building an adapter harness, these are the circuits that must be identified and transferred:

| Function | Notes |
|---|---|
| Battery 12V | Constant power to ECU |
| Ignition 12V | Switched power |
| Power ground | ECU chassis ground |
| Sensor ground | Separate from power ground |
| Injector outputs (×6) | Low-side drive per cylinder |
| Coil trigger | To ignition module / ICM |
| CPS signal + / − | From bellhousing sensor |
| Cam sensor signal | From distributor |
| TPS signal | From throttle body |
| TPS reference (5V) | From ECU |
| MAP signal | From firewall sensor |
| CTS signal | From manifold |
| IAT signal | From air cleaner |
| O2 signal | From exhaust |
| IAC coil A+, A−, B+, B− | Stepper motor |
| Fuel pump relay | ECU-controlled output |
| Tachometer output | To instrument cluster |

## Adapter harness strategy
The most reversible swap approach is to build an adapter harness: Renix ECU connector on one end, new open source ECU connector on the other. The stock harness is untouched.

Full Renix pinout reference: Confirm against factory service manual (FSM) for the specific year — pin assignments vary between 1988, 1989, and 1990.
