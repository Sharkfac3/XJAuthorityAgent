# Fuel Pressure Regulator

## Era 1/2 (1988–1995) — External, Rail-Mounted

The regulator is mounted on or near the fuel rail, on the engine side of the system. It is a spring-and-diaphragm device referenced to intake manifold vacuum.

**Location:** On the fuel rail, typically at the front or driver-side end. Accessible in the engine bay without dropping the tank.

**Pressure behavior:**
- With vacuum line disconnected: **39 psi** — this is the base spec and the figure used for injector calibration
- With vacuum applied at idle: approximately **31 psi** — the vacuum pulls the diaphragm open, allowing more fuel to return to the tank and lowering rail pressure
- This vacuum reference allows the system to maintain a consistent fuel/air mixture across throttle positions

**Vacuum line note:** A cracked or disconnected vacuum reference line causes the regulator to run at max pressure (39 psi) at all times, which richens the mixture at idle and light throttle. Always check the vacuum line when diagnosing fuel mixture or idle issues on Era 1/2.

**How it works:** Pump output is unregulated at source. Excess fuel flows through the regulator's return port back to the tank. Rail pressure is set by regulator spring tension, modified by manifold vacuum. See `vehicle/systems/fuel/return-vs-returnless.md`.

Source: Community-verified (NAXJA forum, FSM references — 39 psi without vacuum, ~31 psi with vacuum applied).

## Era 3 (1996–2001) — In-Tank, Part of Pump Module

The regulator moved inside the fuel tank with the redesign to OBD-II. It is integrated into the top of the fuel pump module. There is no external regulator at the fuel rail on Era 3.

**Location:** Inside the tank, on top of the pump module. Not accessible without dropping the tank.

**Pressure behavior:**
- Fixed at **49 psi** — no vacuum reference, no load-dependent variation
- The regulator bypasses excess fuel internally within the tank rather than through an external return line

**1996 note:** The 1996 XJ has a unique pump/regulator assembly that is not interchangeable with 1997–2001 units. The 1996 uses a carry-over tank from pre-1996 with a new-style pump module fitted to it. Regulator OEM part number 4669239 is cited in forum sources. Confirm year-specific fitment before ordering. Source: NAXJA.

**Parts confusion warning:** Aftermarket suppliers have been documented supplying an Era 1/2 rail-mount regulator when the customer ordered a 1996 part. An Era 1/2 regulator installed in the pump assembly will produce ~39 psi instead of 49 psi, causing rich-running or no-start conditions. Verify the part tests at 49 psi before installation. Source: Cherokee Forum, NAXJA threads.

## Failure symptoms (all eras)

- **Rich at idle / black exhaust** — regulator diaphragm has failed, allowing fuel into the vacuum reference line (Era 1/2); or regulator is stuck open, flooding the rail
- **Lean or low power** — regulator stuck closed (high pressure) or failed open causing low pressure
- **Fuel smell from vacuum line (Era 1/2)** — diaphragm failure; fuel is being drawn into the intake manifold through the vacuum reference port
- **Hard start after sitting** — check valve failure or regulator allowing pressure to bleed back to tank

## Testing (Era 1/2)

1. With engine running, connect a fuel pressure gauge at the Schrader valve on the rail.
2. At idle with vacuum line connected: approximately 31 psi.
3. Disconnect the vacuum reference line from the regulator. Pressure should immediately rise to approximately 39 psi.
4. If pressure does not change when the vacuum line is disconnected, the vacuum reference circuit is not functioning — check the line, check for cracks.
5. With the vacuum line disconnected, check for fuel weeping out of the vacuum port. Any fuel here means the diaphragm has failed — replace the regulator.

## Testing (Era 3)

1. Connect fuel pressure gauge at the Schrader valve.
2. Key-on engine-off: should reach 49 psi within a few seconds.
3. Start engine. Pressure should hold at 49 psi at idle.
4. Key off. Observe pressure decay over several minutes. Rapid drop suggests check valve failure in the pump module or a leaky injector.
