# Renix-Native: CPS Connector

## Used on
- Crankshaft position sensor — Era 1 (1988–1990) only
- Bellhousing-mounted VR sensor

## Physical description
- 2-pin proprietary Renix body + separate shield wire
- Rectangular housing with integral strain relief
- The shield wire (bare or with ring terminal) grounds separately to the block — do not omit

## Pinout
| Pin | Circuit |
|---|---|
| A | CPS signal + |
| B | CPS signal − |
| Shield | Ground to engine block |

## Polarity
VR sensors are polarity-sensitive. Reversing A and B shifts the trigger edge and will cause incorrect ignition timing. Mark wire orientation before disconnecting.

## Signal characteristics
The Renix CPS produces a weak signal at cranking RPM — this is a known characteristic of the sensor and the 66-2-2-2 pattern. At cranking speed (~200 RPM), peak-to-peak voltage may be as low as 1V. Verify the open source ECU's VR input threshold can reliably detect this signal, or plan for a VR signal conditioner board between the sensor and ECU.

## Sourcing
Renix CPS pigtails are scarce. The sensor itself (available from XJ suppliers) typically comes with a short pigtail — splice to existing harness.

## Swap note
No modern drop-in substitute exists for the Renix CPS at the bellhousing location. The sensor must be retained, or the flywheel/flexplate swapped for an Era 2/3 unit with the 18-2-2-2 pattern — which uses a standard CPS with Packard connectors. See `vehicle/era1/trigger.md` for the flywheel swap option.
