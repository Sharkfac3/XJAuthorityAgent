# Fuel Pump

## Location
In-tank on all XJ years in scope (1988–2001). The pump is submerged in fuel, which both cools and lubricates it. Running the tank low repeatedly shortens pump life.

## Access
The XJ has **no factory floor pan access port**. The standard method for all years is to drop the fuel tank. There is no rear-seat floor cutout from the factory.

Some owners cut their own access hole through the cargo area floor above the pump. This avoids dropping the tank but requires careful cutting to avoid puncturing the tank, and carries structural and safety considerations. It is a DIY workaround, not a factory method. Source: community discussion (NAXJA, JeepForum).

**Trailer hitch note:** A receiver hitch blocks access to the tank strap hardware on the driver's side. The hitch must be removed before the tank can be dropped. This is a very common complication — plan for it.

## Fuel pressure specs
| Era | Years | Key-on pressure |
|-----|-------|----------------|
| 1 (Renix) | 1988–1990 | 39 psi |
| 2 (SBEC) | 1991–1995 | 39 psi |
| 3 (JTEC) | 1996–2001 | 49 psi |

These are key-on-engine-off specs (Schrader valve test). Era 1/2 pressure is measured with the vacuum line disconnected from the FPR; with vacuum applied at idle it drops to approximately 31 psi. Era 3 runs at a fixed 49 psi regardless of vacuum. Source: community-verified (NAXJA, Cherokee Forum FSM references).

## Typical failure symptoms
- **Whine under load or at WOT** — pump cavitating or weakening; pressure may still be acceptable at idle but drops under demand
- **Engine stumble or hesitation at wide-open throttle** — pump cannot sustain rail pressure at high fuel demand
- **No-start with no fuel pressure** — pump has failed or is not receiving power (check ASD relay and fuse first before condemning the pump)
- **Pressure drops rapidly after key-off** — check valve in the pump has failed; fuel drains back from the lines; hard start after sitting

## Testing procedure
1. Connect a fuel pressure gauge to the Schrader valve on the fuel rail.
2. Cycle the key to RUN (do not crank). Pump should prime and pressure should reach spec within a few seconds.
3. Record pressure at key-on-engine-off — compare to spec above.
4. Start the engine. Pressure should hold near spec at idle (Era 1/2 will drop slightly due to vacuum reference — this is normal).
5. Key off. Observe residual pressure over 30 minutes. Per the Era 1 FSM, pressure should remain between 19–39 psi after 30 minutes. A rapid drop to zero indicates check valve failure or a leaky injector.

To isolate: clamp the return line (Era 1/2 only) and retest. If pressure holds, the leak is the regulator or return line. If pressure still drops, the check valve in the pump or a leaky injector is the cause.

## Replacement
Drop the tank. Drain fuel as much as practical before dropping — reduces weight and spill risk. The pump module is retained by a lock ring on top of the tank; a spanner tool or hammer-and-punch is needed to turn the ring.

On Era 3 (1996–2001), the pressure regulator is part of the pump module assembly. If replacing the pump, the regulator comes with it (or must be transferred from the old module — verify with the specific pump kit). The sending unit is also part of this module on Era 3. See `vehicle/systems/fuel/fuel-tank-and-sending-unit.md`.

**Recommended brands (community consensus):** Bosch and Carter/ACDelco are the community-preferred replacements. Airtex pumps have a documented history of inaccurate sending unit resistance values and premature failure — avoid if possible. Source: NAXJA, Cherokee Forum community threads.
