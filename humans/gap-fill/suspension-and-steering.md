# Gap Fill: Suspension and Steering

Copy and paste the prompt below into a new chat session with the Knowledgebase Builder agent active.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then check `vehicle/systems/suspension/` and `vehicle/systems/steering/` to see what stubs exist before writing.

## Task

Suspension and steering are empty. Build foundational vehicle-level coverage. This is not a how-to section — it belongs in `vehicle/systems/` and should document what the XJ has stock and why it matters for modifications.

## What to build

### Suspension

**`vehicle/systems/suspension/overview.md`**
- Stock suspension type: front coil spring with upper/lower control arms and track bar; rear leaf springs
- Axles: Dana 30 front, AMC Model 20 or Dana 35 rear (year-dependent), Chrysler 8.25 rear (year-dependent)
- What years got which rear axle
- Factory ride height and ground clearance
- Why the stock geometry creates lift-specific problems (caster, trackbar angle, CV angles)

**`vehicle/systems/suspension/front.md`**
- Control arm geometry
- Track bar: what it does, why angle matters at lift
- Caster: stock spec, what changes at lift, why adjustable upper control arms are the standard fix
- Ball joints: upper and lower, replacement threshold
- Coil spring specs

**`vehicle/systems/suspension/rear.md`**
- Leaf spring pack specs
- Shackle length and lift math
- Add-a-leaf vs. full replacement
- Spring over (SOA) — mention as a lift option, not a detailed how-to
- Rear axle identification: how to tell AMC 20, Dana 35, Chrysler 8.25 apart

**`vehicle/systems/suspension/lift-geometry.md`**
- What changes when you lift an XJ
- Track bar correction: drop bracket vs. adjustable track bar
- Caster correction options
- CV joint angle limits
- Driveshaft angle and SYE relationship
- Brief mention of bump stop extensions

### Steering

**`vehicle/systems/steering/overview.md`**
- Stock steering type: recirculating ball steering box (Saginaw), drag link and tie rod
- Power steering pump: belt-driven, common failure points
- Steering box: location, adjuster screw, when to adjust vs. replace
- Drag link vs. tie rod: what each does, flip kit concept for lifted trucks

**`vehicle/systems/steering/death-wobble.md`**
- What death wobble is and why XJs get it
- Root causes in order of likelihood: worn track bar or track bar bushings, loose track bar bolt, worn drag link, worn tie rod ends, worn ball joints, out-of-balance tires, bent components
- Why it's a cumulative problem (multiple worn parts compound)
- Diagnostic approach: start with track bar, work outward
- Cross-reference `diagnostics/steering-and-suspension/death-wobble.md`

Place all files in `vehicle/systems/suspension/` and `vehicle/systems/steering/`. Update the index files for both directories after writing.
Also be sure to triple check information with online sources as you work.