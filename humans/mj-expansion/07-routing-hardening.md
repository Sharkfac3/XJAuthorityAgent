# Prompt 7 — Routing Hardening

Copy and paste the prompt below into a new chat session to run this step.

Prerequisite: Prompts 1–6 must be complete before running this one.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then read:
- `vehicle/mj/overview.md`
- `vehicle/mj/index.md`

## Your task

Harden routing across all four knowledge roots so the expert agent can correctly and efficiently navigate questions about both XJ and MJ. This is a structural pass — you are checking and correcting indexes and routers, not adding new knowledge.

## What to verify and fix

### 1. Platform disambiguation in `AGENTS.md`

Read `AGENTS.md`. Verify:
- The expert routing rules ask for platform (XJ or MJ) when the answer depends on it
- The knowledge roots describe both platforms
- No routing step sends the agent to ECU swaps as a special first-class destination (ECU swap is one type under `work/swaps/`)

Fix any remaining XJ-only language.

### 2. `vehicle/index.md` — platform routing

Read it. The vehicle index should route the expert agent to the right content based on platform. Verify:
- There is a clear path to MJ-specific content (`vehicle/mj/index.md`)
- The XJ era files (`vehicle/era1/`, `vehicle/era2/`, `vehicle/era3/`) are linked with a note that era 3 is XJ-only
- The systems index properly notes shared vs. MJ-divergent systems

Add any missing routing paths.

### 3. `vehicle/years/index.md`

Read it. Verify:
- MJ year coverage is mentioned and routed
- The scope boundary file is linked
- XJ and MJ year splits are both accessible

Fix any gaps.

### 4. `diagnostics/index.md` — platform disambiguation

Read it. Verify:
- The index notes which diagnostic branches apply to MJ
- Era 3 diagnostics are marked as XJ-only
- New MJ diagnostic leaves (from Prompt 4) are listed and linked

Add any missing entries.

### 5. `sourcing/index.md` — MJ routing

Read it. Verify:
- MJ donor profile is linked
- MJ interchange content is listed and routed
- The index does not imply XJ-only scope

### 6. `work/index.md` — platform scope

Read it. Verify:
- Scope now says XJ and MJ (already fixed)
- Any MJ-specific work files created in Prompt 6 are linked or reachable via their subcategory index
- The swap routing does not special-case ECU swaps at the top level

### 7. `vehicle/systems/index.md` — system-level routing

Read it. Verify:
- Each subsystem entry has been updated with an MJ applicability note (from Prompt 3) or is linked to MJ divergence content
- No system entry implies XJ-only scope without explaining why (e.g., Era 3 content)

### 8. Cross-root boundary links

Check that every root's boundary-links section correctly mentions both vehicles where appropriate:
- `vehicle/index.md` boundary links
- `work/index.md` boundary links
- `diagnostics/index.md` boundary links
- `sourcing/index.md` boundary links

### 9. `humans/start-expert-agent.md` routing accuracy

Read it. Verify:
- The classification logic includes platform (XJ or MJ) as a disambiguation step
- The ECU swap routing is not listed as a peer-level category (it is under `work/swaps/`)
- The prompt accurately reflects how the expert should route both-platform questions

Fix any remaining drift.

### 10. `humans/start-knowledgebase-builder.md` accuracy

Read it. Verify the placement rules and operating instructions reflect the two-vehicle scope. Fix any remaining XJ-only language.

## Routing test — run these questions mentally

After completing the above, mentally route each of these example questions through the updated index structure. For each, identify which files the expert agent would load and verify that path is correct:

1. "What axles came on a 1988 MJ Comanche with 4WD?"
   - Expected: `vehicle/mj/overview.md` or `vehicle/mj/divergence.md` → `vehicle/systems/axles/` (shared content)

2. "My 1990 MJ Comanche isn't getting spark. Where do I start?"
   - Expected: `diagnostics/ignition/` → no-spark leaf → confirm Era 1 (Renix) applies to 1990 MJ → `vehicle/era1/overview.md`

3. "I want to swap the ECU in my 1991 MJ. What do I need?"
   - Expected: `work/swaps/ecu/index.md` → Stage 1 identifies Era 2 → Era 3 files skipped → `vehicle/era2/overview.md` → `work/swaps/ecu/ecu-selection/requirements.md`

4. "Where do I look for rust on a used MJ?"
   - Expected: `diagnostics/body-and-interior/mj-rust-inspection.md` AND `work/inspections/pre-purchase/mj-checklist.md`

5. "Can I use MJ axles in my XJ?"
   - Expected: `sourcing/interchange/mj-xj-drivetrain.md`

If any of these paths breaks (file doesn't exist or router doesn't lead there), note the gap but do not create speculative content to fill it — flag it for the gap audit in Prompt 8.

## Output

Leave a plain-text summary listing:
1. Each index or router file updated and what was changed
2. Any routing gaps found (with specific question example that broke)
3. Any items deferred to the Prompt 8 gap audit
