# ECU Selection: Wideband O2 Sensor

## Why it's needed
The stock narrowband O2 sensor can only indicate rich or lean — not by how much. Effective VE table and WOT tuning requires knowing the actual AFR. A wideband O2 sensor measures across the full range (typically 10:1–20:1 AFR) and outputs a proportional voltage.

## Recommended sensor
Bosch LSU 4.9 — the current industry standard for aftermarket wideband use. Used by virtually all wideband controllers.

## Wideband controller options
A controller is required to read the LSU 4.9 and output a usable analog voltage:
- AEM X-Series wideband
- Innovate MTX-L Plus
- PLX Devices SM-AFR
- DIY options (14point7 Spartan, etc.)

All output a 0–5V analog signal proportional to AFR. Connect to a spare analog input on the open source ECU for real-time logging during tuning.

## Installation
- Weld a bung into the exhaust before the catalytic converter
- Mount controller within the cabin or in a protected location
- Connect wideband analog output (0–5V) to open source ECU spare analog input
- Configure the ECU analog input to display AFR using the controller's output curve

## Usage
- Use wideband for VE table tuning and WOT pulls
- Retain the stock narrowband for closed-loop idle and cruise correction — narrowband switches faster than wideband and is better suited for closed-loop control
- Do not use wideband for closed-loop control unless the ECU specifically supports wideband closed-loop with the LSU 4.9 protocol
