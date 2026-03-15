# Renix-Native: TPS Connector

## Used on
- Throttle position sensor — Era 1 (1988–1990) only
- Note: Some 1988–1990 TPS units have 3 pins (standard potentiometer); some have 4 pins (potentiometer + idle switch). Confirm before ordering pigtail.

## Physical description
- 3-pin or 4-pin proprietary Renix body
- Side locking tab
- Located on throttle body, driver's side

## Pinout — 3-pin standard
| Pin | Circuit |
|---|---|
| A | TPS ground |
| B | TPS signal (0.5V–4.5V) |
| C | 5V reference |

## Pinout — 4-pin (with idle switch)
| Pin | Circuit |
|---|---|
| A | TPS ground |
| B | TPS signal |
| C | 5V reference |
| D | Idle switch signal |

## Sourcing
Renix TPS pigtails are difficult to source. The idle switch version is particularly rare.

## Recommended modern substitute
Many builders replace the Renix TPS with a standard Chrysler/GM TPS that fits the Renix throttle body shaft. Confirm shaft diameter and body bolt pattern before ordering. A modern TPS will use a standard Metri-Pack 150 3-pin connector — see `swap/wiring/connectors/metri-pack/mp150-3pin.md`. Idle switch function is not required by open source ECUs.
