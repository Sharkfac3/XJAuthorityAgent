# Era 3: Ignition — Distributor (1996–1999)

## System overview
Identical ignition architecture to Era 2. Single external coil, cap, rotor, and plug wires. JTEC drives the coil primary via the ASD relay. Cam sensor inside the distributor body provides phase sync.

## Components
- Distributor: Cap-and-rotor, houses cam sensor
- Coil: Single external ignition coil, mounted on engine
- Plug wires: 6 individual wires from distributor cap to spark plugs
- Cam sensor: Hall effect, inside distributor — 3-wire (power, ground, signal)

## Swap notes
- Distributor and coil remain physically in place
- Open source ECU connects to: coil negative (trigger), cam sensor signal wire
- Single ignition output on ECU triggers the coil
- No changes to distributor, cap, rotor, or plug wires required
- This is the simpler of the two Era 3 ignition configurations
