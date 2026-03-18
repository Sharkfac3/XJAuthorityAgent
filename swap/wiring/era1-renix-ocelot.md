# Wiring: Era 1 Renix → Speeduino Ocelot

Source: Project owner install notes and field documentation.
See `swap/ecu-selection/speeduino-ocelot.md` for Ocelot hardware overview and full 48-pin connector pinout.

## Important note on old Speeduino documentation
The project owner's original wiring notes were written for the **Speeduino v0.4** board variant. That board has **different physical connector pin numbers** than the Ocelot. Any v0.4 pin numbers from those old notes do not apply here and are not used in the translation tables below.

The Renix ECU side of the translation is fully confirmed and board-agnostic — the Renix connector headers (A, B, C, D series pins) and wire colors are properties of the stock Renix harness, not of any Speeduino board. Ocelot connector pins in this file are sourced from the Ocelot Connector Mapping PDF (github.com/turboedge/SpeedyBoards/OCELOT/DOC/).

---

## ⚠️ Critical: injector circuit topology change
Renix **powers** the injectors and they are grounded in the engine bay.
Speeduino (and all aftermarket ECUs) **ground** the injectors instead.

**Before wiring injectors:** the engine bay injector grounds must be converted to fused power feeds. This is a circuit topology change, not a pin swap. Failure to do this will damage the ECU.

Status: `confirmed` — source: project owner install notes.

---

## Renix ECU connector reference

The Renix ECU uses a multi-connector pinout with labeled headers (A, B, C, D). The pin labels below refer to the **physical header connectors on the Renix ECU itself**. Wire colors are how you identify each circuit in the stock harness when disconnecting from the Renix ECU. Source: project owner field verification.

### Sensors
| Function | Renix pin | Wire color |
|---|---|---|
| Sensor ground | D3 | — |
| Crank sensor + (VR+) | C1 | Violet-white |
| Crank sensor − (VR−) | D1 | White-black |
| Cam sync signal | C5 | Gray-black |
| Cam sensor ground | C16 | Blue |
| Intake air temp | C8 | Tan-white |
| Coolant temp | C10 | Tan |
| TPS input | C7 | Yellow-green |
| TPS 5V supply | C15 | Light blue |
| O2 sensor | — | — (wideband output to Ocelot) |

### Injectors
| Injector | Renix pin | Wire color | Piston |
|---|---|---|---|
| Injector 1 | B1 | Light blue | 1 |
| Injector 2 | A3 | Light green | 2 |
| Injector 3 | A1 | Tan | 3 |
| Injector 4 | A4 | Yellow | 4 |
| Injector 5 | B2 | White | 5 |
| Injector 6 | A2 | Brown | 6 |

### Ignition and IAC
| Function | Renix pin | Wire color |
|---|---|---|
| Ignition output | D13 | Yellow |
| IAC stepper 2A | B3 | Red-yellow |
| IAC stepper 1A | B4 | Blue-yellow |
| IAC stepper 1B | B5 | Green-black |
| IAC stepper 2B | B6 | Pink-black |

---

## Renix → Ocelot pin translation

### Crank sensor (VR conditioner required)
| Function | Renix pin | Ocelot pin | Notes |
|---|---|---|---|
| VR+ (crank +) | C1 | Pin 38 (D19) | Primary trigger input |
| VR− (crank −) | D1 | Pin 22 (VR− only) | Negative side of VR conditioner module |

WTM Tronics VR conditioner confirmed working with Renix CPS signal at cranking RPM. See `swap/ecu-selection/speeduino-ocelot.md`.

### Cam sensor
**Do not wire the cam sensor on a Renix install.** The Renix decoder does not require cam sync for paired injection + single channel ignition. The secondary trigger input (Pin 37, D18) should be left unwired.

Renix ECU connector pins C5 (sync signal, gray-black) and C16 (cam sensor ground, blue) are present in the stock harness but are not connected to the Ocelot. Leave them unterminated or tucked safely.

Status: `confirmed` — source: project owner field install.

### Sensor ground
| Function | Renix pin | Ocelot pin |
|---|---|---|
| Sensor ground | D3 | Pin 7, 23, 24, 39, or 40 (ground) |

### Injectors — paired wiring (wiring-level solution, not TunerStudio config)
⚠️ See critical topology note above before wiring.

Two Renix injector wires are spliced together and run to a single Ocelot injector pin. The ECU fires that pin; both injectors fire simultaneously. TunerStudio is set to batch injection mode with firing order 1-5-3-6-2-4. The pairing is handled entirely at the wiring level.

| Ocelot injector | Ocelot pin | Arduino | Renix pins | Pistons |
|---|---|---|---|---|
| Injector 1 | Pin 48 | D8 | B1 + A2 | 1 & 6 |
| Injector 2 | Pin 47 | D7 | A3 + B2 | 2 & 5 |
| Injector 3 | Pin 32 | D6 | A1 + A4 | 3 & 4 |
| Injector 4 | Pin 16 | D5 | — | unused |

Pairing logic: each pair has TDC events 360° apart on the XJ 4.0L firing order (1-5-3-6-2-4). Status: `confirmed` — source: project owner install notes.

### Ignition
| Function | Renix pin | Ocelot pin | Notes |
|---|---|---|---|
| Ignition output | D13 | Pin 43 (D35, Ignitor 1) | Era 1 single coil (distributor) |

### IAC stepper motor
The Ocelot has a **built-in stepper driver** — no external DRV8825 module required. (Older Speeduino boards required adding a DRV8825 add-on chip. Ignore that instruction if following older guides.)

| Function | Renix pin | Wire color | Ocelot pin | Notes |
|---|---|---|---|---|
| Stepper 2A | B3 | Red-yellow | Pin 1 (Stepper A1) | `needs verification` — naming convention differs between boards |
| Stepper 1A | B4 | Blue-yellow | Pin 9 (Stepper B1) | `needs verification` |
| Stepper 1B | B5 | Green-black | Pin 8 (Stepper A2) | `needs verification` |
| Stepper 2B | B6 | Pink-black | Pin 41 (Stepper B2) | `needs verification` |

⚠️ Stepper pin translation from old Speeduino labeling (1A/1B/2A/2B) to Ocelot labeling (A1/A2/B1/B2) is provisional. Confirm correct wiring against Ocelot schematic (OCELOT/Ocelot-vA4/STEPPER.kicad_sch on GitHub) or by testing stepper movement direction at first start.

### Temperature sensors
| Function | Renix pin | Wire color | Ocelot pin |
|---|---|---|---|
| Intake air temp | C8 | Tan-white | Pin 33 (A5) |
| Coolant temp | C10 | Tan | Pin 19 (A4) |

### Throttle position sensor
| Function | Renix pin | Wire color | Ocelot pin | Notes |
|---|---|---|---|---|
| TPS signal input | C7 | Yellow-green | Pin 18 (A3) | — |
| TPS 5V supply | C15 | Light blue | Pin 5 (5V out) | — |

After wiring, use TunerStudio TPS calibration wizard to set min/max values.

### O2 / wideband
| Function | Ocelot pin | Notes |
|---|---|---|
| O2 input | Pin 17 (A1) | Connect wideband controller 0–5V output here. See `swap/ecu-selection/wideband.md`. |

### MAP sensor
Built into the Ocelot. Run a vacuum line from the throttle body to the onboard MAP sensor port. No wiring required.

---

## TunerStudio configuration notes (Renix-specific)

All values below are confirmed from project owner TunerStudio config on a running Renix XJ unless otherwise noted.

### Trigger settings
- **Trigger pattern:** Select `Renix` from the dropdown. No tooth count is entered manually — the firmware selects the correct pattern from your cylinder count.
- **Cylinder count:** `6` — firmware internally uses the **66-2-2-2** pattern (66 nominal teeth, 3 groups of 2 missing). The TunerStudio UI shows only "Renix" regardless of variant; you cannot tell from the UI whether 44 or 66 is active.
- **Trigger edge:** `Rising` — confirmed for the WTM Tronics VR conditioner module, which uses a **MAX9926 IC**. Per Speeduino manual: MAX9926 and LM-based conditioners use Rising; DSC-based conditioners use Falling. Verify your conditioner IC before changing this.
- **Skip revolutions:** `1`
- **Trigger angle:** `-60` (crank degrees ATDC for tooth #1)

### Injection settings
- **Injector layout:** `Paired` (Engine Constants → Injector Layout). Colloquially called "batch." 3 channels used; 2 injectors physically spliced per channel at the wiring level. TunerStudio has no visibility into the physical pairing.
- **Injector staging:** `Alternating` (recommended per Speeduino manual)
- **Firing order:** `1-5-3-6-2-4`

### Ignition settings
- **Ignition mode:** `Single channel` — Era 1 Renix uses a single coil through a distributor. Only IGN1 output (Ocelot Pin 43, D35) is used.
- **Cam sync:** Not required. Leave secondary trigger (Pin 37) unwired.

### Sensor calibration
- **TPS:** Use TunerStudio calibration wizard after wiring to set min/max values.
- **Coolant temp / IAT:** `GM` curve used as starting point. Status: `provisional` — confirmed functional but not precision-calibrated against stock Renix sensors. A custom curve may improve cold-start fuel trims.

---

## Useful references from original project notes
- Bosch 124 with Megasquirt: megamanual.com/ms2/Bosch_124.htm
- How to Megasquirt the Jeep Cherokee (Cherokee Forum guide) — large source for original wiring work
- Speeduino wiki: wiki.speeduino.com/en/home
- Speeduino manual PDF: speeduino.com/Speeduino_manual.pdf
- Renix ECU pinout images: cherokeeforum.com (image quality noted as poor — verify against physical harness)
- Live tune reference: tunes.speeduino.com/#/t/w6QbwuXaTo/tune/settings/triggerSettings

---

## What still needs documentation

### Deferred — come back later
- **Power wiring** — Renix ECU power pins to Ocelot Pin 6 (keyed 12V) and Pin 10 (unswitched 12V) not yet mapped
- **Fuel pump wiring** — Ocelot fuel pump output is Pin 46 (D23); Renix harness tap point not yet confirmed
- **Injector flow rate** — stock Renix injector cc/min or lb/hr needed for Required Fuel calculation in TunerStudio
- **Relay rewire** — noted as incomplete in original install; needs a clean pass
- **Injector circuit rewire procedure** — topology change confirmed (convert engine bay grounds to fused power); step-by-step procedure not yet written

### Needs physical verification
- **Stepper motor pin translation** — Ocelot labels (A1/A2/B1/B2) vs old Speeduino labels (1A/1B/2A/2B) not confirmed to be identical. Verify by observing IAC movement direction at first start. If stepper runs backwards, swap one coil pair.

### Confirmed resolved this session
- ✅ Trigger edge: Rising (MAX9926 VR conditioner)
- ✅ Ignition mode: Single channel
- ✅ Skip revolutions: 1
- ✅ Trigger angle: -60
- ✅ Cam sensor: not wired on Renix install, secondary trigger left unwired
- ✅ Injector impedance: High-Z all eras, no resistors needed
- ✅ Injector pairing: 1&6 / 2&5 / 3&4 confirmed correct
- ✅ TunerStudio injection layout: Paired, staging Alternating
- ✅ Temperature sensor curve: GM (provisional)
