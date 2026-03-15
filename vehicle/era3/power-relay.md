# Era 3: ASD Relay (Automatic Shut Down)

## Identical to Era 2 in function
The JTEC uses the same ASD relay architecture as the SBEC. The relay simultaneously supplies 12V to the ignition coil (or coil rail on 2000–2001), fuel injectors, and fuel pump. PCM drops the relay on CPS signal loss.

## 2000–2001 coil rail note
On 2000–2001 vehicles the ASD relay supplies all 3 coil rail outputs rather than a single coil. The relay and PCM behavior is identical — only the load on the ignition side differs.

## Swap implications
Same as Era 2 — see `vehicle/era2/power-relay.md` for the full wiring strategy. The open source ECU fuel pump/ASD output replicates this behavior identically across Era 2 and Era 3.
