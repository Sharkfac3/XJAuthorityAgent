# Brake Pedal Feel

## Purpose
Fault-isolate abnormal brake pedal feel: spongy, soft, slow-sinking, hard, or fading pedal. Distinguish master cylinder problems from air in the system from power brake booster failure.

## Symptom definition
Use this leaf when the brake pedal does not feel right:
- Spongy or springy resistance instead of firm pressure
- Pedal sinks slowly to the floor when held
- Pedal feels unusually hard or requires excessive foot pressure
- Normal feel for the first stop, then fading feel on repeated applications

## Do not use this leaf when
- The main complaint is brake pull to one side → brake imbalance diagnosis (not covered in this leaf)
- The main complaint is pulsation or vibration during braking → brake rotor and caliper flatness issue
- Rear drums feel correct but overall pedal travel is long → [`rear-drum-issues.md`](rear-drum-issues.md) — rear drums may be out of adjustment

---

## Symptom isolation guide

### Spongy or soft pedal — most likely air in the system

A spongy pedal that compresses like a spring instead of building firm resistance is the classic symptom of air in the hydraulic circuit. Air is compressible; brake fluid is not.

**Most common sources:**
1. Recent brake work where bleeding was incomplete
2. A leak that admitted air after a component failure
3. Old, degraded rubber flex hoses — the inner lining of a brake hose can delaminate and partially block flow, or the outer rubber can allow microscopic air ingestion; this is more common on high-mileage XJs where hoses have never been replaced

**Test:** Pump the pedal several times. If it firms up with pumping but returns to spongy after a pause, air is present.

**Resolution:** Bleed the system. If the condition returns after a proper bleed, find the source of air ingestion (leaking caliper, wheel cylinder, hose).

---

### Pedal sinks slowly to the floor under steady pressure — master cylinder internal leak

A pedal that builds normally when first pressed but slowly sinks to the floor when held steadily indicates the master cylinder is bypassing internally. The piston seals are worn and fluid is passing from the high-pressure side back to the reservoir.

**Test:** With the engine running (booster active), press and hold the pedal firmly for 30–60 seconds. If it sinks progressively toward the floor with no change in foot pressure, the master cylinder is failing internally. There may be no external fluid leak.

This is distinct from a spongy pedal — the pedal feels firm initially, then gives way slowly.

**Resolution:** Master cylinder replacement.

---

### Hard pedal — power brake booster failure

A pedal that requires significantly more foot effort than usual to achieve braking effect indicates a power brake booster problem. The booster uses engine intake manifold vacuum to multiply pedal effort; when it fails, the brakes revert to unassisted hydraulic operation.

**Test sequence:**
1. With the engine off, pump the brake pedal 5–6 times to bleed down any stored vacuum in the booster
2. Hold the pedal down with moderate pressure
3. Start the engine
4. A working booster will cause the pedal to move down slightly as vacuum is applied
5. If the pedal does not move down when the engine starts, the booster is not generating assist

**Additional check:** With the engine off and vacuum depleted (pumped down), hold steady moderate pressure on the pedal. If the pedal sinks to the floor under this condition, the master cylinder is bypassing — the booster condition is secondary to the master cylinder problem.

**Vacuum source:** The XJ brake booster is fed by engine intake manifold vacuum. Confirm the vacuum hose from the booster to the intake manifold is intact and not cracked before condemning the booster.

**Resolution:** Booster replacement if vacuum supply is confirmed good but assist is absent.

---

### Pedal fade under repeated hard stops — heat buildup

Brake fade under repeated hard applications is not a hydraulic problem — it is a thermal problem. The brakes are overheating.

**Most likely cause:** A sticking front caliper piston or frozen rear drum adjuster is causing one wheel to drag continuously, overheating the brake assembly. The dragging wheel gets hot, pad material glazes, and effectiveness drops.

**Quick check:** After a test drive involving several brake applications, park and use an infrared thermometer on each wheel. A wheel that is significantly hotter than the others has a dragging brake.

**Secondary cause:** Brake fluid with a low boiling point from water absorption. Old fluid can vaporize at the caliper under high heat, creating a compressible pocket — fluid fade. Brake fluid absorbs moisture over time; flushing old fluid is part of brake system maintenance.

**Resolution:** Find and fix the dragging caliper or drum adjuster. Flush brake fluid if age is unknown.

---

## Exit criteria

- **Spongy pedal:** bleed the system; replace any flex hoses that are original or show cracking
- **Sinking pedal:** master cylinder replacement
- **Hard pedal:** booster replacement; confirm vacuum supply first
- **Pedal fade:** identify dragging brake; flush fluid if age is unknown

## Related stock reference
- Brakes stock overview: [`../../vehicle/systems/brakes/overview.md`](../../vehicle/systems/brakes/overview.md)
- Rear drum inspection: [`rear-drum-issues.md`](rear-drum-issues.md)
