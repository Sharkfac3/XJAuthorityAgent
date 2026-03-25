# Rear Brakes and Emergency Brake — Sterling 10.50

Disc brake retention, e-brake integration, and proportioning for a 2005+ Super Duty Sterling 10.50 rear axle under a Jeep Cherokee XJ.

---

## Retaining the Sterling disc brakes

The Sterling 10.50 comes with large disc brakes from the Super Duty. Retain them — they are a massive upgrade over any stock XJ rear brake option.

### Components to retain
- Rotors (vented discs, with drum-in-hat center section on full-float models)
- Calipers and caliper brackets
- Brake pads (use Super Duty pads)

### After housing narrowing
If the housing was narrowed (see [`housing-prep.md`](housing-prep.md)):
- The caliper brackets bolt to the hub/spindle assembly, not the housing tube — so narrowing does not directly affect caliper mounting
- Verify rotor-to-caliper clearance after re-assembling the shortened axle
- Check that the caliper clears the inside of the wheel at the chosen backspacing

## Brake line routing

The donor brake lines will not match XJ frame geometry. Fabricate new lines.

### Hard lines
- Run from the XJ proportioning valve along the rear frame rail to flexible hose connections near each rear wheel
- 3/16" double-flared steel brake line (DOT standard)
- Route along the existing XJ rear brake line path where possible

### Flexible hoses
- Connect from the frame-mounted hard line to each rear caliper
- Must accommodate full suspension droop without stretching and full compression without kinking
- Braided stainless steel hoses recommended for durability

### Fitting compatibility
- Sterling calipers may use metric banjo fittings
- XJ hard lines are typically SAE
- Verify before ordering — adapter fittings are available

## Emergency brake (e-brake)

### How the Sterling e-brake works

Full-float Sterling 10.50 rear axles from 05+ Super Dutys use a **drum-in-hat** e-brake design:
- The disc brake rotor has a drum surface cast into its center hat section
- Small brake shoes sit inside this drum, behind the rotor
- The shoes are actuated mechanically by cables, not by the hydraulic brake circuit
- When the e-brake lever is pulled, the cables pull the shoe actuator, which expands the shoes against the drum surface

This system is completely separate from the main hydraulic disc brakes.

### XJ integration challenges

1. **Cable routing** — the Super Duty e-brake cables are routed for the F-250/F-350 frame and cabin. They will not fit the XJ.
2. **Cable length** — XJ wheelbase is much shorter than the Super Duty. The cables are too long.
3. **Lever connection** — the XJ e-brake lever uses a different cable interface than the Super Duty.

### Solutions

| Approach | Complexity | Notes |
|----------|-----------|-------|
| Custom e-brake cables | Moderate | Have a brake cable shop fabricate cables to XJ length and fitting dimensions. Most reliable solution. |
| Aftermarket e-brake cable kit | Low | Some off-road fab companies sell e-brake cable kits for common one-ton swaps. Check current availability. |
| Universal e-brake cables | Low–Moderate | Off-the-shelf universal cables with adjustable fittings. May require adapter brackets at the axle and cabin ends. |
| Delete e-brake | Minimal | Remove e-brake hardware entirely. **Not legal for street use in most states. Not recommended.** |

### Cable routing on the XJ
- Route the cables from the drum-in-hat mechanisms along the rear axle housing
- Run along the XJ frame rail (inside or alongside the frame) toward the cabin
- Enter the cabin through the stock XJ e-brake cable passage (or drill a new passage with a grommet)
- Connect to the XJ e-brake lever mechanism

### Adjustment
- After installation, adjust cable tension so that the e-brake holds the vehicle on a moderate grade with the lever 3–5 clicks from rest
- Verify that the e-brake fully releases — dragging shoes will overheat the drum-in-hat and damage the rotor

## Proportioning

With large disc brakes on both front and rear axles, the stock XJ proportioning valve is incorrect. It was calibrated for small front discs and rear drums.

### Options
- **Adjustable proportioning valve** — install in-line on the rear brake circuit. Allows tuning the front/rear bias on the vehicle. Start with more rear bias than stock (since the rear brakes are now much larger) and adjust based on brake feel and lock-up behavior.
- **Residual pressure valve** — may be needed if the rear calipers do not retract properly (disc brake calipers prefer zero residual pressure in the line when the pedal is released).

### Master cylinder
If the front brakes are also upgraded (Dana 60 discs), the master cylinder likely needs upsizing — see [`../one-ton-front/brake-integration.md`](../one-ton-front/brake-integration.md) for details.

---

## Related
- Rear housing preparation: [`housing-prep.md`](housing-prep.md)
- Front brake integration: [`../one-ton-front/brake-integration.md`](../one-ton-front/brake-integration.md)
- Master cylinder and proportioning: [`../one-ton-front/brake-integration.md`](../one-ton-front/brake-integration.md)
