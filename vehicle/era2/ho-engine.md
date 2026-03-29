# HO Engine — Identity and Mechanical Profile

## What "HO" means
HO stands for **High Output**. It is Jeep's marketing designation for the revised 4.0L inline-six introduced in 1991 when Chrysler replaced the Renix engine management system. The name reflects real mechanical improvements over the Renix-era 4.0L — it is not purely a rebadge.

The HO designation applies to the engine hardware. It is distinct from the ECU system. HO engines were used across two management eras:
- **1991–1995** — SBEC (Era 2, OBD-I)
- **1996–2001** — JTEC (Era 3, OBD-II)

When someone says "HO engine" they are referring to the 1991+ mechanical package, regardless of which ECU is attached to it.

The YJ Wrangler never received the Renix 4.0L — it only got the 4.0L starting in 1991, so it is HO-only.

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
| Head bolt pattern | Same across all 4.0L generations — heads are mechanically cross-compatible |
| Fuel system | Sequential multi-port injection |
| Valve train type | Hydraulic flat-tappet camshaft, stamped steel rocker arms (1.6:1 ratio, pedestal mount) |

**Valve train note:** Both Renix and HO use stamped steel, non-roller rocker arms with a hydraulic flat-tappet camshaft. Roller rockers are strictly an aftermarket upgrade (Harland Sharp, Yella Terra). Neither generation used roller rockers from the factory. A full roller cam conversion is extremely difficult on the 4.0L due to anti-rotation requirements for roller lifters and tight bore geometry — there is no practical off-the-shelf solution.

---

## What changed from Renix to HO

### Cylinder head
The most significant mechanical difference. The Renix uses a **low-port head** with intake port geometry inherited from the older 4.2L (258ci) engine. The HO head raises the intake ports approximately 1/8″ (3.2mm) for a better entry radius and improved airflow.

The ports do not align between Renix and HO heads. You cannot bolt an HO intake manifold to a Renix head (or vice versa) without also swapping the head. Exhaust ports are the same between Renix and HO.

#### Head casting evolution within HO
| Casting | Years | Notes |
|---------|-------|-------|
| 0331 (early) | 2000–mid-2001 | Prone to cracking between cylinders 3–4. Avoid. |
| 0331 TUPY | Mid-2001+ TJ/WJ | Improved casting, no cracking issue. Desirable swap head. |
| 0630 | 1996–1999 XJ/ZJ/TJ | Solid casting. May or may not have rear temp sender boss. |

0630 and 0331 heads have different coil rail mounting boss configurations and different exhaust port shapes — cross-era installation requires adapter gaskets or custom brackets.

### Intake manifold
New casting with raised port geometry to match the HO head. Not interchangeable with the Renix manifold without a head swap.

The HO intake also evolved within its own run:
- **1991–1998** — Straight-runner intake. Better than Renix but not ideal.
- **1999–2000** — Revised "curved runner" intake. Noticeably better flow. The community calls this the "good intake."
- **2001 XJ** — Even larger intake casting. Best stock intake of the XJ run.

### Exhaust manifold
New casting. EGR was eliminated on the HO, so HO exhaust manifolds lack the EGR port tube present on Renix manifolds. Exhaust port dimensions are the same, so Renix and HO manifolds will physically bolt to either head — but the castings are different shapes and EGR provisions differ.

### Camshaft profile
Different profile between Renix and HO. The HO cam was installed approximately 8° retarded compared to the Renix cam (which runs 1–2° advanced). This shifts the HO power band higher in the RPM range and reduces low-end cylinder pressure enough that the HO does not require a knock sensor. The Renix cam favors low-end torque; the HO cam leans toward top-end output.

### EGR and knock sensor
The Renix system includes both an EGR valve and a knock sensor. The HO eliminated both.

**EGR:** Not relevant to stroker build decisions. EGR is a manifold and head feature — it gets deleted on virtually all stroker builds regardless of block year.

**Knock sensor:** The Renix knock sensor allows the factory ECU to retard timing in response to detonation. Whether this is an advantage depends entirely on ECU choice:
- **Stock Renix ECU retained:** Knock sensor provides adaptive timing protection — useful, but reportedly has limited retard range and may not be effective on aggressive builds.
- **Aftermarket ECU (Speeduino, rusEFI, Megasquirt, etc.):** Knock sensor integration is ECU-configurable. The presence or absence of a factory-machined knock sensor boss on the block is a minor consideration. The 1991–1995 HO blocks have the knock sensor boss cast in but undrilled — it can be drilled and tapped if needed.

The knock sensor is **not a reason to prefer a Renix block** for a stroker build. It is an ECU-level concern, not a block-level one.

### Power output
| Engine | Horsepower | Torque |
|--------|-----------|--------|
| Renix 4.0L (1987) | 173 hp @ 4,500 RPM | 220 lb-ft @ 2,500 RPM |
| Renix 4.0L (1988–1990) | 177 hp @ 4,500 RPM | 224 lb-ft @ 2,500 RPM |
| HO 4.0L (1991–2001) | 190 hp @ 4,750 RPM | 225 lb-ft @ 4,000 RPM |

The HO produces more peak power and makes its torque at a higher RPM. The Renix engine delivers peak torque lower in the rev range.

### Fuel rail
- **Renix:** Fuel enters at front of rail, returns at rear.
- **1991–1995 HO:** Fuel pressure and return are both at the front of the rail.
- **1996+ HO:** Returnless fuel system — regulator is in or on the tank. No return line at rail.

### Distributor
The HO distributor contains only the cam position sensor (sync pulse generator). The Renix distributor also housed the ICM. The two are **not interchangeable** — the HO distributor cannot be used with Renix engine management, and vice versa.

### Flywheel and flexplate
The HO flywheel/flexplate carries the **18-2-2-2 reluctor ring** that the SBEC CPS is designed to read. The Renix CPS reads a different pattern. When doing an HO block-into-Renix-chassis swap, the Renix flywheel/flexplate must be retained. See `work/swaps/engine/ho-into-renix.md`.

### Oil filter thread
| Engine | Thread |
|--------|--------|
| Renix | M20×1.5 metric |
| HO | 7/8″-11 SAE |

When swapping a Renix long block into an HO vehicle, or vice versa, the oil filter adapter must be swapped as well. See `work/upgrades/engine/oil-filter-sae-conversion.md` for converting a Renix block to SAE thread.

### Alternator voltage regulator
- **Renix:** Separate external voltage regulator.
- **HO:** Voltage regulator is integrated into the PCM.

---

## Distributorless ignition (DIS) — 2000+ sub-generation

Starting with the **2000 model year TJ** and **1999 WJ Grand Cherokee**, the distributor was eliminated in favor of a coil-rail waste-spark DIS system. This is a hard sub-generation boundary within HO:

- 2000+ heads have coil pack mounting bosses that earlier heads lack.
- Converting either direction requires matching PCM, harness, cam sensor, oil pump drive, and coil pack. No bolt-on kit exists.
- The 1999 TJ was a mixed production year — verify individually.

---

## Block compatibility

All 4.0L blocks share the same deck height and head bolt pattern. However, **motor mount and accessory mounting bolt holes** differ between generations, making some block swaps require fabrication.

### Compatible group A — XJ/ZJ/YJ/early TJ
Motor mounts and accessory positions are the same. Drop-in compatible with each other:
- 1991–2001 XJ Cherokee
- 1993–1998 ZJ Grand Cherokee
- 1991–1995 YJ Wrangler
- 1997–1999 TJ Wrangler

### Compatible group B — 1999+ WJ and 2000+ TJ
Clean-sheet external block redesign in 1999/2000. Motor mount bolt holes and accessory belt component mounting holes are in different locations. **Not drop-in compatible with Group A** without significant fabrication.
- 1999–2004 WJ Grand Cherokee
- 2000–2006 TJ Wrangler

### Stroker block preference
**NVH blocks (1996+) are the preferred foundation for stroker builds.** The 1996 redesign added main bearing web ribbing and a main bearing stud girdle — real structural improvements that matter under higher cylinder pressures. The "NVH" designation (Noise, Vibration, Harshness) is physically cast into the block and is the easiest identification marker.

Pre-NVH blocks (1987–1995) are not incapable of being stroked — builders have used them successfully — but they lack these structural improvements and are not the community's recommended choice. Claims of Renix blocks having thicker walls or higher nickel content are disputed and unproven on the forums (JeepStrokers).

For forced induction strokers, the NVH stud girdle becomes more meaningful, and an aftermarket ECU is the strongly preferred path regardless of block year.

Motor mount compatibility (Group A vs Group B) is the more urgent concern than block era — a mismatched block-to-chassis combination requires fabrication regardless of how good the block internals are.

### Known casting numbers
| Casting | Years | Notes |
|---------|-------|-------|
| 53005535 | 1987–1990 | Renix. Pre-NVH — no main web ribbing or girdle. Not preferred for stroker builds. |
| 53008405 | 1991–1995 | Group A HO. Pre-NVH. |
| 53020569 / 53010341 | 1996–1998 | **NVH block.** First year with main web ribbing and stud girdle. Preferred for stroker builds. |
| 53010449 / 53010449AA | 1999–2001 XJ/TJ | **NVH block.** Group A. |
| 53010327AB / 53010328AB | 1999–2004 WJ, 2000–2006 TJ | **NVH block.** Group B — not compatible with Group A. |

---

## Temperature sender location
| Years | Gauge sender location |
|-------|----------------------|
| 1987–1995 | Rear of cylinder head (driver's side) |
| 1991–1995 | PCM sensor moved to thermostat housing; head boss still present |
| Mid-1996 (transition) | Mixed production — some heads still have head boss drilled, some capped |
| 1997–2001 | Single sensor in thermostat housing only; PCM drives dash gauge from that signal |

When swapping a 1997+ head onto a pre-1997 chassis, the temperature gauge sender must be relocated to the thermostat housing and the PCM or gauge sender circuit adapted accordingly.

---

## Summary: HO vs Renix at a glance

| Feature | Renix (1988–1990) | HO (1991–2001) |
|---------|-------------------|----------------|
| Head port location | Low port (4.2L heritage) | Raised port (~1/8″ higher) |
| Valve train | Stamped steel flat-tappet | Same — stamped steel flat-tappet |
| Cam profile | Advanced, low-RPM torque bias | Retarded ~8°, higher RPM bias |
| Peak power | 177 hp | 190 hp |
| Peak torque RPM | 2,500 RPM | 4,000 RPM |
| EGR | Yes | No |
| Knock sensor | Yes | No |
| Distributor | ICM + cam sync | Cam sync only |
| Flywheel pattern | Renix-specific | 18-2-2-2 |
| Oil filter thread | M20×1.5 metric | 7/8″-11 SAE |
| Fuel return | Rear of rail | Front of rail (1991–95); returnless (1996+) |
| Voltage regulator | External | Integrated into PCM |
| Engine management | Renix ECU + ICM | SBEC (1991–95) / JTEC (1996–2001) |

---

## See also
- `vehicle/era2/overview.md` — SBEC ECU system (1991–1995 management)
- `vehicle/era3/` — JTEC ECU system (1996–2001 management)
- `vehicle/engine.md` — shared 4.0L baseline facts
- `work/swaps/engine/ho-into-renix.md` — installing an HO block into a Renix chassis

## Sources
Community-verified via NAXJA, JeepForum, CherokeeTalk, CherokeeForum, Pirate4x4, JeepStrokers, Wrangler TJ Forum; cross-referenced against Wikipedia AMC Straight-6 engine article and Allpar Jeep 4.0 PowerTech documentation.
