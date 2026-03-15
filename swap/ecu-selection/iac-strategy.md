# ECU Selection: IAC Strategy

## The challenge
All XJ 4.0L engines use a 4-wire stepper motor IAC. Not all open source ECU boards include a stepper motor driver. This must be resolved before first start.

## Option 1: Native stepper support (preferred)
Choose an open source ECU board that includes a 4-wire stepper motor driver. Wire stepper coils A+, A−, B+, B− directly from ECU to IAC valve.

**Pros:** No additional hardware. Stock IAC valve retained.
**Cons:** Not all boards include stepper driver — verify before purchasing.

## Option 2: External stepper driver board
Use an open source ECU without native stepper support, plus an external stepper driver module wired between the ECU and IAC valve.

**Pros:** Allows use of preferred ECU board regardless of stepper support.
**Cons:** Additional component. Requires mounting and wiring the driver board.

## Option 3: PWM IAC valve swap
Replace the stock 4-wire stepper IAC with a 2-wire PWM-controlled IAC valve. Requires:
- A 2-wire IAC valve with compatible throttle body adapter (or custom machined adapter)
- PWM output on the open source ECU (virtually all open source ECUs have this)

**Pros:** Simpler ECU output. More ECU options available.
**Cons:** Physical throttle body modification or adapter required. Some fit challenges.

## Option 4: Manual idle air bypass (trail builds only)
Delete the IAC entirely and install a manual bypass screw in the throttle body. Idle speed set manually.

**Pros:** Zero complexity. Nothing to fail.
**Cons:** Cold start idle quality is poor. Engine may stall until warm. Not appropriate for street use.

## Recommendation
For a street-driven XJ: Option 1 or 2. Confirm stepper support on the chosen ECU board before purchasing — it is the most common oversight in XJ open source ECU planning.
