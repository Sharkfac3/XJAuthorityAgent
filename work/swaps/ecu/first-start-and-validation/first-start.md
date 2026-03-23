# Tuning: First Start

## Before cranking — verify these first
- [ ] Crank trigger wiring confirmed (CPS polarity marked and correct)
- [ ] Cam sensor wiring confirmed (power, ground, signal — correct pins)
- [ ] TPS reads 0.5V at closed throttle in ECU software
- [ ] MAP reads barometric pressure (~100 kPa) at key-on engine-off
- [ ] CTS reads plausible ambient temperature
- [ ] IAT reads plausible ambient temperature
- [ ] Fuel pump activates at key-on (listen for pump prime)
- [ ] Fuel pressure at spec for the era
- [ ] All injector connectors fully seated
- [ ] No fuel leaks (visual inspection after prime)
- [ ] Ignition output wired to coil negative (or coil rail trigger on 2000–2001)
- [ ] ASD / fuel pump relay wired and functioning
- [ ] All grounds installed and confirmed clean

## Prime the fuel system
Turn key to ON (do not crank) — wait 3 seconds — turn OFF — repeat 3 times. This builds fuel pressure and wets the injectors before the first combustion event.

## First crank attempt
Crank for no more than 5 seconds. If no start:
- Stop — do not continue cranking a flooded engine
- Check: Is ECU receiving crank signal? (Look for RPM reading in ECU software during crank)
- Check: Is spark present? (Remove a plug, ground it, crank — watch for spark)
- Check: Is fuel pump running during crank?
- Check: Is the ASD relay activating?

## Once running
- Do not rev the engine until coolant temperature reaches 160°F
- Watch for fuel leaks constantly during first 5 minutes
- Monitor ECU software: RPM, MAP, CTS, TPS, O2 — all should show plausible values
- Idle quality will be rough — this is expected on a cold base map
- If idle is dangerously rough (misfiring, stalling constantly), richen the idle VE cells before proceeding
