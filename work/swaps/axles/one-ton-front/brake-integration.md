# Front Brake Integration — Dana 60

Brake setup, line routing, and master cylinder considerations for XJ Cherokee builds running a 2005+ Super Duty Dana 60 front axle.

---

## Retaining the Super Duty disc brakes

The 05+ Super Duty Dana 60 comes with large vented disc brakes that are dramatically stronger than any stock XJ front brake setup. **Retain the donor brakes** — there is no practical reason to downsize.

### Donor brake components to retain
- Rotors (vented, significantly larger than XJ rotors)
- Calipers (dual-piston or single-piston depending on donor year)
- Caliper brackets (bolt to the knuckle)
- Brake pads (use Super Duty pads, not XJ pads)

### After housing narrowing
If the housing was narrowed (see [`housing-prep.md`](housing-prep.md)), verify that:
- The caliper brackets still bolt to the knuckles correctly (narrowing affects the outer tube stubs where the knuckles mount, but the knuckle-to-bracket interface is unchanged)
- The rotors spin freely without contacting the caliper body or bracket
- The caliper clears the inside of the wheel at the new backspacing

## Brake line routing

The donor brake lines will not match XJ frame routing. New lines must be fabricated or sourced.

### Hard lines
- Run from the XJ's master cylinder / proportioning valve along the frame rail to flexible hose connections near each front wheel
- Use 3/16" double-flared steel brake line (DOT standard)
- Route along the existing XJ frame rail brake line path where possible
- Secure with brake line clips to prevent vibration fatigue and trail damage

### Flexible hoses
- Connect from the frame-mounted hard line to the caliper on the moving axle
- Must be long enough to handle full suspension droop without stretching
- Must not bind or kink at full compression
- Use DOT-approved braided stainless steel hoses for durability (preferred over rubber on trail rigs)
- Thread fittings: verify the Super Duty caliper banjo fitting size matches your hose ends (adapter fittings are available if needed)

### Fitting sizes
- Super Duty calipers may use metric banjo fittings
- XJ master cylinder and hard lines are typically SAE (3/16" inverted flare)
- Adapter fittings or custom hose assemblies bridge the difference
- Verify before ordering hoses — measure the caliper inlet fitting

## Master cylinder considerations

The Super Duty disc brakes have significantly larger caliper piston(s) than stock XJ brakes. This means:
- More fluid volume is needed per brake application to move the larger pistons
- The stock XJ master cylinder may feel soft or have excessive pedal travel with one-ton brakes

### Options
- **Stock XJ master cylinder** — may work adequately if only the front axle is upgraded. Pedal feel will be softer than stock.
- **Larger master cylinder** — a WJ Grand Cherokee or similar master cylinder with larger bore provides more fluid displacement per stroke. Improves pedal feel but reduces mechanical advantage (more pedal effort).
- **Adjustable proportioning valve** — if both front and rear axles are upgraded to large discs, an adjustable proportioning valve allows tuning the front/rear brake bias. The stock XJ proportioning is calibrated for small front discs and rear drums — it will not be correct for one-ton disc brakes on both ends.

**Most one-ton XJ builds with Dana 60 front + Sterling rear:** upgrade the master cylinder and add an adjustable proportioning valve. This combination provides correct pedal feel and allows tuning bias for the specific brake setup.

## ABS considerations

- The stock XJ ABS system will not work with the Dana 60 — the tone ring, sensor mounting, and controller are all incompatible
- Most one-ton XJ builds **delete ABS entirely** — remove the ABS module and run a simple manual proportioning valve
- If ABS is desired, aftermarket standalone ABS systems exist but add significant cost and complexity

## Brake bleeding

After installation, the entire brake system must be bled:
1. Start at the wheel furthest from the master cylinder (typically right rear)
2. Move to left rear, right front, left front
3. Verify firm pedal with no sponginess
4. Check all connections for leaks under pedal pressure

---

## Related
- Front housing preparation: [`housing-prep.md`](housing-prep.md)
- Rear brakes and e-brake: [`../one-ton-rear/brake-and-ebrake.md`](../one-ton-rear/brake-and-ebrake.md)
- Steering conversion (shared knuckle): [`steering-conversion.md`](steering-conversion.md)
