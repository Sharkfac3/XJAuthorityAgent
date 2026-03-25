# Fitment: Super Duty Dana 60 Front → XJ Cherokee

Dimensional comparison and fitment decision guide for installing a 2005+ Ford Super Duty Dana 60 front axle under a Jeep Cherokee XJ.

For donor identification, see: [`../../donor-vehicles/axles/ford-super-duty-dana-60.md`](../../donor-vehicles/axles/ford-super-duty-dana-60.md)
For stock XJ baseline specs, see: [`../../../vehicle/systems/axles/stock-specs.md`](../../../vehicle/systems/axles/stock-specs.md)

---

## Dimensional comparison

| Spec | XJ Dana 30 (stock) | Super Duty Dana 60 (SRW) | Delta |
|------|-------------------|--------------------------|-------|
| Housing width (WMS-to-WMS) | ~57.2" | ~71" | **+13.8"** (~7" per side) |
| Axle tube OD | 2.5" | 3.5" | +1.0" |
| Ring gear diameter | 7.125" | 9.75" | +2.625" |
| Spline count | 27 | 35 (outer), 30 (inner) | Significant upgrade |
| U-joint size | 260/297 | 1480 (outer) | Major upgrade |
| Bolt pattern | 5 on 4.5" | 8 on 170mm | **Different — requires new wheels** |
| Spring type (donor) | Leaf | Coil | **Coil buckets must be removed** |
| Steering | Y-link | Radius arm | **Radius arm mounts cut off; crossover steering required** |
| Approximate weight | ~180 lb | ~350 lb | **+170 lb** |

## Critical fitment issues

### 1. Width — narrowing is mandatory

The Super Duty Dana 60 is ~14" wider than the stock XJ Dana 30. This is the single biggest fitment challenge.

**Options:**
- **Cut-and-turn the inner C** — the most common approach. The inner C (center section housing ears where the tubes press in) is cut, the tubes are shortened, and the inner C is re-welded at the correct width. Requires a competent welder and precise measurement. Target width is typically 60–64" WMS depending on tire width and fender clearance goals.
- **Aftermarket truss kit** — companies sell bolt-in or weld-in truss kits for the Dana 60 that include pre-cut tubes at common widths. Stronger than a bare cut-and-turn but more expensive.
- **Aftermarket narrowed housing** — buy a complete housing already narrowed to XJ width. Most expensive option but eliminates fabrication risk.

**Narrowing affects:** axle shaft length (shafts must be shortened or custom-ordered), driveshaft angle, and steering geometry. All downstream decisions depend on final housing width.

### 2. Coil-to-leaf conversion

The Super Duty Dana 60 is a coil-spring axle. The XJ uses leaf springs.

**Required work:**
- Remove the coil spring buckets from the top of the housing tubes (cut and grind)
- Remove the radius arm mounts from the bottom of the tubes (cut and grind)
- Weld leaf spring perches to the top of the tubes at the correct width and spacing for XJ leaf springs
- Set center pin location to establish correct pinion angle and axle centering

See: [`../../../work/swaps/axles/one-ton-front/spring-perch-relocation.md`](../../../work/swaps/axles/one-ton-front/spring-perch-relocation.md)

### 3. Steering — crossover conversion mandatory

The stock XJ Y-link steering geometry cannot work with a Dana 60. The knuckle steering arms are in a completely different location and the drag link angles are wrong.

**Required:**
- High-steer arms (bolt to the top of the Dana 60 knuckles — aftermarket, widely available for ball-joint 60s)
- Crossover steering layout: drag link runs from the pitman arm across to the passenger-side knuckle, tie rod connects between the two knuckles at the top
- Track bar relocation to match the new axle center height
- Possible steering box upgrade or ram-assist hydraulic steering for the added weight and larger tires

See: [`../../../work/swaps/axles/one-ton-front/steering-conversion.md`](../../../work/swaps/axles/one-ton-front/steering-conversion.md)

### 4. Hubs and wheel bolt pattern

The Dana 60 uses an 8-on-170mm bolt pattern. Stock XJ is 5-on-4.5".

**This means:**
- All four wheels must be replaced with 8-lug wheels (or the rear must also be an 8-lug axle — the Sterling 10.50 matches)
- Unit bearing hubs from the donor are retained — no conversion needed
- Wheel spacers can adjust backspacing but do not change the bolt pattern

### 5. Brakes

Super Duty Dana 60 disc brakes are significantly larger than stock XJ brakes.

**Considerations:**
- Retaining the donor disc brakes is standard practice — they are much stronger than anything the XJ had
- Brake line routing must be fabricated for XJ frame
- Master cylinder may need upsizing to handle the larger caliper piston volume (especially if the rear is also upgraded to large discs)
- Proportioning valve adjustment is likely needed to balance front/rear bias

See: [`../../../work/swaps/axles/one-ton-front/brake-integration.md`](../../../work/swaps/axles/one-ton-front/brake-integration.md)

### 6. Differential and carrier

The Dana 60 uses a removable carrier (drop-out third member on some, standard carrier on others depending on ratio).

**Carrier break:**
- Dana 60 has a carrier break at approximately 4.10 — ratios 4.10 and numerically lower use one carrier, ratios steeper than 4.10 use a different carrier
- When re-gearing, verify you have the correct carrier for your target ratio
- Locker options: ARB air locker, Detroit locker, Eaton E-locker, lunchbox lockers — all widely available for the Dana 60

### 7. Weight

The Dana 60 assembly weighs roughly 170 lb more than the stock Dana 30. This adds unsprung weight to the front, which affects:
- Ride quality (harsher on-road)
- Spring rate requirements (stiffer springs needed)
- Steering effort (heavier components to turn)
- Shock valving requirements

This is accepted as a trade-off in one-ton builds. The XJ frame and body are light enough that the weight penalty is manageable with proper spring and shock selection.

## Lift height requirement

A one-ton Dana 60 front axle swap generally requires **6" of lift minimum** to clear the housing under the XJ frame and provide adequate suspension travel. Many builders run 7–8" for better clearance with 37–40" tires.

See: [`../../../work/swaps/axles/support-work/lift-and-clearance.md`](../../../work/swaps/axles/support-work/lift-and-clearance.md)
