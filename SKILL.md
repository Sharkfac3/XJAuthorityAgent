---
name: xj-swap-book
description: Use this skill for all work on the Jeep XJ open source ECU swap book. Load at the start of every session. Contains no facts — routes to the correct file for any task.
---

# XJ ECU Swap Book — Agent Routing Index

## What this project is
A DIY book for mechanically capable Jeep XJ owners (1988–2001, 4.0L I6) on replacing the stock ECU with an open source engine management system. Written for a human reader who is not an engineer. Built by AI agents pulling from this knowledge base.

## Folder map

| Folder | What lives there |
|---|---|
| `agents/` | Agent role definitions — what each agent does and which files it loads |
| `vehicle/` | XJ-specific facts — engine, transmissions, all three ECU eras |
| `swap/` | How to do the swap — ECU selection, wiring, tuning |
| `book/` | What we're building — outline, audience, writing standards |

## Load by task

| Task | Load these files |
|---|---|
| Writing any chapter section | `book/writing/style.md` + `book/writing/callouts.md` + `book/audience.md` |
| Any Era 1 (Renix) topic | `vehicle/era1/overview.md` + relevant leaf file |
| Any Era 2 (OBD-I) topic | `vehicle/era2/overview.md` + relevant leaf file |
| Any Era 3 (OBD-II) topic | `vehicle/era3/overview.md` + relevant leaf file |
| Sensor spec for any era | `vehicle/eraX/sensors/[sensor].md` |
| Connector identification | `swap/wiring/connectors/index.md` → relevant family folder |
| ECU selection | `swap/ecu-selection/requirements.md` + platform file |
| Wiring procedure | `swap/wiring/grounds.md` + `swap/wiring/harness.md` + era overview |
| Tuning procedure | `swap/tuning/[topic].md` |
| AW4 automatic trans | `vehicle/trans/aw4.md` |
| Agent role definitions | `agents/[role].md` |

## Era quick reference

| Era | Years | ECU | Key file |
|---|---|---|---|
| 1 — Renix | 1988–1990 | Renix | `vehicle/era1/overview.md` |
| 2 — OBD-I | 1991–1995 | Chrysler SBEC | `vehicle/era2/overview.md` |
| 3 — OBD-II | 1996–2001 | Chrysler JTEC | `vehicle/era3/overview.md` |

⚠️ 1996 is a transition year — OBD-II ECU with OBD-I era sensors and harness. See `vehicle/era3/1996-notes.md`.
