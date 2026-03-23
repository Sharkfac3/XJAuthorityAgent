# ABS Vs Non-ABS

## Purpose
Provide the stock baseline split for XJs where anti-lock brake system presence changes the safe answer.

## Scope
Use this file before assuming brake hydraulic layout, axle-side brake hardware details, warning-light expectations, or bleeding / diagnosis paths that may differ when ABS is present.

## Core rule
Do not assume an XJ is non-ABS just because the question starts as a generic brake complaint.
ABS presence can change the stock brake-system baseline enough that the expert agent should confirm it before giving detailed brake, axle, or sourcing guidance.

## When ABS status matters most
ABS status is a first-hop filter when the question involves:
- brake hydraulic architecture
- brake warning lights or ABS-specific fault indicators
- axle or brake-hardware interchange questions
- bleeding, repair, or post-repair verification paths
- parts ordering where sensor, tone-ring, or brake-family assumptions may change

## Where to route next
- stock brake baseline: [`../systems/brakes/overview.md`](../systems/brakes/overview.md)
- brake diagnostics: [`../../diagnostics/brakes/index.md`](../../diagnostics/brakes/index.md)
- brake maintenance and repair: [`../../work/maintenance/brakes/index.md`](../../work/maintenance/brakes/index.md), [`../../work/repairs/brakes/index.md`](../../work/repairs/brakes/index.md)
- stock interchange baselines when brake-family fitment matters: [`../interchange-baselines/index.md`](../interchange-baselines/index.md)

## What this file can answer now
This file establishes that ABS presence is a required narrowing dimension for many brake answers.
It is the right first stop when the expert agent needs to decide whether a brake, axle, or parts answer is safe without overcommitting to a non-ABS assumption.

## Current limits
Current canon does **not** yet include:
- a full year-by-year ABS availability map
- a complete ABS hardware-family breakdown
- brake-family leaves that fully separate ABS and non-ABS stock parts

When the exact stock hardware is still uncertain, say so explicitly and confirm the vehicle configuration before giving a narrow answer.

## Cross-links
- Configuration routing root: [`index.md`](index.md)
- Engine and transmission combinations: [`engine-trans-combinations.md`](engine-trans-combinations.md)
- 2WD vs 4WD baseline: [`2wd-vs-4wd.md`](2wd-vs-4wd.md)
