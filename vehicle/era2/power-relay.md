# Era 2: ASD Relay (Automatic Shut Down)

## What the ASD relay does
The PCM activates the ASD relay when it receives a valid CPS signal. The ASD relay simultaneously supplies 12V to:
- Ignition coil primary
- All 6 fuel injectors
- Fuel pump

If the CPS signal is lost at any point, the PCM immediately drops the ASD relay — cutting spark, injector power, and the fuel pump together in a single action.

## Why this matters for the swap
The open source ECU must replicate ASD relay behavior:
- A relay output on the ECU must control a relay wired to supply injectors, coil, and fuel pump
- If the ECU loses crank signal, it must drop this relay
- Most open source ECUs have a dedicated fuel pump output that can drive a relay — wire it to control a single relay supplying all three loads
- Do not wire injectors, coil, and fuel pump to separate unsynchronized relay outputs

## Relay specs
- Standard Bosch-style 4-pin or 5-pin automotive relay (30A)
- ECU output: Low-side ground switching (ECU grounds the relay coil)
- Relay coil: ~85–90 ohm, 12V

## Swap notes
- Unlike Era 1, a single relay controls ignition, fuel, and injectors together — simpler to replicate
- The open source ECU fuel pump control output is typically configurable to behave as an ASD relay equivalent
- Retain the original ASD relay socket in the PDC/fuse box if possible — simplifies wiring
