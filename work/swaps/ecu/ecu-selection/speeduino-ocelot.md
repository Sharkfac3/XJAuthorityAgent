# ECU Selection: Speeduino — Ocelot Variant

Sources:
- wtmtronics.com/product/ocelot/ — confirmed product listing
- github.com/turboedge/SpeedyBoards/tree/master/OCELOT — hardware repo (KiCad schematics, connector mapping PDF)
- wiki.speeduino.com/en/wiring/Injector_wiring — injector wiring modes and pairing rules
- Project owner field install — Renix VR conditioner + batch fire on XJ 4.0L confirmed working
Load this file alongside `work/swaps/ecu/ecu-selection/speeduino.md` when the installer has chosen or is evaluating the Ocelot board specifically.
For Era 1 Renix full wiring translation (Renix ECU header pins → Ocelot connector pins), see `work/swaps/ecu/wiring/platform-specific/speeduino-ocelot/era1-renix-to-ocelot.md`.

## What it is
The Ocelot is a Speeduino-based engine management board made by WTM Tronics. It is an evolution of the UA4C design with the Arduino controller integrated directly into the PCB, automotive-grade connectors, flyback diodes on all high-current outputs, and a smaller overall footprint. It runs standard Speeduino firmware and is configured via TunerStudio MS.

Price: $160–$187 USD depending on configuration (harness connector housing sold separately).

**NO ARDUINO REQUIRED** — fully integrated solution.

---

## Confirmed I/O summary

### Outputs
| Output type | Count | Detail |
|---|---|---|
| Ignition | 4 channels | Logic 5V, 330mA max pulse |
| Injector | 4 channels | Ground switching |
| High current (flyback protected) | 4 | Idle, Idle2, Boost, VVT |
| Low current | 8 | Fuel pump, Tach, Fan, Fan2, Aux1–4 |
| Stepper idle | Built-in | Dedicated onboard stepper control chip |

### Inputs
| Input | Detail |
|---|---|
| Trigger inputs | 2 (crank + cam) — conditioner module sockets included |
| MAP sensor | 400 kPa onboard |
| Barometric pressure | Yes |
| Throttle position | Yes |
| Coolant temp / Air temp | Yes |
| Oxygen sensor | Yes |
| Flex fuel | Yes (interrupt-capable) |
| Launch input | Yes |
| Knock | Future support |
| VSS | Digital, interrupt-capable |
| Spare analog-capable inputs | 2 |
| Voltage correction | Yes |

### Communications
| Interface | Detail |
|---|---|
| Serial3 | Routed to external connector |
| Bluetooth | Header onboard |
| CAN bus | Optional (requires additional controller) |

---

## Connector pinout — 48-pin connector
Source: Ocelot Connector Mapping PDF (OCELOT/DOC/, github.com/turboedge/SpeedyBoards).
All outputs except ignitors and stepper idle are **ground switching**. Connect at least two ground terminals to a single ground source.

### Injectors
| Pin | Arduino | Function |
|---|---|---|
| 48 | D8 | Injector 1 |
| 47 | D7 | Injector 2 |
| 32 | D6 | Injector 3 |
| 16 | D5 | Injector 4 |

### Ignition
| Pin | Arduino | Function |
|---|---|---|
| 43 | D35 | Ignitor 1 |
| 42 | D36 | Ignitor 2 |
| 27 | D33 | Ignitor 3 |
| 26 | D34 | Ignitor 4 |

### Stepper idle (IAC)
| Pin | Function |
|---|---|
| 1 | Stepper Idle A1 |
| 8 | Stepper Idle A2 |
| 9 | Stepper Idle B1 |
| 41 | Stepper Idle B2 |

### Trigger inputs
| Pin | Arduino | Function |
|---|---|---|
| 38 | D19 | Primary trigger (crank) |
| 22 | — | Primary trigger VR− only |
| 37 | D18 | Secondary trigger (cam) |
| 21 | — | Secondary trigger VR− only |

Note: VR− pins are the negative input of the VR conditioner module. Required for all XJ eras (VR crank sensor). Cam sync (Hall) uses only the D18 pin.

### Sensors
| Pin | Arduino | Function |
|---|---|---|
| 17 | A1 | Exhaust gas sensor (O2) |
| 18 | A3 | Throttle position sensor |
| 19 | A4 | Coolant temperature sensor |
| 33 | A5 | Inlet air temperature sensor |
| 3 | A8 | Spare input 1 |
| 4 | A9 | Spare input 2 |

### High current outputs (flyback protected — idle, boost, VVT)
| Pin | Arduino | Function |
|---|---|---|
| 15 | D9 | PWM Idle 1 |
| 14 | D10 | PWM Idle 2 |
| 13 | D12 | Boost |
| 12 | D11 | VVT |

### Low current outputs
| Pin | Arduino | Function |
|---|---|---|
| 46 | D23 | Fuel pump |
| 45 | D24 | Fan 1 |
| 30 | D25 | Fan 2 |
| 44 | D26 | Low current output 1 |
| 29 | D27 | Low current output 2 |
| 28 | D28 | Low current output 3 |
| 11 | D29 | Low current output 4 |
| 31 | D22 | Tachometer |

### Other inputs
| Pin | Arduino | Function |
|---|---|---|
| 20 | D20 | Flex fuel sensor |
| 34 | D37 | Launch / clutch |
| 35 | D2 | Vehicle speed sensor |
| 36 | D21 | Knock sensor |

### Power and ground
| Pin | Function |
|---|---|
| 5 | 5V out |
| 6 | Keyed 12V input |
| 10 | Unswitched 12V input |
| 7, 23, 24, 39, 40 | Ground |

---

## XJ 4.0L fit assessment

### ⚠️ Known limitation — injector outputs
The Ocelot has **4 injector outputs**. The XJ 4.0L is a 6-cylinder engine requiring 6 injectors.

**True sequential injection is not possible** with 4 outputs on a 6-cylinder. **Semi-sequential is also not valid** — Speeduino firmware limits semi-sequential to 4 cylinders or less.

#### Wiring approach — paired injection (3 channels × 2 injectors)
This is solved entirely at the **wiring level**, not in TunerStudio configuration. Three of the four Ocelot injector outputs are used. Injector 4 (Pin 16, D5) is unused.

| Ocelot output | Pin | Arduino | Injectors wired |
|---|---|---|---|
| Injector 1 | 48 | D8 | Pistons 1 & 6 |
| Injector 2 | 47 | D7 | Pistons 2 & 5 |
| Injector 3 | 32 | D6 | Pistons 3 & 4 |
| Injector 4 | 16 | D5 | — unused — |

Status: `confirmed` — source: project owner field install notes (corroborated by original wiring document).

#### Why this pairing is correct
Speeduino paired injection requires each channel's injectors to have TDCs **360 crank degrees apart**. XJ 4.0L firing order is **1-5-3-6-2-4**:
- Pistons 1 & 6 → 360° apart ✅
- Pistons 2 & 5 → 360° apart ✅
- Pistons 3 & 4 → 360° apart ✅

All three pairs satisfy the rule. This is the mechanically correct grouping for the XJ 4.0L.

#### TunerStudio configuration
TunerStudio does not configure which injectors are physically paired — that is handled entirely by wiring. In TunerStudio:
- Set the **firing order** (XJ 4.0L: 1-5-3-6-2-4)
- Set **Injector Layout** to **Paired** (TunerStudio Engine Constants → Injector Layout)

The ECU then fires its injector outputs in sequence. Because two injectors are physically spliced into each ECU pin, both fire simultaneously on that output. TunerStudio has no visibility into the physical pairing.

Status of TunerStudio settings: `provisional` — confirm exact menu path and field values against project owner's TunerStudio config.

This is a known and accepted tradeoff. Batch injection is functional on the XJ 4.0L for street and trail use.

### Ignition outputs — sufficient for all eras
4 ignition outputs confirmed. XJ requirements:
- Era 1 / Era 2 / Era 3 pre-2000: 1 output (distributor coil) ✓
- Era 3 2000–2001 waste spark: 3 outputs minimum ✓ (Ocelot has 4)

### Injector impedance — all XJ eras
All XJ 4.0L eras use **High-Z (high impedance) injectors** — resistance greater than 8 ohms. No series resistors are required. The Ocelot drives High-Z injectors natively. Status: `confirmed` — source: project owner field knowledge (all eras).

### Stepper IAC — confirmed onboard
The Ocelot includes a dedicated stepper idle control chip. This directly supports the XJ's 4-wire stepper IAC motor on all eras without an external stepper module. See `work/swaps/ecu/ecu-selection/iac-strategy.md` for wiring details.

### Trigger inputs — crank and cam confirmed
2 trigger inputs with conditioner module sockets. The XJ uses:
- VR crank sensor (all eras) — a VR conditioner module in the socket is required; WTM Tronics sells a compatible module at wtmtronics.com (confirmed working with Renix CPS)
- Hall cam sync input (all eras) — confirm logic level compatibility with conditioner module installed

Era 1 Renix note: Renix CPS output is weaker than SBEC/JTEC. The WTM Tronics VR conditioner module (available at wtmtronics.com) has been confirmed to handle the Renix CPS signal at cranking RPM in a field install. The WTM Tronics module uses a **MAX9926 IC** — set TunerStudio trigger edge to `Rising`. Status: `confirmed` — source: project owner field install.

### Form factor
PCB is significantly smaller than the UA4C — "20cm smaller PCB, 41.2cm smaller case." Enclosure planning is easier than UA4C. Automotive-grade connectors replace PC-industry connectors. Harness connector housing sold separately from WTM Tronics.

### Diagnostic LEDs
LEDs on all outputs except stepper idle. Useful for wiring verification and troubleshooting without a laptop connected.

---

## What still needs research
- TunerStudio batch injection menu path — confirm exact field names and values used
- Pinout and connector housing part numbers for XJ harness integration
- Physical enclosure options and mounting locations in XJ firewall/engine bay
- Pinout and connector housing part numbers for XJ harness integration
- Physical enclosure options and mounting locations in XJ firewall/engine bay

---

## Canonical destinations for future findings
- Install reports and field-verified specs → this file (promote from `needs verification` to `confirmed`)
- Era 1 Renix full wiring translation → `work/swaps/ecu/wiring/platform-specific/speeduino-ocelot/era1-renix-to-ocelot.md`
- Connector and pinout details → `work/swaps/ecu/wiring/connectors/`
- Trigger configuration in TunerStudio → `work/swaps/ecu/first-start-and-validation/first-start.md`

⚠️ Open source projects and vendor offerings evolve. Verify current specs against wtmtronics.com and Speeduino firmware documentation before purchasing.
