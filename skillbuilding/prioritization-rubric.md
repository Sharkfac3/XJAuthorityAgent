# Prioritization Rubric

Use this file to rank likely gaps, confirmed gaps, and backlog items consistently.

## Purpose
Not all missing information should be tackled in the order it is discovered.
This rubric helps the project choose the next best work by swap value, risk reduction, and dependency leverage.

## Scoring dimensions
Score each item from 0 to 3.

### 1. Swap-blocking severity
- `0` — not swap-relevant
- `1` — useful but non-blocking
- `2` — causes major friction or likely rework
- `3` — can stop a real swap outright

### 2. Wrong-decision risk
- `0` — unlikely to mislead
- `1` — low-impact confusion
- `2` — can cause incorrect parts/config choices
- `3` — can cause miswiring, no-start, damage, or unsafe behavior

### 3. Year/era ambiguity risk
- `0` — no meaningful split
- `1` — minor range nuance
- `2` — era split matters
- `3` — year-specific exception likely matters materially

### 4. Dependency leverage
- `0` — mostly isolated
- `1` — helps one nearby doc
- `2` — unlocks several related docs
- `3` — foundational for many docs/workflows

### 5. Reader confusion reduction
- `0` — little clarity gained
- `1` — modest improvement
- `2` — major clarity gain
- `3` — removes a persistent confusion point

### 6. Evidence feasibility
- `0` — currently hard to validate
- `1` — possible but expensive/slow
- `2` — realistic with focused work
- `3` — can likely be resolved quickly with available sources

## Interpretation
- `14–18` → do soon
- `9–13` → important, schedule next
- `4–8` → useful but lower urgency
- `0–3` → defer unless it supports another task

## Tie-breakers
When two items score similarly, prefer:
1. the item with higher safety/reliability impact
2. the item that clarifies year/era splits
3. the item with stronger dependency leverage
4. the item with faster evidence path

## Use with other files
- classify the gap with `skillbuilding/gap-taxonomy.md`
- compare against likely high-risk areas in `skillbuilding/critical-unknowns.md`
- convert high-scoring items into backlog work with `skillbuilding/agents/backlog-architect.md`
