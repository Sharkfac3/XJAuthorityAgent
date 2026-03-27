# Renix Distributor Indexing

## Purpose
Correctly index the distributor rotor to the #1 terminal on Renix-era (1987–1990) 4.0L engines to maximize spark strength and eliminate light-throttle bucking caused by factory misalignment.

## Why this matters
The distributor rotor has significant physical width. When the ECU commands ignition, the rotor must be positioned so its trailing edge is just departing the #1 cap terminal — not approaching it. Factory distributors frequently shipped out of spec. Poor alignment forces the spark to bridge a larger gap between rotor tip and terminal, weakening ignition. A Jeep TSB identified distributor indexing as the fix for light-throttle bucking and jerking.

**This procedure applies to Renix 4.0L only. HO engines (1991+) require different methodology.**

---

## Prerequisites
- Establish #1 TDC using the compression method: `work/setup-and-calibration/engine/4-0-tdc-procedure.md`
- One old/spare distributor cap (to cut an inspection window)

## Tools
- 3/4″ wrench or socket (crankshaft bolt)
- Flat blade screwdriver
- Soft-jaw vise
- Saw (to cut distributor locating tab)
- Small file or deburring tool
- O-ring NAPA #727-2024 (replaces traditional distributor gasket)

---

## Procedure

### Step 1 — Create inspection window cap
Cut a window in the old distributor cap at the #1 spark plug wire post. This allows you to watch the rotor tip relative to the #1 terminal during installation.

### Step 2 — Confirm #1 TDC
Rotate the engine clockwise using the 3/4″ crankshaft bolt. Confirm #1 TDC via compression test (finger over plug hole). Align the balancer mark to the 0° mark on the front cover. The rotor tip should be near the #1 position.

### Step 3 — Remove the distributor
- Unplug the distributor electrical connector.
- Remove the holddown clamp and bolt.
- Extract the distributor.
- Remove the cap and rotor.

### Step 4 — Modify the locating tab
- Place the distributor housing upside down in a soft-jaw vise.
- Scribe a line 1/2″ from the end of the distributor locating tab.
- Cut at the scribed line.
- Clean away all burrs and metal debris before reinstalling the rotor.

### Step 5 — Position the oil pump drive shaft
Through the distributor bore, use a flat blade screwdriver to rotate the oil pump gear drive shaft slot to slightly past the **11 o'clock** position.

### Step 6 — Initial installation
- Align the modified locating tab with the holddown clamp bolt hole.
- Rotate the rotor to approximately **4 o'clock**.
- Lower the distributor into the bore until fully seated — the rotor should end up at approximately **5 o'clock** as the helical gear meshes.

### Step 7 — Final alignment
- Install the window cap.
- Rotate the distributor **housing** (not the engine) until the **trailing edge** of the rotor tip just departs the #1 terminal — the rotor has just passed #1, not approaching it.
- Secure the holddown clamp and bolt.
- Verify the rotor position has not shifted during tightening.
- Install the new cap and reconnect all electrical connections.

---

## Verification
Check ignition timing with a timing light at idle. After correct indexing, the ECU-controlled timing should show approximately **12 degrees advance**.

---

## Notes
- **Trailing edge** means the rotor has just passed #1 — if in doubt, the rotor should be slightly past the terminal in the direction of rotation, not before it.
- Firing order progresses clockwise around the cap per the sequence cast on the intake manifold.
- The cam position sensor inside the Renix distributor fires injectors sequentially. The ECU compensates if it fails, but correct indexing optimizes the whole system.
- Use NAPA O-ring #727-2024 in place of the traditional distributor gasket for better sealing.

---

## See also
- `work/setup-and-calibration/engine/4-0-tdc-procedure.md` — establish TDC before indexing
- `diagnostics/ignition/no-spark.md` — if indexing is being done as part of a no-spark diagnosis
- `vehicle/era1/wiring.md` — Renix ICM and distributor wiring context

## Source
Cruiser54 — cruiser54.com, "Distributor Indexing for Renix 4.0L Engines"
