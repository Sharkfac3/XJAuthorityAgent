# 4.0L Engine Date Codes

## Purpose
Decode the engine build date stamp on the 4.0L inline-six to identify manufacturing date and engine specification.

## Location
Passenger side of the engine block, just **forward and up from the distributor**, on a machined flat surface.

---

## Code format

Seven characters: `YYMTTTDD`

| Position | Digits | Meaning |
|----------|--------|---------|
| 1 | 1st | Year (single digit — e.g., 8 = 1998) |
| 2–3 | 2nd & 3rd | Month (01–12) |
| 4–5 | 4th & 5th | Engine type / fuel system / compression ratio |
| 6–7 | 6th & 7th | Day of build (01–31) |

---

## Engine type codes

| Code | Engine | Displacement | Compression | Fuel system |
|------|--------|-------------|-------------|-------------|
| MX | 4.0L | 242 CID | 8.7:1 | Multi-point fuel injection |

---

## Example

**`801MX12`**
- **8** = 1998
- **01** = January
- **MX** = 4.0L / 242 CID / 8.7:1 / multi-point fuel injection
- **12** = 12th day

→ Built January 12, 1998

---

## See also
- `vehicle/era1/overview.md` — Renix-era engine identity
- `vehicle/era2/` — HO era engine context
- `work/swaps/engine/ho-into-renix.md` — engine swap compatibility

## Source
Cruiser54 — cruiser54.com, "4.0L Engine Date Codes"
