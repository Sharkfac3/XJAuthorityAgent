# Coverage Roadmap

This document seeds the next waves of repo expansion across the broader Jeep XJ platform.

It is a roadmap for branch creation and backlog seeding.
It is not a command to research every topic immediately.

Use it with:
- `docs/research-pipeline.md`
- `docs/topic-intake-rules.md`
- `docs/backlog-seeding-guide.md`
- `docs/repo-taxonomy.md`
- `skillbuilding/prioritization-rubric.md`

## Purpose
The repo needs a durable way to expand from ECU-swap-centered coverage into a full Jeep XJ technical knowledge system.

This roadmap defines:
- what major branches should exist
- how they should be seeded without overbuilding
- what order of expansion provides the most value
- how to balance platform-wide coverage against legacy swap depth

---

# 1. Roadmap principles

1. Seed branches before filling them deeply.
2. Prioritize breadth of structure before encyclopedic depth.
3. Keep stock facts, procedures, diagnostics, and sourcing separate.
4. Create routers and narrow leaf targets, not giant placeholder manuals.
5. Expand by practical reader value, risk reduction, and dependency leverage.
6. Respect current canonical `swap/` content during migration.

---

# 2. Expansion phases

## Phase 1: Platform skeleton and high-value routers
Goal:
Create the minimum durable branch structure needed to support full-domain growth.

Primary outcomes:
- major domain routers are present
- major system branches are named consistently
- broad topic families have canonical destinations
- backlog seeding can point to stable targets

Typical work:
- create indexes and overview files
- define compatibility splits
- add stubs only where the branch is clearly durable

## Phase 2: Broad operational coverage
Goal:
Cover the most common XJ owner needs at a usable level.

Priority emphasis:
- maintenance
- repair baselines
- high-frequency diagnostics
- stock platform baselines
- common interchange decisions

Target outcome:
Many core branches reach `partial` or `usable with caveats`.

## Phase 3: High-friction modifications and upgrades
Goal:
Expand into common platform changes that depend on good baselines.

Priority emphasis:
- brakes
- suspension
- steering
- charging/electrical improvements
- cooling upgrades
- driveline upgrades
- axle and interchange planning

## Phase 4: Deep diagnostics, restoration, and specialized projects
Goal:
Broaden and harden advanced branches after baseline coverage exists.

Priority emphasis:
- symptom trees and verification logic
- body/interior restoration
- HVAC nuance
- package- and year-specific edge cases
- high-detail sourcing and donor families
- advanced swaps beyond current ECU coverage

---

# 3. Priority model across repo domains

Use this when choosing between swaps, upgrades, maintenance, diagnostics, restoration, and interchange topics.

## Default platform-wide priority order
1. safety-critical and immobilizing diagnostics
2. maintenance schedules and common service procedures
3. stock platform baselines that unlock many other topics
4. common repair procedures
5. high-friction sourcing/interchange decisions
6. common modifications and upgrades
7. swap hardening and expansion
8. restoration and preservation depth

## Why this order
- diagnostics and maintenance have the widest platform impact
- stock baselines are dependencies for every other domain
- sourcing reduces wrong-part and wrong-donor drift
- common upgrades affect many readers but usually depend on the baseline first
- swaps remain important, but platform-wide growth should not let them dominate all roadmap decisions
- restoration matters, but should grow on a stable base

## Override cases
Move a topic upward when it is:
- safety-critical
- highly repeated in user demand
- blocking several downstream branches
- easy to validate and seed quickly
- a known transition-year trap

---

# 4. Seed branch map

These are the minimum roadmap branches that should be seeded over time.
The list is intentionally broad and structural.
It does not imply deep content for every branch yet.

## A. Engine systems
### Stock baseline
- `vehicle/systems/engine/`

### Work branches
- `work/maintenance/engine/`
- `work/repairs/engine/`
- `work/upgrades/engine/`
- `work/swaps/drivetrain/` for major engine-family changes

### Diagnostics
- `diagnostics/engine/`
- `diagnostics/ignition/`

### Sourcing
- `sourcing/interchange/engine/`
- `sourcing/donor-vehicles/drivetrain/`

### Seed topics
- engine family baselines
- ignition architecture differences
- compression/leakdown and baseline health checks
- common gasket and sealing jobs
- top-end refresh planning
- sensor-family compatibility

## B. Fuel system
### Stock baseline
- `vehicle/systems/fuel/`

### Work branches
- `work/maintenance/fuel/`
- `work/repairs/fuel/`
- `work/upgrades/fuel/`

### Diagnostics
- `diagnostics/fuel/`

### Sourcing
- `sourcing/interchange/fuel/`
- `sourcing/wear-items/fuel/`

### Seed topics
- stock fuel delivery architecture
- pump/module/filter baselines by era
- injector family baselines
- fuel pressure test paths
- common leak and no-pressure branches
- replacement-part family guidance

## C. Cooling system
### Stock baseline
- `vehicle/systems/cooling/`

### Work branches
- `work/maintenance/cooling/`
- `work/repairs/cooling/`
- `work/upgrades/cooling/`

### Diagnostics
- `diagnostics/cooling/`

### Sourcing
- `sourcing/interchange/cooling/`
- `sourcing/oem-vs-aftermarket/cooling/`

### Seed topics
- radiator/fan/thermostat baselines
- refresh and flush procedure routes
- overheating at idle vs at speed
- fan-control and relay family differences
- cooling upgrade decision points

## D. Charging and electrical
### Stock baseline
- `vehicle/systems/electrical/`
- `vehicle/systems/charging-starting/`

### Work branches
- `work/maintenance/electrical/`
- `work/repairs/electrical/`
- `work/upgrades/electrical/`

### Diagnostics
- `diagnostics/charging-and-starting/`
- `diagnostics/body-electrical/`

### Sourcing
- `sourcing/interchange/electrical/`
- `sourcing/connectors/`

### Seed topics
- charging architecture by era
- grounds and distribution baselines
- battery/alternator/starter service routes
- low-voltage and parasitic-draw diagnostics
- body harness and door wiring issues
- connector family and replacement guidance

## E. Drivetrain
### Stock baseline
- `vehicle/systems/transmission/`
- `vehicle/systems/transfer-case/`
- `vehicle/configurations/`

### Work branches
- `work/maintenance/transmission/`
- `work/maintenance/driveline/`
- `work/repairs/transmission/`
- `work/repairs/driveline/`
- `work/upgrades/driveline/`
- `work/swaps/drivetrain/`

### Diagnostics
- `diagnostics/transmission/`
- `diagnostics/transfer-case/`
- `diagnostics/driveline/`

### Sourcing
- `sourcing/interchange/drivetrain/`
- `sourcing/donor-vehicles/drivetrain/`

### Seed topics
- AW4, manual, NP231, NP242 baselines
- fluid service and adjustment routes
- driveline vibration diagnosis
- SYE and driveshaft upgrade branches
- donor drivetrain choice planning

## F. Axles
### Stock baseline
- `vehicle/systems/axles/`
- `vehicle/interchange-baselines/axles/` when built out

### Work branches
- `work/maintenance/axles/`
- `work/repairs/axles/`
- `work/upgrades/axles/`
- `work/swaps/axles/`

### Diagnostics
- `diagnostics/driveline/`
- `diagnostics/steering-and-suspension/` when symptoms overlap

### Sourcing
- `sourcing/interchange/axles/`
- `sourcing/donor-vehicles/axles/`

### Seed topics
- Dana 30 and rear axle family baselines
- fluid and bearing service routes
- gear and brake-family differences
- donor axle selection
- swap-planning compatibility by width, brakes, and bolt pattern

## G. Steering
### Stock baseline
- `vehicle/systems/steering/`

### Work branches
- `work/maintenance/steering/`
- `work/repairs/steering/`
- `work/upgrades/steering/`
- `work/swaps/steering/`

### Diagnostics
- `diagnostics/steering-and-suspension/`

### Sourcing
- `sourcing/interchange/steering/`

### Seed topics
- box, linkage, and pump baselines
- common play/leak issues
- steering upgrade branches
- steering-box donor/interchange decisions
- geometry implications after suspension changes

## H. Suspension
### Stock baseline
- `vehicle/systems/suspension/`
- `vehicle/packages/up-country/` where needed

### Work branches
- `work/maintenance/suspension/`
- `work/repairs/suspension/`
- `work/restoration/suspension/`
- `work/upgrades/suspension/`

### Diagnostics
- `diagnostics/steering-and-suspension/`

### Sourcing
- `sourcing/interchange/suspension/`
- `sourcing/oem-vs-aftermarket/suspension/`

### Seed topics
- stock spring/shock/control-arm baselines
- sag, clunk, and geometry diagnostic routes
- Up Country differences
- common lift paths and their compatibility splits

## I. Brakes
### Stock baseline
- `vehicle/systems/brakes/`

### Work branches
- `work/maintenance/brakes/`
- `work/repairs/brakes/`
- `work/upgrades/brakes/`

### Diagnostics
- `diagnostics/brakes/`

### Sourcing
- `sourcing/interchange/brakes/`
- `sourcing/oem-vs-aftermarket/brakes/`

### Seed topics
- stock front/rear and ABS baselines
- fluid, pad, rotor, shoe, and bleed routes
- pull, fade, vibration, and soft-pedal diagnostics
- common upgrade families and donor decisions

## J. Body and interior
### Stock baseline
- `vehicle/systems/body/`
- `vehicle/systems/interior/`

### Work branches
- `work/repairs/body/`
- `work/repairs/interior/`
- `work/restoration/body/`
- `work/restoration/interior/`

### Diagnostics
- `diagnostics/body-and-interior/`
- `diagnostics/body-electrical/`

### Sourcing
- `sourcing/interchange/body/`
- `sourcing/interchange/interior/`

### Seed topics
- trim and fastening baselines
- door, hatch, window, seat, and headliner issues
- weather sealing and water ingress branches
- restoration-oriented trim recovery topics

## K. HVAC
### Stock baseline
- `vehicle/systems/hvac/`

### Work branches
- `work/maintenance/hvac/`
- `work/repairs/hvac/`
- `work/upgrades/hvac/`

### Diagnostics
- `diagnostics/hvac/` or folded into adjacent branches until dedicated scale exists

### Sourcing
- `sourcing/interchange/hvac/`
- `sourcing/oem-vs-aftermarket/hvac/`

### Seed topics
- heater and A/C architecture baselines
- vacuum-control and blend-door fault paths
- common service jobs
- compressor/core replacement planning

## L. Diagnostics as a first-class domain
### Domain routers
- `diagnostics/index.md`
- system branches listed in taxonomy

### Seed topics
- crank-no-start
- overheating
- low charging voltage
- brake pull/vibration
- driveline vibration
- steering wander and death-wobble-adjacent isolation
- fuel pressure and no-prime
- body electrical intermittent faults

## M. Maintenance schedules and procedures
### Primary branches
- `work/maintenance/engine/`
- `work/maintenance/fuel/`
- `work/maintenance/cooling/`
- `work/maintenance/electrical/`
- `work/maintenance/transmission/`
- `work/maintenance/driveline/`
- `work/maintenance/axles/`
- `work/maintenance/steering/`
- `work/maintenance/suspension/`
- `work/maintenance/brakes/`
- `work/maintenance/body/`
- `work/maintenance/interior/`
- `work/maintenance/hvac/`

### Seed topics
- baseline inspection schedules
- fluids and filters
- tune-up and wear-item service
- seasonal inspection routines
- post-purchase baseline service

## N. Modifications and upgrades
### Primary branches
- `work/upgrades/engine/`
- `work/upgrades/fuel/`
- `work/upgrades/cooling/`
- `work/upgrades/electrical/`
- `work/upgrades/driveline/`
- `work/upgrades/axles/`
- `work/upgrades/steering/`
- `work/upgrades/suspension/`
- `work/upgrades/brakes/`
- `work/upgrades/hvac/`
- `work/upgrades/body/` where justified

### Seed topics
- common reliability upgrades
- capacity or durability improvements
- brake and steering upgrade families
- suspension/lift geometry branches
- lighting and charging improvements

## O. Swaps and interchange
### Primary branches
- current `swap/` for ECU execution during transition
- `work/swaps/drivetrain/`
- `work/swaps/axles/`
- `work/swaps/steering/`
- future `work/swaps/ecu/`
- `sourcing/interchange/`
- `sourcing/donor-vehicles/`

### Seed topics
- donor-family planning
- branch-level compatibility files
- common axle/drivetrain swap planning
- connector and harness interchange
- stock interchange baselines vs sourcing advice split

---

# 5. Cross-cutting roadmap rules

## Year and era truth comes first in stock baselines
When a branch depends heavily on year splits, seed supporting baseline files in `vehicle/` first or in parallel.

## Diagnostics should reference, not replace, repair content
Diagnostic seeds should point to the likely repair branch but remain symptom-first.

## Sourcing should grow where wrong-part risk is high
Prioritize sourcing branches for:
- brake families
- axle donors
- electrical connectors
- drivetrain donors
- wear items with meaningful OEM vs aftermarket tradeoffs

## Restoration should seed where decay is common
Prioritize restoration branches for:
- headliners
- seats and trim
- weather sealing
- interior plastics and mounting failures
- body corrosion and water intrusion workflows

---

# 6. Suggested next-wave backlog seeds

These are roadmap-level seed candidates, not deep research assignments.

## Wave 1
- domain routers for `work/`, `diagnostics/`, and `sourcing/`
- `vehicle/systems/` branch skeleton for major systems
- maintenance branch skeleton across major systems
- top diagnostic symptom routers
- common interchange branch skeleton

## Wave 2
- cooling, brakes, charging-starting, and fuel baseline packages
- common maintenance procedures for fluids, filters, tune-up, and inspections
- high-frequency diagnostics: no-start, overheating, low voltage, brake issues, driveline vibration
- basic sourcing/interchange pages for brakes, axles, electrical, and drivetrain

## Wave 3
- steering and suspension upgrade branches
- axle family baselines and donor comparison branches
- body/interior repair and restoration starters
- HVAC baseline and common fault branches
- drivetrain maintenance and driveline upgrade branches

## Wave 4
- deeper package/year exceptions
- advanced restoration packages
- expanded drivetrain and axle swap planning
- broader upgrade comparison matrices
- migration of ECU swap material toward future `work/swaps/ecu/` once the destination tree is ready

---

# 7. Roadmap maintenance rules

Review the roadmap when:
- a major domain router is added
- a coverage audit changes platform priorities
- repeated user demand shifts the next wave
- evidence availability changes sharply
- migration makes a target branch stable enough to become canonical

When updating this roadmap:
- keep it structural
- avoid turning it into a full technical outline
- point backlog candidates at narrow destinations
- preserve the distinction between roadmap and canon

---

# 8. Summary

The coverage roadmap should expand the repo in layers:
- first, durable branches and routers
- next, broad operational coverage
- then, common upgrades and interchange
- finally, deeper diagnostics, restoration, and specialized swaps

That sequence gives the repo platform-wide usefulness without sacrificing structure or letting any one legacy branch distort future growth.
