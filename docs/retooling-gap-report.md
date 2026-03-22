# Retooling Gap Report

## Purpose
Path-specific audit of remaining architecture, routing, migration, and expansion weaknesses after the retooling effort.

## Severity scale
- **High** — actively distorts navigation or encourages wrong placement now
- **Medium** — structurally weak or incomplete, but not yet causing major drift everywhere
- **Low** — future risk or cleanup item

## Confirmed issues

### G1. Root identity still conflicts with the reframe
**Severity:** High

**Paths**
- `README.md`
- `swap/README.md`
- `swap/index.md`
- `vehicle/README.md`
- `agents/assistant/index.md`
- `agents/book/index.md`
- `book/outline.md`

**Observed problem**
These files still describe the repo as primarily an ECU swap project or instruct agents to load swap-first paths by default.

**Why it matters**
A new agent or human can get two different answers to “what is this repo?” depending on where they enter.

**Impact**
- weakens the broader Jeep XJ identity
- encourages legacy-root inertia
- undermines the domain-classification-first routing model

**Recommended correction**
Update all front-door files so they consistently present:
- repo identity as full Jeep XJ technical knowledge system
- `swap/` as a transitional but still-canonical ECU branch
- domain classification before branch loading

---

### G2. Agent entrypoints are not yet aligned with the new routing model
**Severity:** High

**Paths**
- `agents/assistant/index.md`
- `agents/book/index.md`

**Observed problem**
`agents/assistant/index.md` still says to always load `swap/index.md` and `vehicle/engine.md`.
`agents/book/index.md` still assumes an ECU-swap-book workflow and leans on legacy helper prompts.

**Why it matters**
These files are active behavior surfaces. If they lag behind governance, the repo will behave as if the migration never happened.

**Impact**
- new agents may route incorrectly
- non-swap work is treated as secondary even when the repo now supports it
- book behavior remains tied to one deliverable identity

**Recommended correction**
Revise both agent routers to:
- classify by question type first
- load domain routers first
- treat ECU swap content as one branch, not the default branch

---

### G3. Folder READMEs are now a drift source
**Severity:** High

**Paths**
- `README.md`
- `vehicle/README.md`
- `swap/README.md`
- `agents/README.md`
- `book/README.md`
- `skillbuilding/README.md`

**Observed problem**
The repo now has a stronger `index.md`-based routing model, but several README files still reflect older assumptions or duplicate router work without a clear synchronization rule.

**Why it matters**
Humans may enter through README files while agents enter through `index.md` or `AGENTS.md`. If those differ, the repo has split navigation.

**Impact**
- human/agent navigation divergence
- harder maintenance burden
- likely future drift if both file types keep evolving separately

**Recommended correction**
Choose one policy and apply it consistently:
- either `index.md` is canonical and README files are lightweight mirrors
- or README files are removed where they duplicate routers

---

### G4. Many new routers are generic templates, not real branch routers
**Severity:** High

**Paths**
Representative examples:
- `work/maintenance/cooling/index.md`
- `work/swaps/ecu/index.md`
- `work/repairs/engine/index.md`
- `work/restoration/interior/index.md`
- `work/setup-and-calibration/ecu/index.md`
- `diagnostics/cooling/index.md`
- `diagnostics/brakes/index.md`
- `diagnostics/body-and-interior/index.md`

**Observed problem**
Many routers use generic example child names that do not fit the branch, such as:
- `system-refresh/`
- `headliner-repair/`
- `wj-brake-upgrade/`
- `ls-swap/`

or generic symptom examples repeated across all diagnostics branches:
- `no-start.md`
- `intermittent-failure.md`
- `low-output.md`
- `overheating-at-idle.md`

**Why it matters**
These files look complete enough to trust, but they do not yet provide branch-specific routing intelligence.

**Impact**
- lowers agent confidence in local routing
- encourages copy-forward scaffolding instead of system-aware routing
- weakens deep-tree growth because local branches do not yet advertise their true likely children

**Recommended correction**
Replace template examples with branch-true examples, even if still lightweight.

---

### G5. Major mixed-purpose legacy files remain in active canonical use
**Severity:** High

**Paths**
- `vehicle/engine.md`
- `vehicle/trans/aw4.md`
- `vehicle/trans/manual.md`
- `vehicle/era1/diagnostics.md`
- `vehicle/era2/diagnostics.md`
- `vehicle/era3/diagnostics.md`
- `vehicle/era1/wiring.md`
- `vehicle/era2/wiring.md`
- `vehicle/era3/wiring.md`
- `swap/wiring/connectors/index.md`

**Observed problem**
These files still mix categories the new taxonomy intends to separate.

Examples:
- `vehicle/trans/aw4.md` mixes stock baseline and swap integration guidance
- `vehicle/era3/diagnostics.md` mixes diagnostics and pre-swap inspection workflow
- `vehicle/era3/wiring.md` mixes stock wiring facts with swap-adaptation pointers
- `swap/wiring/connectors/index.md` behaves like sourcing/reference more than procedure

**Why it matters**
These files are where new contributors are most likely to copy old placement behavior.

**Impact**
- keeps routing blurry
- blocks clean migration into `vehicle/`, `diagnostics/`, `work/`, and `sourcing/`
- preserves old mixed-purpose writing patterns

**Recommended correction**
Execute the first split wave from `docs/migration-map.md`, starting with the highest-distortion files.

---

### G6. `swap/` is documented as transitional in governance, but still behaves like a primary root in live navigation
**Severity:** High

**Paths**
- `swap/index.md`
- `swap/README.md`
- `work/index.md`
- `work/swaps/ecu/index.md`

**Observed problem**
Governance says `swap/` is legacy-but-current during migration, but live files still frame it as the repo's central workflow.

**Why it matters**
This is the core migration contradiction.

**Impact**
- agents may continue adding conceptual weight to `swap/`
- new content authors may hesitate to use `work/`
- the transition to `work/swaps/ecu/` remains theoretical

**Recommended correction**
Make `work/swaps/ecu/` the clearly preferred target in live routing and downgrade `swap/` to explicit compatibility-router language.

---

### G7. `humans/` is an undocumented top-level root
**Severity:** Medium

**Paths**
- `humans/README.md`
- `humans/01-project-reframe-and-target-state.md`
- `humans/02-taxonomy-and-routing-redesign.md`
- `humans/03-deep-tree-scaffold-buildout.md`
- `humans/04-existing-content-migration-plan.md`
- `humans/05-agent-orientation-and-governance-refresh.md`
- `humans/06-research-intake-and-expansion-system.md`
- `humans/07-validation-gap-audit-and-next-steps.md`

**Observed problem**
This root exists physically but is not reflected in the documented top-level architecture.

**Why it matters**
Undocumented roots create taxonomy ambiguity and can become accidental long-term storage.

**Impact**
- unclear whether this is permanent or transitional
- weakens the small-number-of-durable-roots rule
- invites future confusion about where prompt artifacts belong

**Recommended correction**
Either:
- document `humans/` as a temporary process-artifact root, or
- relocate/archive it under a documented meta branch such as `skillbuilding/` or `docs/` if that better matches its job

---

### G8. Book-layer migration is unfinished
**Severity:** Medium

**Paths**
- `book/outline.md`
- `agents/book/index.md`

**Observed problem**
The presentation layer still assumes one project-specific deliverable: an ECU swap book.

**Why it matters**
This is not fatal, but it keeps the book layer narrower than the repo's new mission.

**Impact**
- presentation rules are partly generic and partly project-specific
- future human-facing deliverables may not have a clear home

**Recommended correction**
Move project-specific book artifacts into a scoped project branch and keep root `book/` files presentation-generic.

---

### G9. Some migration decisions remain intentionally unresolved, but the live repo gives no short operational convention for them
**Severity:** Medium

**Paths**
- `docs/migration-plan.md`
- `docs/migration-map.md`
- `vehicle/years/index.md`

**Observed problem**
The docs correctly note unresolved decisions such as:
- exact `1996-notes.md` placement
- helper-agent path conventions
- eventual home for broader setup/calibration content

But there is no short “current convention” file summarizing which decisions are locked vs pending.

**Why it matters**
Maintainers may need to read several governance docs to discover what is still provisional.

**Impact**
- avoidable decision churn
- possible inconsistent file creation during the interim

**Recommended correction**
Add a short transition-status note or decision register in `docs/`.

---

### G10. The scaffold is broad, but high-value first content branches are still mostly empty
**Severity:** Medium

**Paths**
Representative branches:
- `work/maintenance/*`
- `diagnostics/*`
- `sourcing/*`
- `vehicle/systems/*`

**Observed problem**
The structure exists, but many practical branches only contain routers.

**Why it matters**
The repo now scales structurally, but still relies heavily on legacy ECU material for real-world usefulness.

**Impact**
- broader mission is credible in form more than in coverage
- users outside ECU work may reach stubs quickly but not answers quickly

**Recommended correction**
Build the first few high-value branch packages in maintenance, diagnostics, stock baselines, and sourcing before broadening further.

## Future risks

### R1. Placeholder language may become pseudo-canon
If generic routers are not tightened soon, future agents may treat template examples as branch guidance.

### R2. Legacy files may continue to attract new detail
If mixed files stay active too long, contributors may keep enriching them instead of splitting them.

### R3. Humans and agents may diverge in repo understanding
If README files, `AGENTS.md`, and branch indexes keep drifting, the repo will have multiple competing entry models.

### R4. The broad architecture may outpace evidence-backed content
The repo now has room for many branches; without disciplined prioritization, the result could be elegant emptiness.

## Strong areas with no major gap finding
- `AGENTS.md` as the main repo router
- top-level domain separation in governance docs
- migration planning quality
- file creation and naming rules
- research intake and backlog system
- explicit anti-drift rules

## Highest-value gap cluster
The most important gap cluster is **not missing folders**.
It is the mismatch between:
- strong new governance
- strong new scaffold
- stale live entrypoints and unsplit legacy content

That cluster should be addressed before large-scale branch fill-out.