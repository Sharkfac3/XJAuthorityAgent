# Fuse Blocks and Power Distribution Center

## Overview

The XJ uses two generations of fuse/relay distribution hardware depending on model year. The split is at 1993 — not at the Era 2/Era 3 boundary. Understanding which hardware is present matters when chasing electrical faults and when identifying which circuits are affected by a failed fuse or relay.

**Note:** The existing `vehicle/era2/wiring.md` states that 1991–1995 XJs have no under-hood PDC. FSM documentation (jeep-manual.ru, ManualsLib 1993 Cherokee Maintenance Manual p.26) shows the PDC was introduced mid-Era 2 in 1993. The 1991–1992 vehicles have no PDC; 1993–1995 vehicles do.

---

## 1984–1992: Under-dash fuse block only

**Location:** Driver-side kick panel, under the left side of the instrument panel.

**Coverage:** All fuses and most relays for this generation are in this single block. Protected circuits include:
- Interior lighting (dome, courtesy)
- Exterior lighting (headlights, parking, tail)
- Accessory circuits (radio, windows, locks, wipers)
- HVAC blower
- Ignition-fed circuits
- Circuit breakers for power windows and door locks (embedded in the fuse block)

**High-current paths in the engine compartment (1984–1992):**
Rather than a centralized PDC, high-current circuits are distributed through **fusible links** connected via ring terminals to a stud on or near the **starter relay**, typically located on the firewall or inner fender near the battery. On Renix-era vehicles (1988–1990), up to five fusible links (four green, one blue) share this stud. These protect the battery feed, alternator output, and major circuit feeds. There is no black plastic enclosure — the links and relays are individual components mounted at scattered points in the engine compartment.

---

## 1993–2001: Under-dash fuse block + under-hood PDC

### Under-dash fuse block

**Location:** Driver-side kick panel, same physical location as the pre-1993 block. On 1997–2001 XJs, the under-dash block is referred to as the **junction box** in factory service manuals; the layout changed slightly between 1996 and 1997.

**Coverage:** Body, accessory, and cabin circuits:
- Interior and exterior lighting
- Power windows, door locks
- Wiper motor
- Blower motor
- Radio, clock memory
- Ignition-switched accessory feeds

### Under-hood PDC

**Location:** Right front fender apron (passenger side), mounted on the inner fender with two screws. Black plastic enclosure with a snap or screw-on cover. On 1996 and later vehicles, the cover has a fuse/relay identification label on its underside.

**Coverage:** High-current and engine-management circuits:
- Starter relay
- Automatic Shutdown (ASD) relay — supplies coil, injectors, and fuel pump together
- Fuel pump relay / fuel pump fuse
- Engine controller (PCM) feed
- Generator/alternator field feed
- A/C compressor relay
- Auxiliary cooling fan relay (where equipped)
- Heated rear window relay (where equipped)
- High-current maxi fuses for battery feed and major circuit protection

**PDC fuse/relay layout varies by year.** The 1993–1995, 1996, and 1997–2001 layouts are each different. The label inside the PDC cover is the fastest reference. For a vehicle with a missing or damaged cover, the FSM for that specific year is required — positions are not interchangeable between years.

---

## Fuse block connector corrosion — diagnostic note

The under-dash fuse block on all XJ years receives its main power through a multi-pin plastic connector on the back of the block. On high-mileage and older XJs, this connector corrodes at the terminals, causing:

- Individual circuits that are intermittent or dead despite good fuses
- Fuses that read correct voltage on one side but nothing on the load side
- Multiple unrelated circuits failing at the same time

**When diagnosing any electrical problem on a high-mileage XJ, inspect the back of the fuse block.** Pull the connector, clean the terminals, and apply dielectric grease before condemning individual components downstream.

The PDC connector (on 1993+ vehicles) is exposed to the elements and develops its own corrosion. Inspect the PDC connector as part of any charging, fuel pump, or ASD relay diagnosis.

---

## See also

- System overview: [`overview.md`](overview.md)
- Era 1 wiring (1988–1990): [`../../era1/wiring.md`](../../era1/wiring.md)
- Era 2 wiring (1991–1995): [`../../era2/wiring.md`](../../era2/wiring.md)
- Era 3 wiring (1996–2001): [`../../era3/wiring.md`](../../era3/wiring.md)
- Body electrical fault isolation: [`../../../diagnostics/body-electrical/index.md`](../../../diagnostics/body-electrical/index.md)

## Sources
PDC introduction year: ManualsLib Jeep Cherokee 1993 Maintenance Manual p.26 ("Power Distribution Center Identification 1993–96"); jeep-manual.ru FSM 1993 section (FUSES & CIRCUIT BREAKERS). Pre-PDC fusible link layout: NAXJA community thread on XJ fuse information. 1984–1991 fuse block location: jeep-manual.ru FSM 1984–1991 (ELECTRICAL COMPONENT LOCATOR, p.92). Connector corrosion: JeepForum, CherokeeForum, NAXJA threads on electrical gremlins.
