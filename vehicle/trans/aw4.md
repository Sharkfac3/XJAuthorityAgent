# Transmission: AW4 Automatic

## Identity
- Full name: Aisin Warner 4-speed automatic (AW4)
- Years: 1987–2001 in XJ
- Shifts: 4 forward, 1 reverse
- Has torque converter lockup (TCC)

## ECU interaction — critical for swap
The AW4 TCM taps the TPS signal wire directly from the engine harness. It uses TPS voltage to determine:
- Shift aggressiveness (kickdown behavior)
- Torque converter lockup engagement and release timing

### TPS requirements
- Closed throttle: 0.5V
- WOT: 4.5V
- Reference: 5V
- The signal must be continuous — the AW4 TCM reads it in real time

**If TPS output voltage or curve changes after the ECU swap, transmission behavior will change.** Erratic shifts or failed lockup are the symptoms.

## Torque converter lockup (TCC)
The stock ECU commands the TCC solenoid to lock the converter at highway speeds — this eliminates torque converter slip and improves fuel economy.

### Swap options for TCC control
1. **ECU-controlled** — wire TCC solenoid output to a spare digital output on the open source ECU; configure lockup logic in software (preferred)
2. **Standalone lockup controller** — dedicated 3rd-party module controls lockup based on speed/TPS (simple, reliable)
3. **Always locked** — wire solenoid to switched 12V; converter locks at all times (harsh at low speed, not recommended)
4. **Never locked** — leave solenoid disconnected; converter never locks (increased heat, reduced fuel economy, not recommended for highway use)

## Swap notes
- Do not cut or re-route the TPS signal wire going to the AW4 — it must remain intact from TPS to AW4 TCM
- See `swap/wiring/aw4-tps.md` for the full wiring strategy
- The AW4 does not communicate with the engine ECU beyond the TPS tap — no CAN, no serial data
