# Era 3: Injectors

## Fuel pressure change — critical
Era 3 increased fuel pressure from 39 psi (Era 1/2) to **49 psi**. Era 1/2 injectors are not directly interchangeable without accounting for this difference.

## Specs by year
| Years | Part number | Color | Flow rate | Connector |
|---|---|---|---|---|
| 1996 | Same as Era 2 (53030343) | Tan | ~21 lb/hr @ 39 psi | EV1 |
| 1997–1998 | 53030778 | Gray | ~23.2 lb/hr @ 49 psi | EV1 |
| 1999–2001 | 04854181 | Blue tip | ~22.5 lb/hr @ 49 psi | EV6/USCAR |

## ⚡ 1996 note
1996 retains Era 2 injectors and fuel pressure (39 psi) with EV1 connectors. The fuel pressure increase did not arrive until 1997.

## Connector transition
- 1996: EV1 — see `swap/wiring/connectors/ev1-bosch/injectors.md`
- 1997–1998: EV1 — see `swap/wiring/connectors/ev1-bosch/injectors.md`
- 1999–2001: EV6/USCAR — see `swap/wiring/connectors/ev6-uscar/injectors.md`

## TunerStudio / ECU swap reference
Enter the values matching your specific year into the Required Fuel calculator:
| Years | Flow rate | Fuel pressure |
|---|---|---|
| 1996 | ~21 lb/hr | 39 psi |
| 1997–1998 | ~23.2 lb/hr | 49 psi |
| 1999–2001 | ~22.5 lb/hr | 49 psi |

Injector dead time (open time): 0.9–1.5 ms typical starting point — calibrate against actual injector spec sheet if available.

## Upgrade options

### 1996 (EV1/Jetronic, 39 psi)
Same connector and pressure as Era 1/2 — see `vehicle/era1/injectors.md` for upgrade options.

### 1997–1998 (EV1/Jetronic, 49 psi)
EV1 connector retained but fuel pressure increased to 49 psi. Flow rate scales with pressure — account for this when selecting aftermarket injectors rated at a different base pressure.
Bosch EV14 catalog numbers for EV1/Jetronic connector: 62687, 62203
Status: `needs verification` — confirm connector type before ordering.

### 1999–2001 (EV6/USCAR, 49 psi)
EV6/USCAR is the modern standard connector with the widest aftermarket availability.
Bosch EV14 catalog numbers for EV6/USCAR connector: 62385, 62648, 62647
Status: `needs verification` — confirm connector type before ordering.

Popular GM cross-reference for EV6/USCAR at 49 psi:
| Source | Part number | Flow rate |
|---|---|---|
| Chevy LT1 | 1712424 | ~24 lb/hr @ 43.5 psi |
| Chevy LT4 | 17124251 | ~28 lb/hr @ 43.5 psi |
| Chevy LS1 (98) | 12533952 | ~25.2 lb/hr @ 58 psi |

### Sizing guidance
Stock 4.0L naturally aspirated builds are well served by OEM or direct-equivalent injectors. Upgrade for forced induction or stroker builds. Keep duty cycle below 80% at max power. Larger injectors improve headroom but require careful dead time calibration at idle.

## Swap notes
- If retaining stock injectors, enter the correct flow rate and fuel pressure into ECU software
- If upgrading injectors, the EV6 connector on 1999–2001 is the modern standard — wide aftermarket availability
- EV1-to-EV6 adapter harnesses are available if mixing injector generations
