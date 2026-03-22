# Agent Architecture

## Purpose
This repo is now organized around a central Markdown knowledge base that multiple agents can consume.

## Shared knowledge base
All reusable Jeep XJ and ECU-swap knowledge should live in nested Markdown under:
- `vehicle/` — stock Jeep/XJ facts
- `swap/` — ECU-swap procedure and decision knowledge
- `book/` — presentation rules used by the Book agent

These folders are the central repository.
They are designed to stay deeply nested so agents can load the narrowest truthful file for a question.

## Agent homes
Each user-facing agent should have its own folder under `agents/`.

Current agent homes:
- `agents/book/`
- `agents/assistant/`

Each agent home should expose:
- `README.md` — quick purpose and entrypoint
- `index.md` — the actual routing prompt for that agent

## Legacy prompts
The existing top-level files under `agents/` remain valid helpers during migration:
- `writer.md`
- `reviewer.md`
- `technical.md`
- `wiring.md`
- `tuning.md`

These should be treated as reusable specialist prompts that agent homes can call into.

## Design rule
Agent folders define behavior.
The central Markdown repository defines facts.
Do not move Jeep facts into agent prompts.

## Near-term direction
- Keep the Book agent using the current book-writing stack
- Add new operational agents as folders under `agents/`
- Let all agents share the same canonical Markdown repository instead of branching duplicate knowledge stores
