# Prompt 8 — Gap Audit

Copy and paste the prompt below into a new chat session to run this step.

Prerequisite: Prompts 1–7 must all be complete before running this one.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`. Then read:
- `vehicle/mj/overview.md`
- `vehicle/mj/divergence.md`
- `vehicle/years/scope-boundary.md`

## Your task

Run the final coverage gap audit. After the first seven prompts, the knowledgebase should have full MJ coverage that mirrors XJ depth. This prompt finds anything that was missed.

## Audit dimensions

### 1. Platform symmetry check

For every major XJ content branch, verify there is an equivalent MJ treatment — either a MJ-specific file, or an applicability note on the existing XJ file. Run through this checklist:

**vehicle/**
- [ ] MJ platform overview exists (`vehicle/mj/overview.md`)
- [ ] MJ year matrix exists (`vehicle/mj/years.md`)
- [ ] MJ divergence document exists (`vehicle/mj/divergence.md`)
- [ ] MJ Era 1 notes exist or XJ Era 1 file has MJ note
- [ ] MJ Era 2 notes exist or XJ Era 2 file has MJ note
- [ ] XJ Era 3 files are marked as XJ-only (MJ does not apply)
- [ ] Each vehicle system file has an MJ applicability note or a cross-link to a MJ-specific file
- [ ] Scope boundary file accurately describes MJ as in-scope

**diagnostics/**
- [ ] `diagnostics/index.md` routes for both platforms
- [ ] Era 3 diagnostic content is clearly marked XJ-only
- [ ] MJ body rust inspection exists
- [ ] MJ water intrusion diagnostic exists
- [ ] All other diagnostic leaves have MJ applicability notes

**sourcing/**
- [ ] MJ donor profile exists
- [ ] MJ-to-XJ drivetrain interchange document exists
- [ ] MJ body non-interchange document exists
- [ ] Sourcing index routes for both platforms

**work/**
- [ ] Work index scope covers both platforms
- [ ] Maintenance content has MJ applicability notes
- [ ] Repair content has MJ applicability notes or MJ-specific files where needed
- [ ] ECU swap content applies to Era 1/2 MJ; Era 3 content is marked XJ-only
- [ ] MJ 2.5L ECU requirements document exists
- [ ] MJ pre-purchase inspection checklist exists
- [ ] Suspension upgrade content has MJ caveats where rear suspension differs

### 2. XJ-only language sweep

Search the entire repo for any remaining instances of language that implies XJ-only scope in a context that should cover both vehicles. Look for:
- "XJ knowledgebase" (should be "XJ and MJ knowledgebase")
- "Jeep Cherokee XJ" in a context that excludes MJ without explanation
- "this knowledgebase covers XJ" without mentioning MJ
- Files in `vehicle/`, `work/`, `diagnostics/`, `sourcing/` that have XJ in the title or scope statement with no MJ equivalent

For each instance found:
- If it is in a shared-content file: add MJ language
- If it is genuinely XJ-specific (e.g., Era 3 content): add an explicit note that MJ does not apply

### 3. Verification tag sweep

Search for any `Status: needs verification` tags added during Prompts 1–6. For each:
- List the file and the specific claim
- Attempt to confirm the claim from the existing knowledgebase content or well-established community knowledge
- If confirmed: remove the tag
- If still uncertain: leave the tag and add it to the unresolved list in your output

### 4. Orphaned content check

Check that all new files created in Prompts 1–6 are reachable from at least one index or router file. A file with no inbound links is orphaned and will never be loaded by the expert agent.

For each orphaned file found: add a link to the appropriate index.

### 5. Duplication check

Check for any content that was duplicated between XJ files and new MJ files instead of cross-linked. If you find duplicated facts:
- Identify the canonical file (the one that should be authoritative)
- Replace the duplicate with a cross-link
- Do not delete the canonical content

## Output

Leave a plain-text summary containing:

**Completed items:** List each checklist item above that passed.

**Gaps found and fixed:** List what was missing and what was done to address it.

**Remaining gaps (deferred):** List any gaps that could not be filled because no verifiable content exists. These are the knowledgebase's known coverage limits — they should be acknowledged, not invented around.

**Verification tags resolved:** List claims confirmed and tags removed.

**Verification tags remaining:** List claims still uncertain. These are the knowledgebase's known uncertainty points.

**Orphaned files fixed:** List any files that now have inbound links.

**Duplicates resolved:** List any content consolidated.

---

When this audit is complete, the MJ expansion series is done. The knowledgebase now covers both the Jeep Cherokee XJ and Jeep Comanche MJ with the same depth and the expert agent can route correctly for both platforms.
