# Front Axle Disconnect (CAD)

## Purpose
Document the vacuum-operated Central Axle Disconnect (CAD) system used on Command-Trac XJs to disconnect the passenger-side front axle shaft when in 2WD.

## Scope
Factory CAD hardware on 1984–~1991 XJ models equipped with the Command-Trac transfer case (NP207 or NP231). Selec-Trac models (NP228/NP229/NP242) were never equipped with CAD — their front axle shafts are always connected via a one-piece passenger shaft.

---

## What the CAD does

The CAD disconnects the **passenger-side inner axle shaft** when the transfer case is in 2WD. The goal was to eliminate parasitic drag from the front differential, front driveshaft, and ring-and-pinion spinning while in 2WD. In practice, the fuel economy improvement was negligible and the added complexity created a common failure point.

When the CAD is disengaged (2WD mode):
- The passenger-side inner shaft is mechanically separated at a spline collar
- The driver-side inner shaft and the differential still spin (driven by wheel rotation), but no torque path exists through the differential to the front driveshaft
- The front driveshaft is stationary

When the CAD is engaged (4WD mode):
- The spline collar slides to bridge the two-piece passenger inner shaft
- Both front axle shafts are connected through the differential
- The front driveshaft spins, driven by the transfer case

---

## How it works mechanically

The CAD system has four key components in series:

| Component | Location | Function |
|-----------|----------|----------|
| Vacuum switch | On the transfer case shift lever linkage | Toggles vacuum supply between "engage" and "disengage" lines when the driver shifts the t-case |
| Vacuum lines | Route from the switch, along the frame, to the axle housing | Carry vacuum signal; typically four color-coded hard plastic lines |
| Vacuum actuator | Bolted to the passenger side of the Dana 30 axle housing, near the inner axle shaft | Contains a rubber diaphragm that converts vacuum signal to mechanical movement of a shift fork |
| Shift fork and spline collar | Inside the axle housing at the passenger inner shaft | The fork slides the spline collar along the two-piece inner shaft to engage or disengage |

### Engagement sequence
1. Driver shifts the transfer case from 2H to 4H or 4L.
2. The vacuum switch on the shift linkage redirects engine vacuum to the "engage" vacuum line.
3. Vacuum travels through the hard plastic lines (routed along the frame rail) to the actuator on the axle housing.
4. The vacuum pulls the actuator diaphragm, which moves the shift fork.
5. The shift fork slides the spline collar to bridge the gap in the two-piece passenger inner shaft.
6. Both front wheels are now mechanically connected to the front driveshaft via the differential.

### Disengagement sequence
Shifting back to 2H redirects vacuum to the "disengage" line, pulling the diaphragm in the opposite direction and sliding the collar off the spline engagement.

---

## Vacuum line routing

The vacuum lines run from the transfer case shift lever area, along the driver-side frame rail, across the front crossmember, and to the actuator housing on the passenger side of the Dana 30 axle.

There are typically **four color-coded hard plastic vacuum lines**:
- Two lines run to the vacuum actuator on the axle (one for engage, one for disengage)
- One line supplies engine manifold vacuum
- One line connects to a vacuum reservoir / check valve to maintain vacuum signal when manifold vacuum drops (under throttle)

A **vacuum check valve** is in the circuit to maintain the engagement signal even when engine vacuum is low (e.g., during acceleration). If this check valve fails, the CAD may intermittently disengage under throttle.

**Status: needs verification** — The exact color coding and routing path varies by year and source. The above describes the general layout. Consult the factory service manual for the specific year.

---

## Which years had the CAD

| Year range | Transfer case | CAD equipped? |
|------------|--------------|---------------|
| 1984–1986 | NP207 (Command-Trac) | Yes |
| 1984–1986 | NP228/NP229 (Selec-Trac) | No — one-piece shaft |
| 1987–~1991 | NP231 (Command-Trac) | Yes |
| 1987–2001 | NP242 (Selec-Trac) | No — one-piece shaft |
| 1992–2001 | NP231 (Command-Trac) | No — one-piece shaft |

- Some early 1991 production XJs with the NP231 still have the CAD, as Chrysler used remaining inventory during the transition.
- By 1992 production, all NP231-equipped XJs switched to a one-piece passenger axle shaft and eliminated the CAD entirely.
- **All Selec-Trac XJs of any year have one-piece shafts** — full-time 4WD mode requires the front axle to always be engaged.

**Status: needs verification** — The exact last production date for CAD-equipped NP231 XJs is debated. 1991 is the most commonly cited last year on community forums (NAXJA, JeepForum). Some sources cite 1990 as the last clean year with no transition overlap.

---

## Why it fails

The CAD is the single most common reason that 4WD fails to engage on older XJs. The system has multiple age-sensitive failure points:

| Failure | Cause | Symptom |
|---------|-------|---------|
| Cracked vacuum lines | Hard plastic lines become brittle with age and heat cycling | 4WD does not engage — no vacuum signal reaches the actuator |
| Torn actuator diaphragm | Rubber diaphragm deteriorates over time | 4WD does not engage, or engagement is intermittent |
| Corroded spline collar | Moisture intrusion into the axle housing corrodes the collar and shaft splines | 4WD does not engage (collar stuck disengaged), or grinding/clunking in 2WD (collar stuck engaged) |
| Broken shift fork | Shifting into 4WD while front and rear wheels are at different speeds can snap the fork | Permanent inability to engage 4WD via vacuum; collar is free-floating |
| Failed vacuum check valve | Check valve in the supply circuit leaks | 4WD engages briefly then drops out under throttle application |
| Failed vacuum switch | Switch at the transfer case linkage does not toggle vacuum lines | No response at all when shifting the transfer case |

### Stuck engaged vs. stuck disengaged
- **Stuck disengaged** (most common): 4WD does not work. Front wheels spin freely while the transfer case is in 4H/4L. Often caused by vacuum leaks or torn diaphragm.
- **Stuck engaged**: Grinding, clunking, or vibration while driving in 2WD. The front driveline is spinning when it should not be. Caused by a corroded collar that cannot slide back, or a broken fork leaving the collar in the engaged position.

---

## Fix options

### Option 1 — Repair the vacuum system
Replace the hard plastic vacuum lines with flexible rubber vacuum hose from an auto parts store. Inspect and replace the actuator diaphragm if torn. Clean or replace the spline collar if corroded. Replace the vacuum check valve.

**Pros:** Preserves stock configuration. Low cost.
**Cons:** The system will fail again with age. Only practical if the collar and fork are in good condition.

### Option 2 — Posi-Lok manual cable conversion
A manual cable-operated replacement for the vacuum actuator. A knob inside the cab pulls a cable that mechanically slides the collar. Eliminates the entire vacuum circuit.

**Pros:** Reliable, driver-controlled engagement. Moderate cost (~$100–150).
**Cons:** Requires manual actuation — driver must reach down and pull/push the knob when switching between 2WD and 4WD.

### Option 3 — CAD delete (one-piece shaft)
Replace the two-piece passenger inner axle shaft with a one-piece shaft from a 1992+ NP231 XJ or any NP242-equipped XJ. Remove the vacuum actuator and cap or remove the vacuum lines.

**Pros:** Eliminates the entire CAD system permanently. Most reliable long-term solution. The front differential and driveshaft spin in 2WD, but the fuel economy penalty is negligible (same as what 1992+ XJs do from the factory).
**Cons:** Front driveline components spin in 2WD, adding minor wear to U-joints and front differential over time. Requires sourcing the correct one-piece shaft.

**CAD delete is the most popular and widely recommended fix in the XJ community.** It is what Chrysler themselves chose to do starting in 1992.

---

## Cross-links
- Parent: [overview.md](overview.md) — 4WD engagement system overview
- Locking hub misconception: [locking-hubs.md](locking-hubs.md)
- Dana 30 front axle architecture: [`../axles/dana30-front.md`](../axles/dana30-front.md)
- Stock axle specs: [`../axles/stock-specs.md`](../axles/stock-specs.md)
- 2WD vs 4WD configuration: [`../../configurations/2wd-vs-4wd.md`](../../configurations/2wd-vs-4wd.md)

## Boundary links
- CAD delete procedure: `work/upgrades/axles/` (when documented)
- 4WD engagement diagnostics: `diagnostics/driveline/` and `diagnostics/transfer-case/`

## Sources
Community-verified via NAXJA, JeepForum, CherokeeTalk, CherokeeForum; cross-referenced against factory service manual vacuum diagrams and component descriptions.
