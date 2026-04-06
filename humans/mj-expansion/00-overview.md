# MJ Expansion Series — Overview

This folder contains the complete prompt series for expanding the XJ knowledgebase to fully cover the Jeep Comanche MJ.

Run each prompt in order. Each prompt activates the Knowledgebase Builder agent and produces a specific, bounded piece of MJ knowledge. Do not skip prompts — each one builds on the previous.

---

## What this series produces

When complete, the knowledgebase will:
- Have a full MJ platform baseline matching the depth of the XJ baseline
- Cover MJ year and era splits (1986–1992; Era 1 and Era 2 only — no Era 3)
- Document every system where MJ diverges from XJ, and explicitly confirm what is shared
- Have MJ-aware diagnostic routing
- Have MJ sourcing content (donors, body parts, unique interchange)
- Have MJ-specific work procedure notes where the XJ procedure does not apply
- Route the expert agent correctly for both platforms across all knowledge roots

---

## Prompt execution order

| Prompt | File | Produces |
|--------|------|---------|
| 1 | `01-mj-platform-baseline.md` | MJ vehicle foundation — identity, eras, engine options, shared architecture |
| 2 | `02-mj-year-and-era-splits.md` | MJ year matrix and era-specific control system content |
| 3 | `03-mj-vehicle-systems.md` | MJ-specific system files for every subsystem that diverges from XJ |
| 4 | `04-mj-diagnostics.md` | MJ-aware diagnostic routing and MJ-specific symptom notes |
| 5 | `05-mj-sourcing.md` | MJ donor profiles, body part sourcing, and unique interchange facts |
| 6 | `06-mj-work-procedures.md` | MJ-specific work procedure notes and any unique MJ execution paths |
| 7 | `07-routing-hardening.md` | Cross-root routing audit — verify all indexes route correctly for both vehicles |
| 8 | `08-gap-audit.md` | Final coverage gap check — identify any remaining XJ-only content that needs MJ treatment |

---

## Key facts to keep in mind

- The MJ shares nearly all powertrain and electrical architecture with the XJ. Document shared content once and cross-link — do not duplicate.
- The MJ has Era 1 (Renix, 1986–1990) and Era 2 (SBEC, 1991–1992) only. Era 3 (JTEC) is XJ-only.
- MJ body, cab, bed, and unibody floor sections do not interchange with the XJ. Everything behind the firewall is different.
- The MJ had a 2.5L I-4 option alongside the 4.0L I-6. The XJ also had a 2.5L but it was less dominant.
- MJ wheelbase: short-bed (119.4 in) and long-bed (131 in). XJ is 101.4 in.
- Use `vehicle/years/scope-boundary.md` as the authoritative reference for what is and is not in scope.
