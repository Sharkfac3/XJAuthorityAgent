# Gap Fill: Sourcing Gaps

Copy and paste the prompt below into a new chat session with the Knowledgebase Builder agent active.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then read `sourcing/index.md` and all existing sourcing files to understand what's already there before writing anything.

## Task

Most of the `sourcing/` tree is empty routers. Build the sourcing content the expert agent needs to answer "where do I get this" and "OEM or aftermarket" questions.

## What to build

### Swap kits (`sourcing/swap-kits/`)

**`sourcing/swap-kits/index.md`** — update router with leaf table

**`sourcing/swap-kits/lift-kits.md`**
- Types: spacer lift (budget), coil spring lift, long-arm suspension
- What's in a typical kit: springs, shocks, track bar bracket, sway bar links, bump stop extensions
- Brands with known XJ fitment: Rough Country, Rubicon Express, Old Man Emu, TeraFlex
- What a kit does NOT fix: caster (needs adjustable UCAs separately), driveshaft angle (needs SYE for larger lifts)
- Lift height guidance: 2" = spacer or mild spring; 3.5"–4.5" = most common, good trail clearance with geometry correction; 6"+ = long-arm territory

**`sourcing/swap-kits/sye-kits.md`**
- SYE = Slip Yoke Eliminator; converts NP231 from slip yoke output to fixed flange for better driveshaft angles at lift
- Required with: lifts over ~3.5" combined with stock slip yoke driveshaft, or any time driveshaft vibration appears at lift
- Kit includes: tailhousing replacement, fixed output flange, often a new rear driveshaft or CV driveshaft
- Brands: Tom Woods, TeraFlex, SYE.com (Advance Adapters)
- Cross-reference `vehicle/systems/transfer-case/np231.md`

**`sourcing/swap-kits/cad-delete.md`**
- CAD delete kit replaces the vacuum-actuated front axle disconnect with a solid inner shaft
- Eliminates the vacuum system failure point entirely
- Typically includes: solid inner axle shaft, new seal, sometimes updated lockout hub
- Cross-reference `vehicle/systems/4wd/front-axle-disconnect.md`

### OEM vs. aftermarket guidance

**`sourcing/oem-vs-aftermarket/cooling/index.md`** → **`sourcing/oem-vs-aftermarket/cooling/radiator.md`**
- OEM-style aluminum radiator: adequate for stock engine; Mishimoto and Wizard Cooling are well-regarded aftermarket options
- When to upgrade: towing, built engine, hot climate operation
- Cheap eBay radiators: inlet/outlet sizing and fitting positions frequently wrong for XJ — avoid

**`sourcing/oem-vs-aftermarket/engine/gaskets.md`**
- Head gasket: Felpro is the community standard; MLS (multi-layer steel) preferred over composite for built engines
- Exhaust manifold gasket: stock-style or Remflex (graphite) — Remflex handles cracked manifold surfaces better
- Intake manifold gasket: Felpro stock replacement is fine

**`sourcing/oem-vs-aftermarket/brakes/pads-and-rotors.md`**
- Front rotors: stock size replacement is straightforward; EBC, PowerStop, and Centric are well-regarded
- Pad compound: semi-metallic for street/trail; avoid ceramic for off-road (dusting at temperature, reduced initial bite)
- Rear drums: standard replacement — no strong preference; just avoid the cheapest no-name hardware

**`sourcing/oem-vs-aftermarket/electrical/sensors.md`**
- CPS (crank position sensor): OEM Mopar or Standard Motor Products preferred; cheap offshore sensors cause intermittent no-start
- TPS: Standard Motor Products or OEM; avoid cheap replacements — dead spots cause drivability issues
- CTS / IAT: standard NTC thermistors; most aftermarket replacements are acceptable
- O2 sensor: Bosch or Denso; avoid cheap replacements on a tuned setup

### Interchange

**`sourcing/interchange/electrical/index.md`**
- Battery: Group 34 or Group 65; any brand
- Alternator: Denso OEM replacement; remanufactured units have mixed reliability
- Starter: OEM Nippondenso or quality reman; high-torque aftermarket available for built engines

**`sourcing/interchange/drivetrain/index.md`**
- Driveshafts: Tom Woods custom driveshafts are the community standard for lifted XJs; stock-length shafts from same-year XJs interchange
- U-joints: Spicer (Dana) OEM-spec joints; greaseable u-joints preferred for off-road

### Donor vehicle strategy

**`sourcing/donor-vehicles/electrical/index.md`**
- Best donor for ECU: same-era XJ or ZJ (same harness and ECU)
- Alternator: same-year XJ or ZJ; MJ Comanche also compatible
- Instrument cluster: same year range only (gauge calibrations differ)

**`sourcing/donor-vehicles/drivetrain/index.md`**
- AW4 transmission: any 1987–2001 XJ, ZJ with 4.0L
- AX-15: 1989–1995 XJ or YJ with 4.0L or 2.5L (bellhousing differs by engine)
- NP231: any 1987–2001 XJ — highly interchangeable; verify slip yoke vs. fixed flange output

Update all index.md routers in affected directories after writing.
Also be sure to triple check information with online sources as you work. If its not backed by forum posts we dont want the information in our repository.