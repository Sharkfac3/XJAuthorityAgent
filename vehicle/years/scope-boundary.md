# XJ and MJ Knowledgebase Scope Boundary

Defines what this knowledgebase covers and what it does not. The expert agent uses this file to avoid answering out-of-scope questions with in-scope assumptions.

---

## In scope — Jeep Cherokee XJ (1988–2001)

**1988–2001 Jeep Cherokee XJ with the 4.0L inline-six engine.**

The 1988 start date covers the first full model year of the revised Renix 4.0L SMFI (sequential multi-port fuel injection). Engine, ECU, axle, and electrical documentation in this knowledgebase was written against this vehicle range.

The 2001 end date is the final XJ model year.

**Control eras covered:**
- Era 1 / Renix — 1988–1990
- Era 2 / SBEC (OBD-I) — 1991–1995
- Era 3 / JTEC (OBD-II) — 1996–2001

---

## In scope — Jeep Comanche MJ (1986–1992)

**1986–1992 Jeep Comanche MJ with the 4.0L inline-six or 2.5L inline-four engine.**

The Comanche is a pickup truck built on the XJ Cherokee unibody platform. It shares the majority of its powertrain, electrical, and drivetrain architecture with the XJ.

**Control eras covered:**
- Era 1 / Renix — 1986–1990 (4.0L and 2.5L)
- Era 2 / SBEC (OBD-I) — 1991–1992

The MJ does not have an Era 3 / JTEC variant. It was discontinued before the 1996 OBD-II transition.

### What the XJ and MJ share

The following content documented in this knowledgebase applies to both platforms unless explicitly noted otherwise:

| System | Shared |
|--------|--------|
| 4.0L inline-six engine | Yes — same block, head, and injection architecture |
| 2.5L inline-four engine | Yes — same engine family in both |
| Renix ECU (Era 1) | Yes — same ECU and sensor architecture |
| SBEC ECU (Era 2) | Yes — same ECU family |
| AW4 automatic transmission | Yes — identical unit and TCM wiring |
| AX-15 manual transmission | Yes — identical unit |
| NP231 transfer case | Yes — identical unit |
| NP242 transfer case | Yes — available in both |
| Dana 30 front axle | Yes — same axle family |
| Dana 35 rear axle | Yes — same axle family |
| Chrysler 8.25 rear axle | Yes — available in MJ |
| Front suspension geometry | Yes — same coil-spring front suspension |
| Most electrical sensors | Yes — same CPS, CTS, TPS, MAP architecture |

### Where the XJ and MJ diverge

| System | Difference |
|--------|-----------|
| Body structure | MJ is a pickup truck (cab + bed); XJ is a wagon — no body part interchange |
| Doors | Not interchangeable — different door openings |
| Unibody floor sections | Different — MJ has a pickup frame/unibody hybrid with a separate bed |
| Wheelbase | MJ offered in short-bed (119.4 in) and long-bed (131 in); XJ is 101.4 in |
| Rear suspension | MJ rear is leaf-spring with a conventional pickup setup; XJ rear is also leaf-spring but different geometry |
| Towing capacity | MJ is higher rated due to pickup chassis design |
| Interior | Different dash, trim, and configurations |
| Engine options | MJ was available with 2.5L I-4 from the start; 2.5L XJ was less common in later years |
| Era 3 (JTEC) | XJ only — MJ ended before 1996 |

### Content shared without duplication

Where XJ and MJ use identical hardware, this knowledgebase documents it once with explicit notes on applicability. Do not duplicate shared content into MJ-specific files — cross-link instead. Only create MJ-specific files where the MJ has meaningful differences.

---

## Partial coverage — 1984–1987 XJ

The 1984–1987 XJ Cherokee exists but is only partially covered here.

| Years | Engine options | ECU / fuel system | Status |
|-------|---------------|-------------------|--------|
| 1984–1986 | Carbureted 2.5L I4, Carbureted 2.8L GMV6 | No ECU (carbureted) | Out of scope |
| 1987 | 4.0L Renix MPI (173 hp), 2.5L TBI | Early Renix ECU | Partially out of scope |
| 1988+ | 4.0L Renix MPI (177 hp), 2.5L TBI | Renix ECU (revised) | **In scope** |

The expert agent should not make definitive claims about 1984–1987 XJs using this knowledgebase's content. Many body, axle, and suspension facts do apply (same chassis) but have not been verified against pre-1988 configurations.

---

## Out of scope — related vehicles

### ZJ Grand Cherokee (1993–1998)

Different unibody architecture — wider, longer, and heavier than the XJ. Uses the same 4.0L HO engine family (1991+ head casting, same block, similar ECU architecture). Rear disc brake hardware from ZJ is a common donor source for XJ disc brake conversion.

**Powertrain overlap:** 4.0L HO engine blocks and heads are the same casting family. Some sensors and ECU components interchange. Rear axle (Dana 35 or C8.25 depending on year/option) uses same WMS width as XJ.

ZJ-specific content (body, HVAC, suspension geometry) does not apply to the XJ.

### WJ Grand Cherokee (1999+)

Entirely different platform — no meaningful component overlap with XJ beyond the 4.0L engine family (which continued into early WJ production). Out of scope.

### TJ Wrangler (1997+)

Body-on-frame vehicle. Shares the Dana 30 front axle (and specifically the low-pinion front axle geometry introduced on both TJ and XJ in 1997/2000). Dana 35 and C8.25 rear axle hardware is also shared.

**Axle overlap:** Post-2000 XJ Dana 30 front axle gearsets interchange with TJ Dana 30 (both low-pinion). Pre-2000 XJ Dana 30 (high-pinion) does not interchange with TJ.

TJ-specific drivetrain, ECU, body, and electrical content does not apply to the XJ or MJ.

### XJ Cherokee in other markets (non-US)

This knowledgebase covers US-market XJs. Differences exist in engine options (diesel 4-cylinder available in European market), emissions equipment, and some electrical architecture. Non-US market configurations are out of scope.

---

## Why these boundaries exist

The purpose of these boundaries is to prevent the expert agent from applying XJ-specific diagnostic logic, ECU assumptions, or parts sourcing guidance to vehicles that share a name or some components but have material differences.

When a user's question involves a vehicle at or near these boundaries, the expert agent should explicitly note the boundary and limit its confidence accordingly.
