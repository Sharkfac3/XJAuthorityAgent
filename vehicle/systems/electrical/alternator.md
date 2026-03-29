# Alternator

## Overview

The XJ used two distinct alternator families across its production run, separated at the 1991 model year. The voltage regulation architecture is fundamentally different between the two, which has direct implications for diagnosis: a charging problem on a post-1990 XJ can originate in the PCM, not the alternator.

---

## Era 1 (1987–1990): Delco CS-130, integral regulator

**Alternator:** Delco CS-130 (internally regulated). The voltage regulator is built into the alternator housing — there is no separate external regulator box.

**Output by trim level:**
| Trim / equipment level | Output |
|------------------------|--------|
| Base / standard | 61A |
| Laredo, tow package, base w/ heavy-duty option | 80A |
| Limited / full-option | 100A |

**Regulation:** The Delco CS-130 regulates its own output voltage internally. The ECU/ICM is not involved in alternator control. A charging fault on a Renix XJ is almost always the alternator or a wiring issue — not an ECU problem.

**Note on `vehicle/era2/ho-engine.md`:** That file states "Renix: Separate external voltage regulator." This is incorrect. The Delco CS-130 has an **integral** regulator — there is no stand-alone external regulator box on any Renix XJ. The correct information is documented here.

---

## Era 2 and Era 3 (1991–2001): Nippondenso, PCM-regulated

**Alternator:** Nippondenso. The alternator does not self-regulate — voltage regulation is handled externally by the **PCM**, which controls the alternator's field circuit.

**Output by year range:**
| Years | Typical output |
|-------|---------------|
| 1991–1998 | ~70–90A |
| 1999–2001 | 90–117A (year and trim dependent) |

Output varied with options package. A/C, power accessories, and trailer tow packages pushed alternator ratings higher. The PCM modulates field current to match electrical demand.

---

## Failure symptoms

These symptoms apply to all years:

| Symptom | Likely cause |
|---------|-------------|
| Battery warning lamp illuminated | Charging system fault — test voltage immediately |
| Voltage at battery below 13.8V at idle | Undercharging — alternator output insufficient |
| Voltage at battery above 14.8V at idle | Overcharging — regulator fault |
| Battery repeatedly going dead despite driving | Undercharging or excessive parasitic draw |
| Whining or grinding from alternator | Bearing failure; replace before it leaves you stranded |
| Burning smell from alternator | Winding or diode failure; replace |

---

## Testing

**Voltage test — battery terminals, engine running at idle:**
- 13.8–14.5V: Normal
- Below 13.8V: Undercharging — proceed to alternator output and PCM field signal tests
- Above 14.8V: Overcharging — regulator fault (PCM on Era 2+, internal regulator on Era 1)

If voltage reads low at the battery but higher when measured directly at the alternator output stud, the fault is in the charging wiring or grounds, not the alternator output.

**Ground check before condemning the alternator:**
Charging voltage measured at the battery depends on the quality of the return path. A corroded engine-to-chassis ground will cause low charging voltage at the battery even when the alternator is producing correct output. Always verify grounds before replacing an alternator. See [`../../../diagnostics/body-electrical/ground-faults.md`](../../../diagnostics/body-electrical/ground-faults.md).

---

## PCM failure masquerading as alternator failure (Era 2 and Era 3)

On 1991–2001 XJs, the PCM controls the alternator's field circuit. A failed PCM — or a broken wire in the PCM-to-alternator field circuit — can cause the alternator to stop charging, producing symptoms identical to a dead alternator:

- Battery warning lamp on
- Voltage at battery drops to near battery voltage (12–12.6V) at idle
- Battery drains during driving

Before replacing a Nippondenso alternator on a 1991–2001 XJ, confirm the field signal from the PCM is present at the alternator. If the PCM is not commanding the alternator to charge, the alternator itself may be fine. This is an uncommon failure but has been documented on vehicles with aging SBEC and JTEC ECUs.

---

## See also

- Electrical system overview: [`overview.md`](overview.md)
- Charging and starting baseline (battery, cables, starter): [`../charging-starting/overview.md`](../charging-starting/overview.md)
- Charging diagnostics (low voltage, no charge): [`../../../diagnostics/charging-and-starting/low-charging-voltage.md`](../../../diagnostics/charging-and-starting/low-charging-voltage.md)
- Era 1 wiring context: [`../../era1/wiring.md`](../../era1/wiring.md)
- Era 2 wiring context: [`../../era2/wiring.md`](../../era2/wiring.md)

## Sources
Alternator type and output: NAXJA "Alternator Loads and Sizing" thread; JeepForum "stock alternator amp output" thread; CherokeeTalk "renix alternators" thread; JeepForum "REnix Alternator 1989" thread. Voltage regulator location: NAXJA "Voltage Regulator – Integral or External?" thread; jeep-manual.ru FSM 1984–1991 "ALTERNATOR – DELCO W/INTEGRAL REGULATOR" section. PCM regulation on HO era: CherokeeTalk alternator threads; JeepForum alternator discussions.
