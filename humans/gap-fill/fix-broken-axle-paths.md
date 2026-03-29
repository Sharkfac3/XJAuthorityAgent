# Gap Fill: Fix Broken Relative Paths in Axle Swap Docs

Copy and paste the prompt below into a new chat session with the Knowledgebase Builder agent active.

---

You are the Knowledgebase Builder for this repository.

Start by reading `AGENTS.md`, then `agents/knowledgebase-builder.md`.

Your task is narrow and surgical: fix broken relative paths in the axle swap documentation. Do not add or remove content — only fix paths.

## Known broken files

All files in `work/swaps/axles/` use `../../../` to reach the repo root when they need `../../../../`. The target files all exist — the paths are just wrong.

Fix every cross-reference link in these files:
- `work/swaps/axles/one-ton-front/index.md`
- `work/swaps/axles/one-ton-front/housing-prep.md`
- `work/swaps/axles/one-ton-front/steering-conversion.md`
- `work/swaps/axles/one-ton-rear/index.md`
- `work/swaps/axles/one-ton-rear/housing-prep.md`
- `work/swaps/axles/support-work/index.md`
- `work/swaps/axles/support-work/driveshaft-work.md`
- `work/swaps/axles/support-work/gearing-install.md`
- `work/swaps/axles/support-work/lift-and-clearance.md`

Also fix this separate path error:
- `work/swaps/ecu/wiring/platform-specific/speeduino-ocelot/index.md` — uses `../../../../ecu-selection/` when it should be `../../../ecu-selection/`

After fixing, verify each corrected path resolves to a file that actually exists. Report any targets that are still missing after the path is corrected.
Also be sure to triple check information with online sources as you work.