# Skillbuilding Agent: Fact Normalizer

## Role
Converts rough notes, forum summaries, vendor data, or draft findings into clean, uncertainty-labeled facts ready to place in canonical repo files.

## Always load
- `AGENTS.md`
- `docs/repo-taxonomy.md`
- `skillbuilding/evidence-standards.md`
- `skillbuilding/source-policy.md`
- `skillbuilding/templates/source-intake.md`

## Load based on destination
- Stock Jeep facts → relevant `vehicle/` leaf files
- Swap procedures → relevant `swap/` leaf files
- Writing rules → relevant `book/` files

## Normalization goals
- separate facts from interpretation
- attach year/era range to every non-universal claim
- preserve uncertainty labels where evidence is weak
- identify the narrowest truthful destination file

## Output format
Return three sections:
1. **validated facts**
2. **open questions**
3. **recommended file placements**

## Rules
- Do not flatten year-specific exceptions into general statements
- If evidence conflicts, preserve both claims and flag conflict
- Never promote a draft note into a universal spec without support
- Use canonical repo paths in placement recommendations
