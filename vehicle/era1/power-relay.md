# Era 1: Power Relay System

## Fuel pump relay
The Renix fuel pump relay supplies 12V to both the fuel pump and the injector feed circuit simultaneously. The injector supply voltage enters the Renix ECU board directly through the fuel pump relay contacts at terminals C11 and D10.

## Shutdown behavior
The ECU monitors crank signal. If no crank signal is detected within ~3 seconds of key-on, the ECU drops the fuel pump relay — cutting power to both the pump and injectors together.

## Ignition path — separate
The ignition path (coil, ICM) is NOT controlled by the fuel pump relay. The ICM has its own power supply from the ignition switch. Losing the fuel pump relay does not cut spark on Era 1.

## Latch relay (B+ relay)
A second relay — the B+ latch relay — exists solely to keep power to the IAC stepper motor at ignition-off, allowing it to reset to a known position. This relay is not related to fuel or ignition control.

## Swap implications
- The open source ECU must control a relay that powers the fuel pump and provides injector supply voltage
- Unlike Era 2/3, cutting this relay does NOT cut spark — ignition must be handled separately
- The B+ latch relay function (IAC reset at key-off) must be replicated if using a stepper IAC
- Plan a dedicated fuel pump relay output on the open source ECU
