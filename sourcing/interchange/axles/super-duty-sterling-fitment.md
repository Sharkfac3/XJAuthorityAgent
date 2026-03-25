# Fitment: Super Duty Sterling 10.50 Rear → XJ Cherokee

Dimensional comparison and fitment decision guide for installing a 2005+ Ford Super Duty Sterling 10.50 rear axle under a Jeep Cherokee XJ.

For donor identification, see: [`../../donor-vehicles/axles/ford-super-duty-sterling-10-50.md`](../../donor-vehicles/axles/ford-super-duty-sterling-10-50.md)
For stock XJ baseline specs, see: [`../../../vehicle/systems/axles/stock-specs.md`](../../../vehicle/systems/axles/stock-specs.md)

---

## Dimensional comparison

| Spec | XJ Chrysler 8.25 (stock) | Sterling 10.50 (SRW) | Delta |
|------|-------------------------|----------------------|-------|
| Housing width (WMS-to-WMS) | ~58.5" | ~66" | **+7.5"** (~3.75" per side) |
| Axle tube OD | 3.0" | 3.5" | +0.5" |
| Ring gear diameter | 8.25" | 10.50" | +2.25" |
| Spline count | 29 | 35 | Upgrade |
| Axle type | Semi-float | Full-float | **Upgrade — see notes** |
| Bolt pattern | 5 on 4.5" | 8 on 170mm | **Different — matches Dana 60 front** |
| Spring type (XJ) | Leaf | — | Perches must be welded to Sterling housing |
| Approximate weight | ~170 lb | ~300 lb | **+130 lb** |

## Critical fitment issues

### 1. Width — narrowing required

The Sterling 10.50 SRW is ~7.5" wider than the stock XJ rear. Less extreme than the front Dana 60 but still requires narrowing.

**Options:**
- **Cut and re-weld tubes** — cut the axle tubes to the desired width, re-weld the tube ends with new bearing surfaces. Axle shafts must be shortened to match. Target width is typically 58–62" WMS depending on tire size and fender clearance.
- **Aftermarket narrowed housing** — available from specialty shops, pre-built to common widths.
- **Run it wide** — some builders with wide fenders or tube fenders skip narrowing and run the full SRW width. Only viable with significant fender modification.

**Key difference from the front:** the rear narrowing is simpler because there are no steering knuckles or inner C geometry to worry about. It's a straight tube cut and re-weld.

### 2. Spring perch welding

The Sterling housing has no leaf spring perches from the factory (Super Duty rear suspension varies by year — some leaf, some coil with links). Regardless, the donor perches will not match XJ leaf spring geometry.

**Required work:**
- Weld spring perches to the housing tubes at XJ leaf spring width (~42" center-to-center) and correct fore-aft position
- Set center pin location to establish correct pinion angle
- Pinion angle target: typically 2–3 degrees down from the transfer case output angle (varies with lift height)

See: [`../../../work/swaps/axles/one-ton-rear/spring-perch-welding.md`](../../../work/swaps/axles/one-ton-rear/spring-perch-welding.md)

### 3. Full-float hub clearance

Full-float hubs stand proud of the axle tube end by several inches. This affects:
- **Inner fender clearance** — the hub protrudes further inboard than a semi-float axle. Verify clearance with the XJ fender well, especially after narrowing.
- **Wheel backspacing** — the hub face is further outboard, which changes the effective backspacing. Wheel selection must account for this.
- **Tire-to-frame clearance** — at full lock and full stuff (compression), the tire + hub + caliper stack must not contact the XJ frame rail.

### 4. Brakes

The Sterling 10.50 comes with large disc brakes from the Super Duty.

**Considerations:**
- Retain the donor disc brakes — they are a major upgrade over stock XJ drums or small discs
- Caliper brackets may need re-clocking or modification after housing narrowing
- Brake line routing must be fabricated for the XJ frame and body

### 5. Emergency brake (e-brake)

This is one of the trickier integration points for the rear axle swap.

**Full-float Sterling e-brake design:**
- Uses a **drum-in-hat** design — a small drum brake assembly is built into the rear rotor hat (the center section of the disc rotor)
- The drum-in-hat e-brake is actuated by cables, not the hydraulic brake circuit
- The drum shoes and hardware live inside the rotor hat and actuate against a small drum surface cast into the rotor center

**XJ integration:**
- The e-brake cables from the donor will not match XJ routing — custom cables or cable fabrication is required
- The cable must route from the drum-in-hat mechanism, along the XJ frame, to the XJ e-brake lever in the cabin
- Some builders skip the e-brake entirely (not legal for street use in most states)
- Aftermarket e-brake cable kits exist for common one-ton swap configurations

See: [`../../../work/swaps/axles/one-ton-rear/brake-and-ebrake.md`](../../../work/swaps/axles/one-ton-rear/brake-and-ebrake.md)

### 6. Differential and carrier

**Carrier break:**
- Sterling 10.50 carrier break is at approximately 3.73 — ratios 3.73 and numerically lower use one carrier, ratios steeper than 3.73 use a different carrier
- When re-gearing to 4.56+, you need the high-ratio carrier
- Locker options: ARB air locker, Detroit locker, Eaton E-locker — available but fewer options than the Dana 60 market

### 7. Pinion yoke / flange

The Sterling 10.50 uses a pinion flange (not a yoke) on most configurations.

- **1410-series U-joint** at the pinion end is common
- Driveshaft must be built to match — see [`one-ton-driveshaft-specs.md`](one-ton-driveshaft-specs.md)
- Flange bolt pattern must match or an adapter flange is needed

### 8. Weight

The Sterling assembly adds ~130 lb of unsprung weight over the stock XJ rear. Impacts:
- Rear spring rate requirements (heavier springs or add-a-leafs)
- Shock valving
- Ride quality on-road

## Lift height requirement

The Sterling 10.50 is a larger-diameter housing than any stock XJ rear axle. Combined with full-float hubs and larger brakes, a minimum of **6" lift** is generally required. Most one-ton XJ builds run 7–8" for clearance with 37–40" tires.

See: [`../../../work/swaps/axles/support-work/lift-and-clearance.md`](../../../work/swaps/axles/support-work/lift-and-clearance.md)
