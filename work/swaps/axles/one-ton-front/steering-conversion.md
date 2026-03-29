# Front Steering Conversion — Dana 60

High-steer, crossover steering, and hydraulic assist configuration for XJ Cherokee builds running a 2005+ Super Duty Dana 60 front axle.

---

## Why stock XJ steering cannot work

The stock XJ uses a Y-link steering layout: a drag link from the pitman arm to one knuckle, and a tie rod connecting the two knuckles below the axle. This geometry is designed for the Dana 30's knuckle steering arm position and axle height.

With a Dana 60:
- The knuckle steering arms are in a different position (higher, further outboard)
- The axle sits higher under the XJ due to the larger housing
- The tie rod running below a Dana 60 would hang dangerously low and be vulnerable to trail damage
- The drag link angles would be wrong, causing bump steer and wandering

**Crossover steering with high-steer arms is the standard solution for Dana 60 XJ builds.**

## Crossover steering layout

### Components
1. **High-steer arms** — bolt to the top of the Dana 60 ball-joint knuckles (aftermarket, widely available for 05+ Super Duty Dana 60). These move the steering attachment point from the stock knuckle arm location to the top of the knuckle.
2. **Tie rod** — connects the two high-steer arms across the front of the axle, running above the axle tubes. Typically 7/8" or 1" chromoly DOM tube with high-misalignment heim joints or heavy tie rod ends.
3. **Drag link** — runs from the pitman arm (on the XJ steering box) across to the passenger-side high-steer arm. This is the main steering input link.
4. **Track bar** — relocated to connect from the XJ frame to the axle housing, keeping the axle centered side-to-side. Stock XJ track bar location will not work with the new axle height.

### Geometry
```
[Pitman arm] ---drag link---> [Passenger knuckle (high-steer arm)]
                                        |
                                     tie rod
                                        |
                              [Driver knuckle (high-steer arm)]
```

The drag link runs roughly parallel to the axle, from the steering box side of the XJ frame to the passenger-side knuckle. The tie rod connects both knuckles above the axle.

## High-steer arm selection

For 05+ Super Duty ball-joint Dana 60 knuckles:
- **Reid Racing** — billet aluminum, well-proven, multiple configurations
- **PSC Motorsports** — steel, built for hydraulic assist integration
- **Synergy Manufacturing** — steel, popular in the full-size Jeep community
- **DIY / custom fabricated** — some builders weld their own arms. Requires knowledge of steering geometry and taper fit to the knuckle.

**Key specification:** the arm must bolt to the 05+ Super Duty ball-joint knuckle (not kingpin knuckles from older Dana 60s). Verify compatibility before ordering.

## Tie rod and drag link construction

### Material
- 7/8" x 0.188" wall or 1" x 0.188" wall DOM chromoly tube is standard
- Heim joints (rod ends) at each end with high-misalignment inserts to handle steering geometry arc
- Alternatively: forged tie rod ends with tapered studs for the high-steer arm taper

### Sizing
- Tie rod length is determined by the distance between the two high-steer arms at center (straight-ahead) steering position
- Drag link length is determined by the distance from the pitman arm to the passenger-side high-steer arm
- Both must be adjustable (threaded rod ends with jam nuts) for toe alignment

### Strength
- The tie rod and drag link on a one-ton XJ build see significantly more force than stock XJ steering components
- Under-built links are the most common failure point in one-ton XJ steering
- 1" DOM tube is recommended for 37"+ tires. 7/8" is marginal for 40" tires.

## Track bar relocation

The stock XJ track bar connects from the driver-side frame rail to the axle housing. With a Dana 60:
- The axle is higher (larger housing + more lift), changing the track bar angle
- The attachment point on the axle housing must be fabricated (weld-on bracket)
- The frame-side mount may need a drop bracket to correct the track bar angle

**Track bar angle goal:** as close to horizontal as possible at ride height. Steep track bar angles cause lateral axle shift during compression and droop (the axle moves side-to-side as the suspension cycles).

## Hydraulic assist / ram assist steering

With 37–40" tires on a Dana 60, the XJ's stock steering box may struggle to turn the wheels, especially:
- At low speed (parking lots, tight trail maneuvers)
- In mud, sand, or rocky terrain where tire resistance is high
- With lower tire pressures (aired down for trail use)

### Options

| System | Description | Complexity |
|--------|-------------|-----------|
| Stock XJ steering box | Adequate for 35", marginal for 37", struggles with 40" | No additional work |
| High-flow power steering pump | Increases assist from the stock box. Ford 351 PS pump is a common junkyard swap. | Moderate — pump bracket fabrication |
| Hydraulic ram assist | A hydraulic cylinder mounted to the axle and tie rod, powered by the PS pump. Provides direct assist to the steering linkage. | Significant — plumbing, cylinder mounting, valve integration |
| Full hydraulic steering | Replaces the mechanical steering box entirely with hydraulic cylinders. No mechanical link between the steering wheel and wheels. | Major — requires orbital valve, dedicated pump, and full plumbing |

**Most common for one-ton XJ builds:** stock or upgraded steering box + hydraulic ram assist. Full hydraulic steering is typically reserved for competition or extreme builds.

### Ram assist mounting
- The hydraulic cylinder mounts between a fixed point on the axle housing and the tie rod (or drag link)
- PSC Motorsports is the most popular brand for Jeep ram assist kits
- The cylinder must be sized for the steering force required — larger tires need more force
- Plumbing ties into the power steering system via a flow control valve

## Common mistakes

- **Drag link and track bar not parallel** — if these two links are not roughly parallel and similar length, the axle shifts side-to-side when the steering is turned (bump steer). This is the #1 geometry mistake in crossover steering conversions.
- **Tie rod too low** — the tie rod should run above the axle housing. A low tie rod gets hit by rocks and trail obstacles.
- **Under-built links** — using thin-wall tube or small heim joints on 37"+ tires. The steering linkage is a high-stress component.
- **No adjustability** — tie rod and drag link must be adjustable for toe setting. Fixed-length links cannot be aligned.

---

## Related
- High-steer arm fitment depends on knuckle: [`../../../../sourcing/donor-vehicles/axles/ford-super-duty-dana-60.md`](../../../../sourcing/donor-vehicles/axles/ford-super-duty-dana-60.md)
- Brake integration (shared knuckle): [`brake-integration.md`](brake-integration.md)
- Mounting and brackets: [`mounting-and-brackets.md`](mounting-and-brackets.md)
