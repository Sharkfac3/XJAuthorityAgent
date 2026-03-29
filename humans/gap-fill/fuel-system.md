# Gap Fill: Fuel System

Copy and paste the prompt below into a new chat session with the Knowledgebase Builder agent active.

---

limited out with this one already ran



You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then read `vehicle/era1/injectors.md`, `vehicle/era2/injectors.md`, and `vehicle/era3/injectors.md` (if it exists) before writing — injector content already exists and should be cross-referenced, not duplicated.

## Task

The fuel system beyond injectors is undocumented. Build coverage for the pump, tank, regulator, and system architecture differences by era.

## What to build

**`vehicle/systems/fuel/overview.md`**
- System type: sequential multi-port injection (SMPI) all years in scope
- Era 1/2 (1988–1995): return-style system — fuel pump sends to rail, regulator returns excess to tank
- Era 3 (1996–2001): returnless system — regulator is in or on the tank, no return line at rail
- Why this matters: fuel pressure spec differs (39 psi Era 1/2, 49 psi Era 3), and injector flow rate is calibrated to rail pressure — injectors are not interchangeable between eras without recalibration
- Cross-reference injector files for era-specific injector specs

**`vehicle/systems/fuel/fuel-pump.md`**
- Location: in-tank on all XJ years in scope
- Access: through the floor under rear seat or through the top of the tank (varies by year — document which)
- Typical failure: pump whine under load, engine stumble at WOT, no-start with no fuel pressure
- Fuel pressure specs: Era 1/2 = 39 psi key-on; Era 3 = 49 psi key-on
- Testing: fuel pressure gauge at Schrader valve on rail; residual pressure after key-off (should hold)
- Replacement: drop tank or access through floor pan

**`vehicle/systems/fuel/fuel-pressure-regulator.md`**
- Era 1/2: external regulator on or near the fuel rail; vacuum-referenced on some years
- Era 3: in-tank regulator (part of the pump module)
- Failure symptoms: rich/lean at idle, fuel smell, black exhaust
- Testing: compare fuel pressure at idle vs. key-on-engine-off; check vacuum reference line on vacuum-referenced regulators

**`vehicle/systems/fuel/fuel-tank-and-sending-unit.md`**
- Tank capacity: 20.2 gallons (most years)
- Sending unit: in-tank float, drives dash fuel gauge
- Common failures: float arm bent or stuck (false full/empty reading), sending unit corrosion
- Note: on Era 3, the sending unit is integrated with the pump module — both replaced together

**`vehicle/systems/fuel/return-vs-returnless.md`**
- Explain the architectural difference clearly — this is a common source of confusion when mixing parts across eras
- Return style (Era 1/2): pump → filter → rail → regulator → return line → tank. Rail pressure set by regulator.
- Returnless (Era 3): pump module includes regulator. Pump output is already at regulated pressure. No return line at engine.
- Swap implications: if swapping an Era 3 engine into an Era 1/2 chassis, the fuel system architecture must match the ECU's expectations; cannot mix a returnless pump with a return-style ECU setup without modification

Update `vehicle/systems/fuel/index.md` router. Cross-reference from `vehicle/era1/overview.md`, `vehicle/era2/overview.md`, and `vehicle/era3/overview.md`.
Also be sure to triple check information with online sources as you work. If its not backed by forum posts we dont want the information in our repository.