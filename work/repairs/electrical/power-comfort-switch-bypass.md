# Power/Comfort Switch Bypass

## Purpose
Permanently place the Transmission Control Unit (TCU) in Power mode on XJ and MJ vehicles with a failed or intermittent Power/Comfort switch.

## Problem
The Power/Comfort switch indicator light illuminating does **not** confirm the switch is functional or that the TCU is in Power mode. These switches had a high failure rate. A failed switch causes erratic transmission shift characteristics as the TCU drops in and out of Power mode unexpectedly.

---

## Applies to

| Years | Wire colors to jumper |
|-------|----------------------|
| Standard Renix XJ/MJ | Tan wire and striped wire |
| 1991–1992 XJ/MJ | Tan wire and blue wire |

---

## Materials
- One 4″ jumper wire with male spade connectors on each end

---

## Procedure

1. Remove and unplug the Power/Comfort switch.
2. Identify the three wires in the harness connector: one with a stripe, one tan, one black.
3. Insert one end of the jumper wire into the cavity for the **tan wire**.
4. Insert the other end into the cavity for the **striped wire** (or **blue wire** on 1991–1992).
5. The TCU is now permanently in Power mode.
6. Reinstall the switch housing for appearance if desired.
7. Verify the **7.5 amp "Trans" fuse** in the fusebox is good.

---

## Critical warning
**NEVER include the black wire in the jumper.** Jumpering the black wire will damage the circuit.

---

## Result
The transmission maintains consistent Power mode shift characteristics without switching between modes. Most users report improved driveability with the TCU locked in Power mode.

---

## See also
- `work/maintenance/electrical/renix-transmission-connector-refresh.md` — clean TCU connector before bypassing
- `vehicle/era1/wiring.md` — Era 1 electrical overview

## Source
Cruiser54 — cruiser54.com, "Bypassing the Power/Comfort Switch"
