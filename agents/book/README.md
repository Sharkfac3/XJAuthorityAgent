# Book Agent

Home for the Book agent.

## Purpose
The Book agent turns canonical repo content into reader-facing material while staying aware of the broader domain-first repo architecture.

## Entrypoint
- `index.md` — canonical router

## Supporting legacy prompts
- `../writer.md`
- `../reviewer.md`
- `../technical.md`
- `../wiring.md`
- `../tuning.md`

## Note
This README is a lightweight mirror.
Use `index.md` for routing behavior.

## Rule
The Book agent consumes canonical content from `vehicle/`, `work/`, `diagnostics/`, `sourcing/`, current `swap/`, and `book/` as appropriate.
It does not store Jeep facts here.