# Gap Fill: Maintenance and Wear Items

Copy and paste the prompt below into a new chat session with the Knowledgebase Builder agent active.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then check `sourcing/wear-items/` and `work/maintenance/` to see what stubs exist before writing.

## Task

Basic maintenance and consumables are undocumented. Build the foundational wear-item and fluid reference content the expert agent needs to answer routine maintenance questions.

## What to build

### Fluids (`sourcing/wear-items/fluids/`)

**`sourcing/wear-items/fluids/index.md`** — router listing all fluid files

**`sourcing/wear-items/fluids/engine-oil.md`**
- Viscosity: 10W-30 stock; 10W-40 acceptable in high-mileage; 5W-30 for cold climates
- Capacity: 6 quarts with filter
- Change interval: 3,000–5,000 miles conventional; 5,000–7,500 synthetic

**`sourcing/wear-items/fluids/coolant.md`**
- XJ coolant spec: green HOAT or OAT — do NOT use Dex-Cool
- System capacity: ~11 quarts
- Mix ratio: 50/50 distilled water and coolant
- Note on 1987–1990 Renix: same coolant spec, but thermostat housing/sender differences apply

**`sourcing/wear-items/fluids/transmission-fluid.md`**
- AW4: ATF+4 (Mopar spec) — NOT Dexron, NOT Type F
- AX-15: Mopar Manual Transmission Lubricant or Synchromesh MTF
- BA-10/5: Dexron ATF (unusual for a manual — this is correct)
- Capacity by unit

**`sourcing/wear-items/fluids/transfer-case-fluid.md`**
- NP231: ATF+4
- NP242: ATF+4

**`sourcing/wear-items/fluids/axle-fluid.md`**
- Dana 30 front: 80W-90 GL-5
- Dana 35 rear: 80W-90 GL-5
- Chrysler 8.25 rear: 80W-90 GL-5
- AMC 20 rear: 80W-90 GL-5
- Limited slip additive: required if Trac-Lok equipped

### Filters (`sourcing/wear-items/filters/`)

**`sourcing/wear-items/filters/index.md`** — router

**`sourcing/wear-items/filters/engine.md`**
- Oil filter: Renix uses M20×1.5 metric thread; HO uses 7/8″-11 SAE — cross-reference `vehicle/era2/ho-engine.md`
- Air filter: standard panel filter, dry element
- Fuel filter: inline, on frame rail

**`sourcing/wear-items/filters/transmission.md`**
- AW4 filter: drop pan service, flat gasket (no RTV), filter and gasket kit part numbers

### Belts and hoses (`sourcing/wear-items/belts-and-hoses/`)

**`sourcing/wear-items/belts-and-hoses/index.md`** — router

**`sourcing/wear-items/belts-and-hoses/serpentine-belt.md`**
- Belt routing
- Tension: automatic tensioner (1991+); manual adjustment on some Renix years
- Inspection: cracking, fraying, glazing

**`sourcing/wear-items/belts-and-hoses/coolant-hoses.md`**
- Upper and lower radiator hose
- Heater hoses
- Inspection: soft spots, swelling, collar cracking

### Brake components (`sourcing/wear-items/brake-components/`)

**`sourcing/wear-items/brake-components/index.md`** — router

**`sourcing/wear-items/brake-components/overview.md`**
- Front: disc brakes all years
- Rear: drum brakes 1987–2000; rear disc on some 2001 models (verify)
- Rotor specs: stock dimensions
- Pad compound notes: avoid ceramic on trail use (dusting and fade)
- Brake fluid: DOT 3 stock

## Format guidance
Keep files short and reference-oriented. These are lookup files — the expert agent needs to be able to answer "what fluid does the AW4 take" in one file read. Avoid procedural how-to content here; that belongs in `work/maintenance/`.
Also be sure to triple check information with online sources as you work. If its not backed by forum posts we dont want the information in our repository.