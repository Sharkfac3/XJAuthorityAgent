# Follow-up Prompt: Expand One-Ton Axle Coverage

Use this prompt with the knowledgebase-builder agent to expand one-ton axle coverage beyond the 05+ Ford Super Duty donor family.

---

## Current state
The repo has full coverage of 2005+ Super Duty one-ton axle swaps:
- Dana 60 front (donor ID, fitment, and full swap execution)
- Sterling 10.50 rear (donor ID, fitment, and full swap execution)
- Support work: gearing, driveshafts, lift/clearance

## Expansion candidates

### GM 14-bolt rear axle
- AAM 10.5" (GM 14-bolt SF) from 2001+ GM 2500HD/3500 trucks
- Full-float and semi-float variants
- Common alternative to the Sterling for builders who prefer GM donors or have access to GM trucks
- Files to create:
  - `sourcing/donor-vehicles/axles/gm-14-bolt.md`
  - `sourcing/interchange/axles/gm-14-bolt-fitment.md`
  - Possible execution leaves under `work/swaps/axles/one-ton-rear/` (much of the procedure is shared with Sterling — evaluate whether to add variant notes to existing files or create separate leaves)

### Military Dana 60 front axle
- Closed-knuckle, kingpin design from M715, CUCV, and similar military vehicles
- Significantly different from the 05+ Super Duty ball-joint Dana 60
- Narrower donor options, different knuckle/hub/steering geometry
- Files to create:
  - `sourcing/donor-vehicles/axles/military-dana-60.md`
  - `sourcing/interchange/axles/military-dana-60-fitment.md`
  - May need separate execution leaves due to kingpin-specific procedures

### Older Ford Dana 60 (pre-2005)
- 1999–2004 Super Duty Dana 60 — similar but some differences in knuckle and housing design
- Kingpin models from older F-250/F-350 (pre-1999)
- Evaluate whether these warrant separate donor/fitment files or can be addressed with variant notes in the existing 05+ files

## How to execute
1. Start the knowledgebase-builder agent
2. Read `AGENTS.md` and `agents/knowledgebase-builder.md`
3. Review the existing one-ton structure under `work/swaps/axles/`, `sourcing/interchange/axles/`, and `sourcing/donor-vehicles/axles/`
4. Create new donor and fitment files following the same patterns as the Super Duty files
5. Update index files to include the new children
6. Evaluate whether execution procedures need separate leaves or variant notes in existing files
