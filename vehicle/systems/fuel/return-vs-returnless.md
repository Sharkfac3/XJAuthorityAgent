# Return vs. Returnless Fuel System Architecture

This is one of the most common sources of parts confusion when mixing components across XJ eras or swapping engines.

## Return-style (Era 1/2: 1988–1995)

**Flow path:**
```
Tank → Pump → Fuel filter → Supply line → Fuel rail → Pressure regulator → Return line → Tank
```

The pump runs continuously and produces more fuel than the engine needs at any given moment. Rail pressure is set by a spring-and-diaphragm pressure regulator mounted externally on or near the fuel rail. Excess fuel flows back to the tank through a dedicated return line.

The regulator is vacuum-referenced: intake manifold vacuum acts on the diaphragm, pulling it open and lowering rail pressure slightly at idle and light throttle. This keeps the fuel pressure differential across the injectors consistent relative to manifold pressure, which stabilizes injected quantity per pulse. At wide-open throttle with low vacuum, rail pressure rises toward 39 psi.

**Key characteristics:**
- Two lines at the fuel rail (supply + return)
- Regulator is engine-bay accessible
- Rail pressure varies slightly with vacuum (~31 psi at idle, ~39 psi at WOT)
- Pump runs at a fixed speed; any excess output returns to tank

## Returnless (Era 3: 1996–2001)

**Flow path:**
```
Tank → Pump/regulator module → Supply line → Fuel rail → Injectors
```

The pressure regulator is integrated into the pump module inside the tank. Excess fuel recirculates inside the tank — there is no external return line running back from the engine. The supply line is the only fuel line at the fuel rail.

Rail pressure is fixed at 49 psi regardless of engine load or vacuum. There is no vacuum reference line on the fuel rail.

**Key characteristics:**
- One line at the fuel rail (supply only)
- No external regulator — regulator is inside the tank with the pump
- Fixed rail pressure (49 psi)
- Regulator and pump are typically one module — replacing one means dealing with both

## Why this matters when mixing parts

### Injectors are not interchangeable between eras
Injector flow rate is calibrated at a specific fuel pressure. At higher pressure, the same injector will flow more fuel per millisecond of open time.

- Era 1/2 injectors rated at 39 psi will flow significantly more at the 49 psi Era 3 system, richening the mixture
- Era 3 injectors rated at 49 psi will flow less at the 39 psi Era 1/2 system, leaning the mixture
- Any injector swap across eras requires recalculation of flow rate at the actual rail pressure

See era injector files for specifics:
- `vehicle/era1/injectors.md`
- `vehicle/era2/injectors.md`
- `vehicle/era3/injectors.md`

### Engine swap fuel system matching
If swapping an Era 3 engine (1996–2001) into an Era 1/2 chassis, the fuel system must be matched to the ECU's expectations:

**The ECU and the fuel system must be from the same era.** The JTEC (Era 3) ECU expects fixed 49 psi with no vacuum reference. The Renix and SBEC (Era 1/2) ECUs operate with a vacuum-modulated 39 psi system.

- Swapping an Era 3 engine with its JTEC into an Era 1/2 chassis: the Era 1/2 return-style pump will not produce 49 psi (it will produce 39 psi); the regulator must be changed to match. The simplest approach is to run the Era 3 returnless pump module in the Era 1/2 tank, or re-plumb the tank with a returnless setup.
- Running a return-style pump into a system expecting returnless (or vice versa) will result in incorrect rail pressure and fueling errors.

### Aftermarket ECU (Speeduino/Ocelot) considerations
When running an aftermarket ECU, the fuel system is independent of the ECU type — you can run either architecture with the right configuration. Set the fuel pressure value in the ECU software to match whatever rail pressure your actual fuel system produces. Ensure the injector flow rate entered in TunerStudio/MegaTune matches the injectors at *your* actual rail pressure. Source: see `work/swaps/ecu/wiring/platform-specific/speeduino-ocelot/index.md`.

## Quick reference

| Feature | Era 1/2 (1988–1995) | Era 3 (1996–2001) |
|---------|--------------------|--------------------|
| Architecture | Return-style | Returnless |
| Rail pressure | ~31–39 psi (vacuum-modulated) | 49 psi (fixed) |
| Regulator location | Fuel rail (engine bay) | In-tank pump module |
| Return line at rail | Yes | No |
| Vacuum reference | Yes | No |
| Pump module includes regulator | No | Yes |
