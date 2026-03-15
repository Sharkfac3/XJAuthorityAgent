# Era 3: EVAP System

## Overview
The JTEC adds active ECU-controlled EVAP (evaporative emissions) management. This is more sophisticated than the passive Era 1 charcoal canister and is not present on Era 2 at all.

## Components
- Charcoal canister: Stores fuel vapors from the fuel tank
- Purge solenoid: ECU-controlled valve — opens to draw stored vapors into the intake manifold
- Vent valve (1999+): Controls canister venting to atmosphere
- Leak detection pump (1999+): Pressurizes the EVAP system to check for leaks

## ECU interaction
The JTEC commands the purge solenoid open at cruise and light load conditions. If the solenoid is stuck open or the system has a large leak, OBD-II codes are set (P0441, P0455).

## Swap implications
The EVAP system does not need to be retained for engine operation. The open source ECU does not need to control the purge solenoid for the engine to run correctly.

However:
- Removing or disconnecting EVAP will set OBD-II codes
- Vehicles subject to emissions testing may fail inspection without a functional EVAP system
- The purge solenoid can be left connected to a switched 12V source (always closed when de-energized) to prevent codes if inspection is a concern
- If the open source ECU has a spare digital output, the purge solenoid can be controlled — configure as a PWM output at cruise conditions
