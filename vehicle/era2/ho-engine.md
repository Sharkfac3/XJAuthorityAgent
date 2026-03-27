# HO Engine — Identity and Mechanical Profile

## What "HO" means
HO stands for **High Output**. It is Jeep's marketing designation for the revised 4.0L inline-six introduced in 1991 when Chrysler replaced the Renix engine management system. The name reflects real mechanical improvements over the Renix-era 4.0L — it is not purely a rebadge.

The HO designation applies to the engine hardware. It is distinct from the ECU system. HO engines were used across two management eras:
- **1991–1995** — SBEC (Era 2, OBD-I)
- **1996–2001** — JTEC (Era 3, OBD-II)

When someone says "HO engine" they are referring to the 1991+ mechanical package, regardless of which ECU is attached to it.

---

## What stayed the same from Renix

The 4.0L HO shares its foundation with the Renix engine:

| Spec | Value |
|------|-------|
| Displacement | 242 CID / 3,964 cc |
| Bore × Stroke | 3.88″ × 3.41″ |
| Compression ratio | ~8.8:1 |
| Firing order | 1-5-3-6-2-4 |
| Block material | Cast iron |
| Head material | Cast iron |
| Fuel system | Sequential multi-port injection |
| Fuel pressure | 39 psi (Era 2); 49 psi (Era 3) |

---

## What changed from Renix to HO

### Cylinder head
The HO received a revised head casting with improved port geometry and better airflow than the Renix head. The intake port shape changed slightly — this is why the Renix intake manifold does not bolt directly to an HO head without a new Renix intake gasket (the ports don't fully match).

### Valve train — roller rockers
The HO introduced **roller rocker arms** in place of the Renix flat-tappet design. Roller rockers reduce valve train friction, extend camshaft life, and allow the engine to rev more freely at the top of its range.

### Intake manifold
New casting with revised port geometry to match the HO head. Not directly interchangeable with Renix manifold without a gasket change.

### Exhaust manifold
New casting. Exhaust port dimensions are identical to Renix, so Renix and HO exhaust manifolds bolt to either head — but the castings are different shapes.

### Power output
| Engine | Horsepower | Torque |
|--------|-----------|--------|
| Renix 4.0L (1988–1990) | 177 hp @ 4,500 RPM | 224 lb-ft @ 2,500 RPM |
| HO 4.0L (1991–2001) | 190 hp @ 4,750 RPM | 225 lb-ft @ 4,000 RPM |

The HO produces more peak power and makes its torque at a higher RPM. The Renix engine delivers peak torque lower in the rev range. Both are strong at street RPMs.

### Distributor
The HO distributor contains only the cam position sensor (sync pulse generator). The Renix distributor also housed the ICM. The two are **not interchangeable** — the HO distributor cannot be used with Renix engine management, and vice versa.

### Flywheel and flexplate
The HO flywheel/flexplate carries a different reluctor ring pattern (**18-2-2-2**) that the SBEC CPS is designed to read. The Renix CPS reads a different pattern. When doing an HO block-into-Renix-chassis swap, the Renix flywheel/flexplate must be retained. See `work/swaps/engine/ho-into-renix.md`.

### Oil filter thread
The HO block uses a standard SAE 3/4″-16 oil filter thread, replacing the Renix proprietary 20mm thread. HO blocks accept standard oil filters without conversion. See `work/upgrades/engine/oil-filter-sae-conversion.md` for converting a Renix block.

---

## Block compatibility notes

Not all HO blocks are interchangeable with all XJ applications. Motor mount bolt holes and accessory mounting holes differ between generations:

| Block family | Compatible applications |
|-------------|------------------------|
| XJ / ZJ ('93–'98) | Interchangeable with each other |
| YJ / '97–'99 TJ | Compatible with XJ/ZJ applications |
| 2000+ TJ / WJ ('99–'04) | Interchangeable with each other only |
| XJ/ZJ blocks | **Not compatible** with 2000+ TJ/WJ without significant modification |

---

## Temperature sender location change (1996+)
Beginning in 1996, the rear head drilling for the temperature gauge sender was eliminated from the casting. 1996+ HO heads require the sender to be relocated to the thermostat housing or the head must be drilled and tapped. This is relevant when swapping a 1996+ HO block into a pre-1996 chassis. See `work/swaps/engine/ho-into-renix.md`.

---

## Summary: HO vs Renix at a glance

| Feature | Renix (1988–1990) | HO (1991–2001) |
|---------|-------------------|----------------|
| Head porting | Original | Revised, better flow |
| Valve train | Flat-tappet rockers | Roller rockers |
| Peak power | 177 hp | 190 hp |
| Peak torque RPM | 2,500 RPM | 4,000 RPM |
| Distributor | ICM + cam sync | Cam sync only |
| Flywheel pattern | Renix-specific | 18-2-2-2 |
| Oil filter thread | Proprietary 20mm | Standard SAE |
| Engine management | Renix ECU + ICM | SBEC (1991–95) / JTEC (1996–2001) |

---

## See also
- `vehicle/era2/overview.md` — SBEC ECU system (1991–1995 management)
- `vehicle/era3/` — JTEC ECU system (1996–2001 management)
- `vehicle/engine.md` — shared 4.0L baseline facts
- `work/swaps/engine/ho-into-renix.md` — installing an HO block into a Renix chassis

## Source
Cruiser54 — cruiser54.com, "HO into Renix Swap" (mechanical context); community-verified specifications.
