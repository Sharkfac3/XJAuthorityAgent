# ECU Selection: XJ and MJ 4.0L Requirements

## Minimum I/O for any era

| Function | Type | Count | Notes |
|---|---|---|---|
| Injector outputs | Low-side digital out | 6 | Sequential preferred; 3 for batch fire |
| Ignition output | Digital out | 1 (Era 1/2, Era 3 pre-2000) or 3 (Era 3 2000–2001 coil rail) | |
| Crank trigger input | VR input | 1 | All eras use VR crank sensor |
| Cam sync input | Hall input | 1 | All eras require cam sync |
| TPS input | 0–5V analog in | 1 | |
| MAP input | 0–5V analog in | 1 | Internal or external 1-bar |
| CTS input | Thermistor analog in | 1 | |
| IAT input | Thermistor analog in | 1 | |
| O2 input (narrowband) | 0–1V analog in | 1 | Closed-loop operation |
| IAC output | 4-wire stepper out | 1 | Or PWM out if valve is swapped |
| Fuel pump / ASD relay | Digital out (low-side) | 1 | |
| Tachometer output | Digital out | 1 | Optional — to instrument cluster |

## Strongly recommended extras

| Function | Why |
|---|---|
| Wideband O2 input (0–5V) | Tuning — see `work/swaps/ecu/sensors-and-inputs/wideband-o2.md` |
| Knock sensor input | Engine protection during tuning |
| A/C idle-up input | Prevents idle dip when A/C engages |
| Fan control output | Electric fan control |
| Data logging (SD card or serial) | Essential for effective tuning |
| USB/serial tuning port | Real-time laptop connection |

## Era-specific requirements

### Era 1 — Renix
- Must support Renix 66-2-2-2 trigger pattern (rusEFI) or Renix 44-2-2 (Speeduino)
- VR input must be sensitive enough for weak Renix CPS signal at cranking RPM — verify threshold spec
- Fuel pump relay control (separate from ignition — unlike Era 2/3 ASD)

### Era 2 — OBD-I SBEC
- Must support Jeep 18-2-2-2 trigger pattern (rusEFI) — confirm Speeduino support
- Single ignition output (distributor coil)

### Era 3 — 1996–1999
- Same as Era 2 trigger-wise
- Single ignition output (distributor coil)

### Era 3 — 2000–2001
- Must support Jeep 18-2-2-2 crank trigger
- **3 ignition outputs minimum** for waste spark coil rail (cylinders 1&6, 2&5, 3&4)
- Cam sensor input from front of engine (different routing)

## Selection process
1. Confirm your era and ignition type
2. Verify trigger pattern support in the ECU's documentation
3. Verify IAC support (stepper motor or plan the PWM IAC strategy — see `work/swaps/ecu/ecu-selection/iac-strategy.md`)
4. Verify ignition output count matches your ignition setup
5. Confirm active community with XJ and MJ experience (shared architecture — same forums apply)
6. See platform files: `work/swaps/ecu/ecu-selection/speeduino.md` and `work/swaps/ecu/ecu-selection/rusEFI.md`
