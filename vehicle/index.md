# Vehicle Index

## Purpose
Route the expert agent to canonical stock Jeep XJ and MJ facts.

## Use this branch when
The main question is about what the XJ or MJ came with, how a factory system is arranged, or what changed by year, era, package, or configuration.

## First-hop loading path
- **Year or control-system split matters first** → [`vehicle/years/index.md`](years/index.md)
- **Subsystem identity matters first** → [`vehicle/systems/index.md`](systems/index.md)
- **Factory package or trim changes the answer** → [`vehicle/packages/index.md`](packages/index.md)
- **A stock configuration matrix is needed** → [`vehicle/configurations/index.md`](configurations/index.md)
- **A factual stock interchange limit is needed** → [`vehicle/interchange-baselines/index.md`](interchange-baselines/index.md)

## High-value live stock files
- Engine family baseline: [`vehicle/engine.md`](engine.md)
- Era 1 / Renix baseline: [`vehicle/era1/overview.md`](era1/overview.md)
- Era 2 / SBEC baseline: [`vehicle/era2/overview.md`](era2/overview.md)
- Era 3 / JTEC baseline: [`vehicle/era3/overview.md`](era3/overview.md)
- Transmission family baseline: [`vehicle/systems/transmission/overview.md`](systems/transmission/overview.md)

## What belongs here
- year and era differences
- stock subsystem architecture
- package and configuration baselines
- factual interchange baselines for stock parts
- factory hardware changes and compatibility boundaries

## What does not belong here
- step-by-step work procedures
- symptom-first diagnostics trees
- donor buying advice or kit recommendations
- agent operating instructions

## Boundary links
- How to do the job: [`work/index.md`](../work/index.md)
- What to test next: [`diagnostics/index.md`](../diagnostics/index.md)
- What to buy or pull: [`sourcing/index.md`](../sourcing/index.md)
- Swap execution (ECU, axle, engine, etc.): [`../work/swaps/`](../work/swaps/)
