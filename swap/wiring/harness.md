# Wiring: Harness Strategy

## Three approaches — choose before touching a wire

### Option 1: Adapter harness (recommended)
Build a custom pigtail adapter that plugs into the existing stock ECU connector on one end and the new open source ECU connector on the other. The stock engine harness is completely untouched.

**Pros:** Fully reversible. Stock ECU can be reinstalled. Clean installation.
**Cons:** Requires building a custom connector. More upfront work.
**Best for:** Anyone who wants to preserve resale value or trail-side reversibility.

### Option 2: Cut and splice
Cut each wire in the stock harness and splice directly to new ECU pigtail wires. Label every wire before cutting.

**Pros:** Simpler to execute than a full adapter harness. No custom connectors required.
**Cons:** Not reversible without significant rework. One wrong cut is a bad day.
**Best for:** Builders confident in wire identification, committed to the swap.

### Option 3: Full custom harness
Remove the stock engine harness entirely and build a new one from scratch.

**Pros:** Clean, purpose-built, no legacy wiring. Correct wire gauges throughout.
**Cons:** Most labor-intensive. Requires complete knowledge of every circuit.
**Best for:** Engine swap builds, race builds, or when the stock harness is damaged beyond repair.

## Wire identification before any approach
Regardless of method, identify and label every wire in the engine harness before proceeding:
1. Obtain the factory service manual (FSM) wiring diagram for the specific year
2. Use a DVOM to verify each wire's function against the FSM — do not trust wire color alone (colors fade and vary by production run)
3. Label each wire with a numbered tag and document in a spreadsheet: wire number, function, source, destination

## Wire gauge reference
| Circuit | Minimum gauge |
|---|---|
| ECU power supply (12V constant, switched) | 14 AWG |
| ECU power ground | 12 AWG |
| Injector outputs | 16 AWG |
| Ignition coil output | 16 AWG |
| Sensor signals (TPS, MAP, CTS, IAT) | 20 AWG |
| O2 sensor signal | 20 AWG |
| IAC stepper coils | 18 AWG |
| Fuel pump / ASD relay output | 14 AWG |
| Cam and crank sensor signals | 20 AWG shielded |

## Splice method
When splicing is required, use one of these methods only:
- **Solder + adhesive-lined heat shrink** — preferred for all signal wires
- **Ratcheting crimp butt connector (weatherproof)** — acceptable for power and ground circuits
- **Never use:** push-in connectors (Scotchlok, posi-tap), uninsulated butt splices, or electrical tape alone
