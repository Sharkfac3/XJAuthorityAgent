# Pigtail Vs Rehousing

## Purpose
Help XJ owners decide whether a damaged connector should be repaired by rebuilding the original shell or by replacing it with a pigtail-style harness end.

## Scope
This is a sourcing decision file.
It helps choose a repair path and repair parts.
It does not teach the full repinning or splice procedure.

## Use this file when
- the connector body is damaged or heat-cycled
- terminal condition is questionable and service parts may or may not exist
- you need to decide whether to preserve the stock shell or replace the harness end
- the next step is ordering repair parts, not doing the wiring work yet

## Rehousing is usually the better first choice when
- the connector body is intact and still locks positively
- the correct terminals, seals, and cavity plugs are available
- wire length is limited and you want to avoid adding splices
- the stock connector family is common enough that service parts are realistic

## A pigtail is usually the better first choice when
- the shell is cracked, melted, or no longer retains terminals correctly
- locking features are broken
- the original terminal family is too scarce or too damaged to rebuild confidently
- prior repairs have already shortened or contaminated the harness end
- the connector family is old enough that service parts are harder to trust than a complete replacement end

## Renix-era caution
Renix-native connector families are a common case where repair choices get harder.
Before ordering service parts, load the legacy family canon here:
- [`swap/wiring/connectors/renix-native/overview.md`](../../swap/wiring/connectors/renix-native/overview.md)
- [`swap/wiring/connectors/renix-native/cts.md`](../../swap/wiring/connectors/renix-native/cts.md)
- [`swap/wiring/connectors/renix-native/map.md`](../../swap/wiring/connectors/renix-native/map.md)
- [`swap/wiring/connectors/renix-native/tps.md`](../../swap/wiring/connectors/renix-native/tps.md)

Those files already show several cases where modern sensor substitution or complete pigtail replacement is more realistic than preserving a brittle original shell.

## Metri-Pack, EV, and other serviceable families
For later connector families that still have widely available service parts, rebuilding the original shell often stays attractive when the body itself is still healthy.
Start with the family overview under [`swap/wiring/connectors/index.md`](../../swap/wiring/connectors/index.md), then decide whether terminals-and-seals service is realistic or whether a pigtail is still the cleaner repair.

## How to make the decision quickly
Ask these questions in order:
1. Is the shell physically sound?
2. Are the locking features intact?
3. Are the correct service terminals and seals realistically available?
4. Would rebuilding leave enough clean wire length and confidence for a durable repair?
5. Is the vehicle better served by preserving stock appearance or by maximizing serviceability?

If several answers are no, a pigtail is usually the safer buy.

## Route after the decision
- If you are preserving the stock harness and shell, continue to [`work/restoration/wiring/index.md`](../../work/restoration/wiring/index.md) for restoration-side work.
- If you need connector-family identification first, continue to [`swap/wiring/connectors/index.md`](../../swap/wiring/connectors/index.md).
- If the repair is now about donor or interchange choices, continue to [`sourcing/interchange/electrical/index.md`](../interchange/electrical/index.md).

## Next likely child leaves
- `terminal-and-seal-families.md`
- `engine-management-connectors/overview.md`
- `body-electrical-connectors/overview.md`
