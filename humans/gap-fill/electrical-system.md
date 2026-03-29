# Gap Fill: Electrical System (Beyond ECU)

Copy and paste the prompt below into a new chat session with the Knowledgebase Builder agent active.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then read `vehicle/era1/wiring.md`, `vehicle/era2/wiring.md`, and `diagnostics/charging-and-starting/index.md` to understand what already exists before writing.

## Task

The XJ's body electrical and charging systems are undocumented outside of ECU-related wiring. Build foundational coverage for the electrical system that a high-mileage XJ owner would need to understand.

## What to build

**`vehicle/systems/electrical/overview.md`**
- 12V negative-ground system, all years in scope
- Battery: group 34 or group 65 typical; cold cranking amp requirements in cold climates
- Charging system: alternator output by era (Renix ~78A; SBEC/JTEC era ~90–117A depending on year)
- Key-on power distribution: fuse box (Era 1/2 under dash) vs. PDC added (some Era 3)
- Ground architecture: multiple ground straps critical on the XJ — cross-reference `work/restoration/wiring/ground-straps.md`

**`vehicle/systems/electrical/fuse-box.md`**
- Era 1 and Era 2 (1988–1995): single under-dash fuse block; no under-hood PDC
- Era 3 (1996–2001): under-hood PDC added in addition to under-dash fuse block
- Document the location of each fuse block and which circuits each covers
- Note: fuse block connector corrosion is common — inspect when diagnosing electrical gremlins

**`vehicle/systems/electrical/alternator.md`**
- Era 1 (Renix): external voltage regulator; alternator output ~78A
- Era 2+ (HO): voltage regulator integrated into PCM; output varies by year
- Failure symptoms: battery warning lamp, undercharging (below 13.8V at idle), overcharging (above 14.8V)
- Testing: voltage at battery at idle should be 13.8–14.5V
- Note: on Era 2+, alternator field signal comes from the PCM — a failed PCM can cause charging system issues that look like alternator failure

**`vehicle/systems/electrical/body-electrical.md`**
- Power windows: motor failure common on high-mileage XJs; regulator type by year (cable vs. scissor)
- Door locks: actuator failure; vacuum locks on some early years vs. electric on later
- Wiper motor: common failure; park position sensor inside motor fails causing wipers to stop mid-sweep
- Headlight switch: rheostat style; contact wear causes intermittent or no dash lighting
- Blower motor: resistor pack failure causes only high-speed operation; resistor pack location

**`vehicle/systems/electrical/instrument-cluster.md`**
- Analog gauges all years in scope
- Common failures: speedometer (speed sensor signal), temp gauge (sender vs. sensor confusion — cross-reference `vehicle/era2/ho-engine.md`), fuel gauge (sending unit)
- Speedometer sensor: mechanical cable (early years) vs. electronic VSS (later years) — document which years transitioned
- Printed circuit board behind cluster: trace cracking causes dead gauges

Update `vehicle/systems/electrical/index.md` router. Cross-reference from era wiring files where relevant.
Also be sure to triple check information with online sources as you work.