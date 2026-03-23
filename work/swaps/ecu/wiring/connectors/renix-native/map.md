# Renix-Native: MAP Sensor Connector

## Used on
- MAP sensor — Era 1 (1988–1990) only
- Firewall-mounted MAP sensor, 3-wire

## Physical description
- 3-pin proprietary Renix body
- Rectangular, approximately 20mm wide
- Single top locking tab
- Wire seals: integral to connector body

## Pinout
| Pin | Circuit |
|---|---|
| A | 5V reference |
| B | MAP signal (0.5V–4.5V) |
| C | Sensor ground |

## Sourcing
Renix MAP pigtails are rarely stocked. Check XJ-specific forums and suppliers.

## Recommended modern substitute
Replace the Renix MAP sensor entirely with a GM 1-bar MAP sensor (GM part 16040749 or equivalent). The GM sensor:
- Mounts directly on the intake manifold (eliminates firewall mount and long vacuum hose)
- Uses a standard 3-pin Metri-Pack 150 connector — see `work/swaps/ecu/wiring/connectors/metri-pack/mp150-3pin.md`
- Is natively supported in rusEFI and Speeduino calibration tables
- Is widely available and inexpensive

When substituting, update the MAP sensor calibration table in ECU software to the GM 1-bar curve.
