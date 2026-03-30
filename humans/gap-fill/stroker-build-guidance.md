# Gap Fill: Stroker Build Guidance

Copy and paste the prompt below into a new chat session with the Knowledgebase Builder agent active.

---



limited out on this one






You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then read `vehicle/era2/ho-engine.md` thoroughly — it covers block selection, NVH blocks, and valve train. Do not duplicate that content; cross-reference it.

## Task

`ho-engine.md` covers block selection well but there is no actual stroker build guidance. Build coverage for the most common 4.0L stroker combinations, what changes, and what the ECU implications are.

## What to build

**`work/upgrades/engine/stroker-overview.md`**
- What "stroking" means: increasing displacement by using a longer-stroke crankshaft
- The 4.0L is a popular stroker candidate because the block has room to grow and the community has well-documented combinations
- The common stroker uses the 4.2L (258ci) AMC crankshaft — it shares the same block and has a longer stroke (3.895" vs 4.0L's 3.41")
- This results in approximately 4.6L (281ci) displacement
- A true 4.7L is achievable with bore work in addition to the stroke increase
- NVH block (1996+) is the recommended foundation — cross-reference `vehicle/era2/ho-engine.md`

**`work/upgrades/engine/stroker-combinations.md`**

Document the two main combinations the community builds:

**4.6L stroker (most common):**
- Block: 4.0L NVH block (1996+)
- Crank: 4.2L (258ci) AMC crankshaft (3.895" stroke) — requires grinding to fit 4.0L rod journals OR use rod spacers
- Connecting rods: stock 4.0L rods work with crank grinding; aftermarket forged rods preferred for boost
- Pistons: custom or shelf slugs sized for the resulting bore
- Head: stock HO head works; porting improves flow at the increased displacement
- Result: ~281ci, significant low-end torque increase
- Note: 4.2L crank availability — pulled from 4.2L (258ci) AMC/Jeep inline-six engines (1980s Cherokee, Wagoneer, CJ, truck)

**4.7L stroker (bore + stroke):**
- Same crank as above plus a 0.030"–0.060" overbore
- Requires piston selection for the specific bore size
- Less common due to added cost; meaningful displacement gain over 4.6L is small

**`work/upgrades/engine/stroker-ecu-implications.md`**
- A stroker changes the Required Fuel calculation significantly — larger displacement needs more fuel
- With a stock ECU (SBEC or JTEC): the ECU cannot be retuned meaningfully; the added displacement will run rich at idle/cruise and lean at WOT without modification. Not recommended without aftermarket ECU.
- With an aftermarket ECU (Speeduino, rusEFI, Megasquirt): displacement, injector flow rate, VE table, and ignition timing table are all tuneable. This is the correct path for a stroker build.
- Injector sizing: stock 21 lb/hr injectors may be undersized for a stroked engine making real power — calculate duty cycle at expected peak power and size accordingly
- Cross-reference `work/swaps/ecu/` for ECU selection guidance

**`work/upgrades/engine/stroker-head-and-intake.md`**
- The stock HO head flows reasonably well for a mild street stroker
- For more power: port and polish the HO head; the 1999+ "good intake" curved runner manifold is a meaningful upgrade
- Aftermarket options: Clifford Performance sells intake and header combinations; Howell Engine makes fuel injection upgrades
- Header: stock exhaust manifold is restrictive; a quality header is one of the best bang-for-buck upgrades on any 4.0L, stroked or not
- Cam: the stock cam is a reasonable starting point; aftermarket grinds exist from Comp Cams and others for the 4.0L — profile selection depends on intended use (street vs. trail vs. tow)

Place files under `work/upgrades/engine/`. Update `work/upgrades/engine/index.md` router if it exists, or create it.
Also be sure to triple check information with online sources as you work. If its not backed by forum posts we dont want the information in our repository.