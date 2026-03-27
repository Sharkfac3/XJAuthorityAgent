# EGR Valve Test

## Purpose
Diagnose EGR valve function on XJ and MJ engines — confirming the valve opens under load, closes at idle, and is not leaking exhaust gas at idle.

## Applies to
All XJ/MJ engines equipped with EGR. Particularly relevant to 1987–1990 Renix vehicles where EGR-related vacuum circuits are common fault points.

---

## Test 1 — Opening test (valve must open under load)

### Procedure
1. Bring the engine to normal operating temperature.
2. With the engine at idle, rapidly open and close the throttle to reach at least 1,500 RPM.
3. Watch the EGR valve diaphragm for movement.

### Results

| Observation | Interpretation |
|-------------|---------------|
| Diaphragm moves visibly | EGR opens correctly |
| No diaphragm movement | Faulty vacuum signal, vacuum line leak, defective EGR diaphragm, or defective backpressure sensor |

---

## Test 2 — Closing test (valve must close at idle)

### Procedure
1. Engine warm, at idle.
2. Manually depress the EGR valve diaphragm by hand.

### Results

| Observation | Interpretation |
|-------------|---------------|
| RPM drops immediately | Valve was properly closed at idle; passage is open |
| RPM changes very little, idle is normal | Passage between EGR valve and intake manifold is plugged — exhaust gas is not reaching the combustion chamber |
| RPM changes very little, idle is already poor | Valve is not closing fully — carbon buildup on the pintle, leaking EGR valve gasket, or bad EGR valve |

---

## Common fault causes
- Faulty vacuum signal to the EGR valve
- Vacuum line leak in the EGR circuit
- Defective EGR diaphragm
- Defective backpressure sensor (Renix)
- Carbon between the pintle and seat (prevents full closure)
- Leaking EGR valve gasket
- Plugged passage between EGR valve and intake manifold

---

## See also
- `vehicle/era1/` — Renix vacuum and EGR system context
- `diagnostics/engine/exhaust-restriction-vacuum-test.md` — if exhaust restriction is suspected alongside EGR issues
- `work/maintenance/engine/throttle-body-and-iac-cleaning.md` — if idle quality is poor after EGR diagnosis

## Source
Cruiser54 — cruiser54.com, "EGR Valve Test"
