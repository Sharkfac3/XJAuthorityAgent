# Retooling Review

## Scope
This review validates whether the repository now supports the broader Jeep XJ knowledge goal and identifies the next highest-value structural work.

Audit inputs reviewed:
- `SKILL.md`
- `AGENTS.md`
- retooling docs under `docs/`
- current folder structure
- key canonical routers and selected legacy content needed to verify routing and migration quality

## Executive verdict
**Mostly yes, but not cleanly enough yet.**

The repo now has a credible target architecture for a full Jeep XJ knowledge system:
- the top-level taxonomy is much broader than ECU swaps
- governance and migration planning are strong
- the scaffold supports future growth across stock facts, work, diagnostics, sourcing, and restoration

However, the **active navigation layer is still split between the new architecture and the old ECU-swap identity**. A new agent can orient itself from `AGENTS.md`, but several real entrypoints and compatibility files still push the old worldview. The result is a structurally promising repo with an incomplete migration surface.

## Short answers to the required audit questions

### Can a new agent orient itself quickly?
**Yes, with friction.**

Strong points:
- `SKILL.md` and `AGENTS.md` provide a clear startup sequence.
- `docs/agent-orientation.md` reinforces the same model.
- Top-level folders now match recognizable question types.

Friction points:
- `README.md` still presents the repo as `XJ ECU Swap Book`.
- `agents/assistant/index.md` still says to always load `swap/index.md` and `vehicle/engine.md`.
- `agents/book/index.md`, `book/outline.md`, `vehicle/README.md`, `swap/README.md`, and `swap/index.md` still frame the repo around ECU swaps first.

Conclusion: orientation is strong for governance-aware agents, but inconsistent for agents or humans that enter through legacy files.

### Is the repo clearly about the Jeep XJ as a whole rather than only ECU swaps?
**At the architecture level, yes. At the live content and entrypoint level, not fully.**

Evidence for success:
- `AGENTS.md` explicitly redefines the repo as a Jeep XJ technical knowledge system.
- `docs/project-reframe.md` and `docs/repo-taxonomy.md` strongly support platform-wide scope.
- `vehicle/`, `work/`, `diagnostics/`, and `sourcing/` now exist and are sensibly separated.

Evidence of remaining ECU-swap bias:
- root `README.md`
- `swap/index.md`
- `swap/README.md`
- `agents/assistant/index.md`
- `agents/book/index.md`
- `book/outline.md`
- `vehicle/README.md`

Conclusion: the repo now *can* be about the whole XJ, but several front-door files still tell users it is mainly about ECU swaps.

### Is the taxonomy durable enough for swaps, upgrades, maintenance, diagnostics, and restoration?
**Yes.**

This is one of the strongest parts of the retooling.

Why:
- top-level ownership is clear
- stock facts vs work vs diagnostics vs sourcing are explicitly separated
- `work/` is correctly split by work class first
- migration docs preserve current canonical paths while defining future destinations
- file creation and naming rules are specific enough to support consistent growth

Weakness:
- many new branch routers are still generic scaffold text rather than branch-specific guidance, which weakens practical durability during day-to-day use

### Are top-level folders cleanly separated by purpose?
**Mostly yes.**

Clear separation now exists for:
- `vehicle/`
- `work/`
- `diagnostics/`
- `sourcing/`
- `swap/`
- `docs/`
- `skillbuilding/`
- `book/`
- `agents/`

Remaining issues:
- `swap/` still acts as an active legacy center rather than a clearly transitional branch
- `humans/` exists at the repo root but is not part of the documented architecture in `AGENTS.md` or `docs/structure-map.md`
- legacy README files still describe older domain boundaries

### Are cross-cutting topics handled explicitly?
**Yes, in governance. Partially in live content.**

Strong governance coverage exists for:
- year and era differences
- package and drivetrain splits
- donor vs stock baseline separation
- compatibility leaves
- stock vs modified-state routing

Still weak in live content because:
- major mixed-purpose files remain unsplit, especially under `vehicle/` and `swap/`
- connector content still straddles sourcing and procedure roles
- diagnostics remain hidden in era files

### Does the structure encourage deep-tree growth instead of flat-file sprawl?
**Yes.**

Evidence:
- the taxonomy strongly favors deep trees
- naming rules support durable nested paths
- migration docs recommend splitting broad mixed files into folders and leaves
- new scaffolds already exist for deeper branching

Remaining concern:
- most new routers are scaffold-only, so practical deep-tree growth will depend on replacing generic placeholder language with branch-specific next-step routing

### Are migration rules and governance strong enough to avoid future drift?
**Yes, if maintainers follow them.**

This is another strong area.

Strengths:
- migration plan is path-specific
- migration map identifies split vs move vs keep decisions
- content governance rules are explicit
- topic intake, research pipeline, and backlog seeding reduce random growth

Remaining concern:
- the repo still contains enough conflicting front-door guidance that contributors may follow old patterns unless the legacy entrypoints are updated soon

## What is working well

### 1. The domain model is now clear and expandable
`vehicle/`, `work/`, `diagnostics/`, and `sourcing/` form a durable platform-wide architecture.

### 2. Governance is unusually strong
The docs set clear rules for:
- domain ownership
- naming
- migration
- anti-duplication
- uncertainty handling
- backlog and research intake

### 3. The migration is planned, not improvised
`docs/migration-map.md` and `docs/migration-plan.md` are concrete enough to guide real follow-up work.

### 4. The scaffold supports future coverage breadth
The repo can now grow into:
- maintenance
- repairs
- restoration
- upgrades
- diagnostics
- sourcing
- major swaps beyond ECU work

## Confirmed weaknesses

### 1. Entrypoint conflict remains the biggest architecture problem
Confirmed conflicting entrypoints:
- `README.md`
- `swap/index.md`
- `swap/README.md`
- `agents/assistant/index.md`
- `agents/book/index.md`
- `vehicle/README.md`
- `book/outline.md`

These files still describe the repo as ECU-swap-centered, which undermines the new taxonomy.

### 2. Many branch routers are still template-like rather than branch-specific
Examples:
- `work/maintenance/cooling/index.md`
- `work/swaps/ecu/index.md`
- many `work/**/index.md` files
- many `diagnostics/*/index.md` files

The scaffold exists, but many routers still contain generic example child names that do not match the branch.

### 3. Important mixed-purpose legacy files still block clean routing
Confirmed examples:
- `vehicle/engine.md`
- `vehicle/trans/aw4.md`
- `vehicle/era3/diagnostics.md`
- `vehicle/era3/wiring.md`
- `swap/wiring/connectors/index.md`

These files still blur stock facts, procedures, diagnostics, or sourcing.

### 4. The top-level architecture has one undocumented extra root
`humans/` is present but not integrated into the documented top-level map. That creates avoidable ambiguity about whether it is a permanent repo domain, a temporary prompt archive, or something else.

## Possible future risks

### 1. Scaffold complacency
Risk: the presence of many routers may create a false sense of completion even though most practical branches are still empty.

### 2. Legacy-root inertia
Risk: contributors may keep treating `swap/` as the real center because mature content still lives there and several active files still tell them to do so.

### 3. Template-router drift
Risk: generic stub language may survive too long and become a second layer of low-quality routing guidance.

### 4. README divergence
Risk: humans entering through folder READMEs may receive a different mental model than agents entering through `AGENTS.md`.

## Overall judgment
The retooling succeeded at the **architecture and governance layer**.
It has **not yet fully succeeded at the active navigation and migration layer**.

The highest-value next work is not broad new content creation first. It is to:
1. unify entrypoint identity
2. clean up generic routers
3. split the most distortion-causing mixed-purpose legacy files
4. make the transitional status of `swap/` obvious in live routing

Once those are fixed, the repo will be much easier for new agents to navigate and much safer to scale.