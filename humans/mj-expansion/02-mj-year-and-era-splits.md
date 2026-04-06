# Prompt 2 — MJ Year and Era Splits

Copy and paste the prompt below into a new chat session to run this step.

Prerequisite: Prompt 1 must be complete before running this one.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then read:
- `vehicle/mj/overview.md`
- `vehicle/mj/divergence.md`
- `vehicle/years/scope-boundary.md`
- `vehicle/era1/overview.md`
- `vehicle/era2/overview.md`

## Your task

Build the MJ year and era split content. The MJ runs 1986–1992 and crosses two XJ control eras. Document what was different year to year and what the era transition means for the MJ specifically.

## What to build

### 1. `vehicle/mj/years.md`

A year-by-year matrix for the MJ covering significant production changes. Include:

**For each year or year range, document:**
- Engine options available
- Transmission options
- Transfer case options
- Control era (Renix or SBEC)
- Notable changes from the previous year (new options, discontinued options, trim changes, electrical changes)
- Any MJ-specific changes that differ from the equivalent XJ year

**Key known year splits to research and document (mark uncertain items as `Status: needs verification`):**
- 1986: First production year — 2.5L and 4.0L available; Renix; NP207 transfer case
- 1987: 4.0L becomes standard on upper trims; first year of revised Renix 4.0L (177 hp)
- 1988–1990: Renix era continues; 2WD and 4WD availability
- 1991: SBEC transition — new OBD-I ECU architecture replacing Renix; changes to fuel injection and ignition control
- 1992: Final production year; any last-year production changes

### 2. `vehicle/mj/era1-notes.md`

MJ-specific notes for Era 1 (Renix, 1986–1990). Cover:

- How the MJ Renix system is the same as the XJ Renix system (direct cross-link to `vehicle/era1/overview.md`)
- Any MJ-specific Renix differences:
  - Were any sensors, harness connectors, or wiring runs different due to the pickup body?
  - Did the 2.5L Renix in the MJ differ from the 4.0L Renix in wiring or ECU?
- Mark claims as `Status: needs verification` where you cannot confirm from community-verified sources

If there are no meaningful MJ differences from the XJ Renix architecture, write that explicitly and cross-link rather than creating an empty or speculative file.

### 3. `vehicle/mj/era2-notes.md`

MJ-specific notes for Era 2 (SBEC, 1991–1992). Cover:

- How the MJ SBEC system is the same as the XJ SBEC system (direct cross-link to `vehicle/era2/overview.md`)
- Any MJ-specific SBEC differences
- The MJ's last two years of production — any known end-of-run production variations
- Mark claims as `Status: needs verification` where needed

If there are no meaningful MJ differences from the XJ SBEC architecture, write that explicitly and cross-link.

### 4. Add a note to `vehicle/era1/overview.md` and `vehicle/era2/overview.md`

Read each file. At the bottom of each, add a short section:

```
## MJ Comanche applicability
The [Era 1 / Era 2] content in this file applies to the Jeep Comanche MJ [1986–1990 / 1991–1992].
For MJ-specific differences, see `vehicle/mj/era1-notes.md` [or era2-notes.md].
```

Only add this if it is not already present.

## Placement rules

- All new MJ files go under `vehicle/mj/`
- Do not duplicate XJ era content — reference and cross-link
- Do not invent specifications — mark uncertain items with `Status: needs verification`

## Output

Leave a short plain-text summary of what was created, what cross-links were added to existing XJ era files, and any items flagged for verification.
