# Body Electrical

## Overview

This file covers the stock body electrical accessories on the XJ: power windows, door locks, wiper motor, headlight switch, and blower motor. These are the highest-failure-rate body electrical components on high-mileage XJs. All of these systems use electric actuation throughout the production run.

For fault isolation on any of these systems, see [`../../../diagnostics/body-electrical/index.md`](../../../diagnostics/body-electrical/index.md).

---

## Power windows

**All XJs with power windows use cable-type window regulators.** The regulator is a plastic carrier with a steel cable running through a drum driven by the window motor. Scissor-type regulators were not used on any production XJ.

**Motor failure** is the primary failure mode on high-mileage XJs. The motor brushes wear and the motor either slows significantly or stops. Symptoms:
- Window moves slowly or erratically, then stops
- Window stops in a position other than full up or down
- Clicking or grinding from inside the door before failure

The motors are rebuildable (brush kits are available) but replacement motors are common and inexpensive. The regulator cable itself can also break or detach from its anchor points inside the door; inspect the cable and drum when the door panel is off.

**Note:** Power windows are protected by a **circuit breaker** embedded in the under-dash fuse block (not a conventional blade fuse). The breaker will self-reset after cooling, which can make a window that "works sometimes" hard to diagnose as an electrical fault vs. a mechanical one.

---

## Door locks

**All XJ years (1984–2001) use electric door lock actuators.** There are no vacuum-actuated door locks on any XJ. The confusion with vacuum systems on the XJ comes from the front axle disconnect (CAD) vacuum actuator and HVAC mode-door vacuum actuators — these are unrelated to door locks.

**Actuator design by year range:**
| Years | Actuator style |
|-------|---------------|
| 1984–1996 | Electric solenoid/motor (first-generation design) |
| 1997–2001 | Updated electric actuator (different part number, same function) |

**Actuator failure** is the most common door lock fault. The actuator motor wears out, leaving one or more doors that do not lock or unlock from the switches. On four-door XJs, front and rear actuators are the same part within each generation. The tailgate/liftgate has its own actuator.

**Power door locks are protected by a 30-amp circuit breaker** in the under-dash fuse block. Door locks will not actuate from the exterior key cylinder when the circuit is open — only interior switches and remote entry (where equipped) actuate the motors electrically.

---

## Wiper motor

**Failure mode: park position sensor.** The wiper motor contains an internal cam-and-switch mechanism that tells the motor controller where the wiper blade is in its sweep. When the park position sensor fails, the wipers lose their ability to return to the parked position at the bottom of the windshield.

**Symptom:** Wipers stop mid-sweep when the switch is turned off, rather than continuing to the parked position. The wipers continue to operate correctly while the switch is held in any "on" position.

The park sensor is inside the motor assembly and is not individually serviceable on most models — the motor is replaced as a unit. Used motors from the salvage yard are common, but confirm the replacement motor's park sensor is functional before installation.

**Wiper intermittent delay:** The intermittent wiper function runs through a relay and the headlight/wiper switch. Random intermittent failures are often traced to the relay or the switch rather than the motor.

---

## Headlight switch

**Design:** The XJ headlight switch uses a **rheostat-style** dash lighting control — a rotating knob that varies resistance to dim the instrument panel and interior lighting. This is separate from the on/off pull for the headlights.

**Failure mode:** The rheostat contacts inside the switch wear with age and use. Symptoms:
- Instrument/dash lights work only at full brightness but cannot be dimmed
- Instrument/dash lights are intermittent at certain rheostat positions
- Dash lights are completely dead despite good fuses (the rheostat contacts have failed open)

The switch is replaced as a unit — the rheostat is not separately serviceable. Replacement switches from the salvage yard are widely available. Confirm the donor switch's rheostat is functional before installing; this failure mode is common enough that aged salvage switches may have the same problem.

---

## Blower motor

**Failure mode: resistor pack.** The blower motor speed is controlled by a **resistor pack** that drops voltage to the motor for low and medium speed settings. When the resistor pack fails (internally open), the control circuit for all speeds except high is lost. Only high-speed blower operation remains functional.

**Symptom:** Blower motor works on high only. Low, medium-low, and medium-high speeds are dead.

**Resistor pack location:** On the HVAC housing under the passenger side of the instrument panel, inboard of the blower motor itself. On 1997–2001 XJs, it is accessible by removing the passenger kick panel (8mm bolt) or by pulling the glovebox door down. Two 8mm screws secure it to the housing. The connector must be unplugged before the screws are removed.

**Note on Automatic Zone Control (AZC):** XJs optionally equipped with the automatic climate control system (AZC) use a **blower power module** in the same location instead of a simple resistor pack. The AZC module provides variable speed control and fails differently than the resistor pack. If only the highest blower speed works on an AZC-equipped XJ, the module is the starting point for diagnosis.

**Blower motor itself:** Blower motor bearing failure produces noise (grinding, squealing) before the motor stops completely. A motor that runs but vibrates or makes noise should be replaced before it fails in service.

---

## See also

- System overview: [`overview.md`](overview.md)
- Body electrical fault isolation: [`../../../diagnostics/body-electrical/index.md`](../../../diagnostics/body-electrical/index.md)
- Ground faults (common cause of multiple simultaneous accessory failures): [`../../../diagnostics/body-electrical/ground-faults.md`](../../../diagnostics/body-electrical/ground-faults.md)

## Sources
Power window cable-type regulators: JeepForum, CherokeeForum community threads; no scissor-type documentation found in production records. Door lock actuator type (electric all years): jeep-manual.ru FSM 1984–1991 "DOOR LOCKS – POWER" section; Crown Automotive J8134627 fitment data (1984–1996); Quadratec XJ door lock actuator listings. Wiper motor park sensor: JeepForum and NAXJA wiper diagnosis threads. Headlight switch rheostat: JeepForum and CherokeeForum rheostat failure threads. Blower resistor location: JeepForum "blower motor resistor change" thread; CherokeeForum "location of blower motor resistors" thread; NAXJA "$2.00 blower motor resistor fix" thread; ExtremeTerrain HVAC Blower Motor Resistor fitment (1997–2001 XJ).
