# Axle Swaps Index

## Purpose
Route axle-family swap projects and fitment workflows for the Jeep Cherokee XJ.

Use this branch when the main question is how to plan, source, prepare, install, or validate an axle swap on an XJ.

## Do not start here when
- the question is mainly about stock factory axle configuration → [`../../../vehicle/systems/axles/overview.md`](../../../vehicle/systems/axles/overview.md)
- the question is mainly about non-axle job execution → [`../../index.md`](../../index.md)
- the question is mainly about symptom diagnosis → [`../../../diagnostics/index.md`](../../../diagnostics/index.md)
- the question is mainly about donor/part selection with no execution focus → [`../../../sourcing/interchange/axles/index.md`](../../../sourcing/interchange/axles/index.md)

## How to use this index
1. Identify what class of axle swap (half-ton upgrade or one-ton conversion).
2. Enter the stage that matches the current decision or task.
3. Pull in `vehicle/`, `sourcing/`, or `diagnostics/` files only where the swap decision depends on them.

---

## One-Ton Swap Workflow — 2005+ Ford Super Duty

Dana 60 front / Sterling 10.50 rear. The staged workflow below walks through the full one-ton conversion.

### Stage 0 — Prerequisite reading
Before beginning a swap project, confirm your current axle configuration:
- Axle identification guide: [`../../../vehicle/systems/axles/identification.md`](../../../vehicle/systems/axles/identification.md)
- Gear ratio identification: [`../../../vehicle/systems/axles/gear-ratio-identification.md`](../../../vehicle/systems/axles/gear-ratio-identification.md)

### Stage 1 — Understand the stock baseline
Load:
- [`../../../vehicle/systems/axles/overview.md`](../../../vehicle/systems/axles/overview.md)
- [`../../../vehicle/systems/axles/stock-specs.md`](../../../vehicle/systems/axles/stock-specs.md)

Use this stage to answer:
- What axles does the XJ currently have?
- What are the dimensional baselines the swap must work against?
- What wheel bolt pattern, gear ratio, and shaft specs are being replaced?

### Stage 2 — Select the donor axles
Load:
- [`../../../sourcing/donor-vehicles/axles/ford-super-duty-dana-60.md`](../../../sourcing/donor-vehicles/axles/ford-super-duty-dana-60.md)
- [`../../../sourcing/donor-vehicles/axles/ford-super-duty-sterling-10-50.md`](../../../sourcing/donor-vehicles/axles/ford-super-duty-sterling-10-50.md)

Use this stage to answer:
- Which model years and trims to target?
- SRW vs DRW — which to pull?
- What components to grab from the donor?
- How to identify the right axle at the junkyard?

### Stage 3 — Evaluate fitment and dimensional decisions
Load:
- [`../../../sourcing/interchange/axles/super-duty-dana-60-fitment.md`](../../../sourcing/interchange/axles/super-duty-dana-60-fitment.md)
- [`../../../sourcing/interchange/axles/super-duty-sterling-fitment.md`](../../../sourcing/interchange/axles/super-duty-sterling-fitment.md)
- [`../../../sourcing/interchange/axles/one-ton-gearing.md`](../../../sourcing/interchange/axles/one-ton-gearing.md)
- [`../../../sourcing/interchange/axles/one-ton-driveshaft-specs.md`](../../../sourcing/interchange/axles/one-ton-driveshaft-specs.md)

Use this stage to answer:
- How much wider is the donor than the XJ? How much narrowing?
- What steering conversion is needed?
- What gear ratio for the intended tire size?
- What U-joint series and driveshaft configuration?
- What brakes, hubs, and wheel changes are required?

### Stage 4 — Plan lift and clearance
Load:
- [`support-work/lift-and-clearance.md`](support-work/lift-and-clearance.md)

Use this stage to answer:
- What minimum lift height is needed?
- What fender work is required for the tire size?
- What are the driveline angle limits?
- Where do bump stops go?

### Stage 5 — Execute front axle swap
Load:
- [`one-ton-front/index.md`](one-ton-front/index.md)
- Relevant leaves as needed:
  - [`one-ton-front/housing-prep.md`](one-ton-front/housing-prep.md)
  - [`one-ton-front/spring-perch-relocation.md`](one-ton-front/spring-perch-relocation.md)
  - [`one-ton-front/steering-conversion.md`](one-ton-front/steering-conversion.md)
  - [`one-ton-front/brake-integration.md`](one-ton-front/brake-integration.md)
  - [`one-ton-front/mounting-and-brackets.md`](one-ton-front/mounting-and-brackets.md)

### Stage 6 — Execute rear axle swap
Load:
- [`one-ton-rear/index.md`](one-ton-rear/index.md)
- Relevant leaves as needed:
  - [`one-ton-rear/housing-prep.md`](one-ton-rear/housing-prep.md)
  - [`one-ton-rear/spring-perch-welding.md`](one-ton-rear/spring-perch-welding.md)
  - [`one-ton-rear/brake-and-ebrake.md`](one-ton-rear/brake-and-ebrake.md)
  - [`one-ton-rear/mounting-and-brackets.md`](one-ton-rear/mounting-and-brackets.md)

### Stage 7 — Support work (driveshafts, gearing, validation)
Load:
- [`support-work/index.md`](support-work/index.md)
- Relevant leaves as needed:
  - [`support-work/driveshaft-work.md`](support-work/driveshaft-work.md)
  - [`support-work/gearing-install.md`](support-work/gearing-install.md)

---

## Branch routers
- Front axle swap → [`one-ton-front/index.md`](one-ton-front/index.md)
- Rear axle swap → [`one-ton-rear/index.md`](one-ton-rear/index.md)
- Support work (driveshafts, gearing, lift) → [`support-work/index.md`](support-work/index.md)

## Boundary links
- Stock axle baseline: [`../../../vehicle/systems/axles/overview.md`](../../../vehicle/systems/axles/overview.md)
- Dana 30 front axle detail: [`../../../vehicle/systems/axles/dana30-front.md`](../../../vehicle/systems/axles/dana30-front.md)
- Dana 35 rear axle detail: [`../../../vehicle/systems/axles/dana35-rear.md`](../../../vehicle/systems/axles/dana35-rear.md)
- Chrysler 8.25 rear axle detail: [`../../../vehicle/systems/axles/chrysler-825-rear.md`](../../../vehicle/systems/axles/chrysler-825-rear.md)
- Donor vehicle identification: [`../../../sourcing/donor-vehicles/axles/index.md`](../../../sourcing/donor-vehicles/axles/index.md)
- Interchange and fitment decisions: [`../../../sourcing/interchange/axles/index.md`](../../../sourcing/interchange/axles/index.md)
- Axle identification guide: [`../../../vehicle/systems/axles/identification.md`](../../../vehicle/systems/axles/identification.md)
- Gear ratio identification: [`../../../vehicle/systems/axles/gear-ratio-identification.md`](../../../vehicle/systems/axles/gear-ratio-identification.md)
- Locker and LSD options: [`../../../vehicle/systems/axles/locker-options.md`](../../../vehicle/systems/axles/locker-options.md)
- Inspections (pre-swap): [`../../inspections/pre-swap/index.md`](../../inspections/pre-swap/index.md)
