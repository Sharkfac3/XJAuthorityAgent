# XJ Knowledgebase Scope Boundary

Defines what this knowledgebase covers and what it does not. The expert agent uses this file to avoid answering out-of-scope questions with in-scope assumptions.

---

## In scope

**1988–2001 Jeep Cherokee XJ with the 4.0L inline-six engine.**

The 1988 start date covers the first full model year of the revised Renix 4.0L SMFI (sequential multi-port fuel injection). Engine, ECU, axle, and electrical documentation in this knowledgebase was written against this vehicle range.

The 2001 end date is the final XJ model year.

---

## Partial coverage — 1984–1987 XJ

The 1984–1987 XJ Cherokee exists but is only partially covered here.

| Years | Engine options | ECU / fuel system | Status |
|-------|---------------|-------------------|--------|
| 1984–1986 | Carbureted 2.5L I4, Carbureted 2.8L GMV6 | No ECU (carbureted) | Out of scope |
| 1987 | 4.0L Renix MPI (173 hp), 2.5L TBI | Early Renix ECU | Partially out of scope |
| 1988+ | 4.0L Renix MPI (177 hp), 2.5L TBI | Renix ECU (revised) | **In scope** |

**What this means in practice:** Electrical, fuel system, and ECU content in this knowledgebase does not apply to 1984–1986 XJs. Many body, axle, and suspension facts do apply (same chassis) but have not been verified against pre-1988 configurations. The expert agent should not make definitive claims about 1984–1987 XJs using this knowledgebase's content.

**Axle and suspension overlap:** The Dana 30 / Dana 35 axle architecture and leaf-spring suspension are shared from 1984 onward. Dimensional specs documented here are generally valid for all XJ years, but the C8.25 rear axle did not exist in XJs before 1991.

---

## Out of scope — related vehicles

### MJ Comanche (1986–1992)

Pickup truck built on the XJ platform. Shares the 4.0L engine family, AW4 transmission, NP231/NP242 transfer cases, front and rear axle assemblies, and most of the Renix/SBEC electrical architecture with the XJ Cherokee.

**Component interchange with XJ:** Engine, transmission, transfer case, axle assemblies, ECU, most electrical hardware interchange directly.

**What does not interchange:** Cab/bed body structure, doors, unibody floor sections.

The Comanche is not documented here. Facts about the 4.0L drivetrain in this knowledgebase generally apply to the MJ but have not been verified against MJ-specific production differences.

### ZJ Grand Cherokee (1993–1998)

Different unibody architecture — wider, longer, and heavier than the XJ. Uses the same 4.0L HO engine family (1991+ head casting, same block, similar ECU architecture). Rear disc brake hardware from ZJ is a common donor source for XJ disc brake conversion.

**Powertrain overlap:** 4.0L HO engine blocks and heads are the same casting family. Some sensors and ECU components interchange. Rear axle (Dana 35 or C8.25 depending on year/option) uses same WMS width as XJ.

ZJ-specific content (body, HVAC, suspension geometry) does not apply to the XJ.

### WJ Grand Cherokee (1999+)

Entirely different platform — no meaningful component overlap with XJ beyond the 4.0L engine family (which continued into early WJ production). Out of scope.

### TJ Wrangler (1997+)

Body-on-frame vehicle. Shares the Dana 30 front axle (and specifically the low-pinion front axle geometry introduced on both TJ and XJ in 1997/2000). Dana 35 and C8.25 rear axle hardware is also shared.

**Axle overlap:** Post-2000 XJ Dana 30 front axle gearsets interchange with TJ Dana 30 (both low-pinion). Pre-2000 XJ Dana 30 (high-pinion) does not interchange with TJ.

TJ-specific drivetrain, ECU, body, and electrical content does not apply to the XJ.

### XJ Cherokee in other markets (non-US)

This knowledgebase covers US-market XJs. Differences exist in engine options (diesel 4-cylinder available in European market), emissions equipment, and some electrical architecture. Non-US market configurations are out of scope.

---

## Why these boundaries exist

The purpose of these boundaries is to prevent the expert agent from applying XJ-specific diagnostic logic, ECU assumptions, or parts sourcing guidance to vehicles that share a name or some components but have material differences. An answer that is correct for a 1999 XJ Cherokee may be wrong for a 1999 WJ Grand Cherokee, a 1986 XJ Cherokee, or a 1999 MJ Comanche.

When a user's question involves a vehicle at or near these boundaries, the expert agent should explicitly note the boundary and limit its confidence accordingly.
