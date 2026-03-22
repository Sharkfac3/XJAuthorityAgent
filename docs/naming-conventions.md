# Naming Conventions

This document defines durable naming rules for folders and files in the repository.

Its goal is to make placement predictable, reduce drift, and let future agents create new content without guessing.

It should be used together with:
- `docs/repo-taxonomy.md`
- `docs/routing-principles.md`

---

# 1. Naming goals

Names should:
- communicate scope before the file is opened
- remain clear as the tree grows deeper
- reflect stable distinctions in the platform and work
- reduce the need for explanatory caveats in every document
- support both human scanning and agent routing

Names should not:
- depend on local tribal knowledge
- hide whether a document is factual, procedural, or diagnostic
- collapse multiple concepts into vague buckets

---

# 2. General file and folder style

## Use lowercase kebab-case

Use lowercase with hyphens for folders and files.

Good:
- `charging-starting/`
- `fuel-pump/`
- `wj-brake-upgrade/`
- `1996-notes.md`

Avoid:
- `FuelPump/`
- `fuel_pump/`
- `Fuel Pump.md`

## Use nouns for domains and component families

Good:
- `cooling/`
- `axles/`
- `steering/`
- `interchange/`

## Use task nouns or durable action labels for work branches

Good:
- `maintenance/`
- `repairs/`
- `upgrades/`
- `swaps/`
- `setup-and-calibration/`

Avoid unstable or vague work labels like:
- `projects/`
- `jobs/`
- `mods/`
- `stuff/`

---

# 3. Folder naming rules by domain

## `vehicle/`

Use names that describe stock truth.

Good second-level names:
- `years/`
- `systems/`
- `packages/`
- `configurations/`
- `interchange-baselines/`

Good system names:
- `engine/`
- `fuel/`
- `ignition/`
- `cooling/`
- `electrical/`
- `charging-starting/`
- `transmission/`
- `transfer-case/`
- `axles/`
- `suspension/`
- `steering/`
- `brakes/`
- `body/`
- `interior/`

## `work/`

First branch by work type, then by system.

Good patterns:
- `work/maintenance/cooling/`
- `work/repairs/interior/`
- `work/upgrades/brakes/`
- `work/swaps/drivetrain/`

## `diagnostics/`

Name branches by symptom domain or affected system.

Good names:
- `cooling/`
- `fuel/`
- `charging-and-starting/`
- `body-electrical/`
- `body-and-interior/`

## `sourcing/`

Name branches by decision class first, then system or part family.

Good patterns:
- `sourcing/interchange/axles/`
- `sourcing/donor-vehicles/drivetrain/`
- `sourcing/connectors/`
- `sourcing/oem-vs-aftermarket/brakes/`

---

# 4. Overview, index, and README naming

These file names have distinct jobs and should not be used interchangeably.

## `overview.md`

Use inside a technical branch folder when the file explains:
- branch scope
- major variants
- compatibility splits
- links to child leaves

Typical use:
- `vehicle/systems/axles/dana-30/overview.md`
- `work/upgrades/brakes/wj-brake-upgrade/overview.md`

## `index.md`

Use when the file acts as a router for a domain, workflow, or agent entrypoint.

Typical use:
- `swap/index.md`
- `agents/book/index.md`
- `skillbuilding/index.md`

## `README.md`

Use for quick human orientation at a folder root.
It may overlap with `index.md`, but it should stay lightweight and introductory.

Typical use:
- top-level or major-root folder summaries

## Rule
If the file is the actual technical source for a topic, do not call it `README.md`.
Use a scope-descriptive name or `overview.md`.

---

# 5. Leaf-file naming rules

Leaf names should describe one narrow job.

## Reference leaf names

Use when the file explains factual structure or differences.

Good names:
- `overview.md`
- `compatibility.md`
- `year-changes.md`
- `specs.md`
- `variants.md`
- `sensor-baseline.md`
- `connector-families.md`

## Procedure leaf names

Use when the file explains what to do.

Good names:
- `procedure.md`
- `install.md`
- `removal.md`
- `replacement.md`
- `refresh.md`
- `bleeding.md`
- `adjustment.md`
- `post-install-checks.md`
- `validation.md`

## Troubleshooting leaf names

Use when the file explains how to isolate a fault.

Good names:
- `no-start.md`
- `overheating-at-idle.md`
- `low-charging-voltage.md`
- `intermittent-cutout.md`
- `hard-shift.md`
- `door-lock-failure.md`

## Selection and sourcing leaf names

Use when the file helps choose parts or donors.

Good names:
- `donor-options.md`
- `kit-selection.md`
- `oem-vs-aftermarket.md`
- `required-parts.md`
- `connector-sourcing.md`

---

# 6. Naming stock baseline vs modified-state content

## Stock baseline names

Use neutral names that describe the factory system.

Good:
- `vehicle/systems/transmission/aw4/overview.md`
- `vehicle/systems/axles/chrysler-8.25/year-changes.md`
- `vehicle/packages/up-country/suspension.md`

Avoid names that imply modification or recommendation in stock files.

Bad:
- `best-aw4-options.md`
- `chrysler-8.25-upgrade.md`

## Modified-state names

Use names that describe the project or changed state.

Good:
- `work/upgrades/electrical/alternator-upgrade/overview.md`
- `work/swaps/drivetrain/ls-swap/overview.md`
- `work/upgrades/driveline/sye/compatibility.md`

---

# 7. Naming upgrades vs swaps

The distinction must be visible in the path.

## Upgrade naming

Use for improved or altered versions of the same general system role.

Good:
- `work/upgrades/brakes/wj-brake-upgrade/`
- `work/upgrades/electrical/alternator-upgrade/`
- `work/upgrades/driveline/sye/`

## Swap naming

Use when the identity of the assembly, donor family, or control architecture changes materially.

Good:
- `work/swaps/ecu/`
- `work/swaps/drivetrain/ls-swap/`
- `work/swaps/axles/dana-44-into-xj/`
- `work/swaps/steering/steering-box/`

## Rule
If readers would naturally ask “what donor or architecture is being swapped in,” use swap naming.
If readers would naturally ask “what improved version of the existing system is being installed,” use upgrade naming.

---

# 8. Naming year, era, and compatibility splits

## Era names

Use stable era labels where the repo already relies on them.

Good:
- `era1/`
- `era2/`
- `era3/`

## Year-specific files

Use exact years when the difference is real.

Good:
- `1996-notes.md`
- `2000-2001-coil-rail.md`
- `1991-transition-notes.md`

## Range naming

Use compact, accurate ranges when one file genuinely covers a stable span.

Good:
- `1997-1999-refresh-notes.md`
- `2000-2001-ignition-differences.md`

Avoid broad range names if the file still needs many exceptions.
In that case, split further.

## Compatibility leaf names

Use `compatibility.md` when the folder already provides the topic scope.

Example:
- `work/upgrades/brakes/wj-brake-upgrade/compatibility.md`

Use scope-specific compatibility names when multiple compatibility documents exist.

Examples:
- `year-compatibility.md`
- `transmission-compatibility.md`
- `abs-compatibility.md`

---

# 9. Naming package, drivetrain, and variant splits

## Packages

Use the recognized package name in kebab-case.

Good:
- `up-country/`
- `towing-package/`

## Drivetrain and transmission splits

Use concise technical labels.

Good:
- `2wd/`
- `4wd/`
- `manual/`
- `automatic/`
- `aw4/`
- `ax15/`

## Axle and component families

Use the common family name that XJ readers will recognize.
Normalize punctuation to kebab-case.

Good:
- `dana-30/`
- `chrysler-8-25/` or `chrysler-8.25/`
- `np231/`
- `np242/`

## Consistency rule for component-family names

Choose one normalized form and use it everywhere in paths.
For decimal-like axle names, prefer a single convention repo-wide.

Recommended:
- `chrysler-8-25/`

Reason:
- it avoids punctuation ambiguity in paths while staying readable

If the repo already uses a different normalized component-family convention, migration should standardize it once rather than allowing mixed variants.

---

# 10. Naming procedure stacks inside topic folders

When a topic grows into a folder, use a predictable internal file set.

## Recommended pattern for project folders

```text
<topic>/
  overview.md
  compatibility.md
  required-parts.md
  procedure.md
  post-install-checks.md
  troubleshooting.md   # only if topic-local troubleshooting is truly needed
```

## Recommended pattern for stock reference folders

```text
<component-family>/
  overview.md
  year-changes.md
  variants.md
  specs.md
```

## Recommended pattern for diagnostic folders

```text
<component-or-symptom>/
  overview.md          # optional, only if branch selection is needed
  no-start.md
  intermittent-failure.md
  low-output.md
```

---

# 11. Names to avoid

Do not create new files or folders with vague names.

Avoid:
- `misc/`
- `general/`
- `notes/`
- `other/`
- `random/`
- `temp/`
- `new/`
- `old/`
- `v2/`
- `final/`
- `stuff/`

Avoid ambiguous file names like:
- `info.md`
- `details.md`
- `guide.md` when the guide type is unclear
- `basics.md` unless there is a clearly defined beginner branch

## Exception rule
A file may use `notes.md` only when paired with a specific scope that represents an actual exception class, such as:
- `1996-notes.md`
- `transition-notes.md`

Even then, prefer a more descriptive name if possible.

---

# 12. Naming rules for routers and summaries

## Small router naming

Use `index.md` for:
- domain routers
- workflow routers
- agent entrypoints

Use `overview.md` for:
- local branch routers in technical content trees

## Summary rule
Routers should summarize and point.
They should not become large technical fact dumps.

If a router accumulates major technical detail, split that detail into named leaves such as:
- `compatibility.md`
- `year-changes.md`
- `required-parts.md`
- `procedure.md`

---

# 13. Naming examples

## Good examples
- `vehicle/systems/transmission/aw4/overview.md`
- `vehicle/systems/axles/dana-30/year-changes.md`
- `vehicle/packages/up-country/suspension.md`
- `work/maintenance/cooling/system-refresh/procedure.md`
- `work/repairs/interior/headliner-repair/procedure.md`
- `work/upgrades/brakes/wj-brake-upgrade/required-parts.md`
- `work/swaps/drivetrain/ls-swap/compatibility.md`
- `diagnostics/fuel/fuel-pump/no-prime.md`
- `diagnostics/body-electrical/door-wiring/intermittent-failure.md`
- `sourcing/interchange/electrical/alternator-donor-options.md`

## Bad examples
- `vehicle/aw4-notes.md`
- `work/brakes/wj.md`
- `diagnostics/electrical/problems.md`
- `sourcing/parts/good-choices.md`
- `vehicle/misc/axle-stuff.md`

---

# 14. Naming checklist for new content

Before creating a new file or folder, confirm:

1. Does the name reveal the domain?
2. Does the path reveal stock fact vs procedure vs troubleshooting vs sourcing?
3. Does the name reveal the system or component family?
4. Does the path reveal whether the topic is an upgrade or a swap?
5. If compatibility matters, is that reflected in either the path or a dedicated leaf name?
6. Could a new agent place or find this topic without knowing repo history?
7. Did you avoid vague bucket names?

If any answer is no, rename before adding content.

---

# 15. Summary

Use names that are:
- stable
- explicit
- narrow
- system-aware
- work-type-aware
- compatibility-aware when needed

The path should do most of the explanatory work.
A future agent should be able to guess where a new topic belongs, and what a file contains, from the naming system alone.
