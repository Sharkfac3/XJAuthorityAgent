# Wiring: Grounds

## Why grounds fail on XJs
XJ grounds are 25–35 years old. The factory ground straps use steel hardware into aluminum and iron surfaces. Corrosion builds resistance invisibly. A ground with 1 ohm of resistance causes a 0.1V error on a 5V sensor — enough to throw codes, cause rough idle, and confuse a tuner into chasing phantom problems.

**Refresh all grounds before the swap. Do not debug a fresh ECU install on corroded grounds.**

## Required ground points for open source ECU install

| Ground | From | To | Wire gauge | Notes |
|---|---|---|---|---|
| ECU power ground | ECU ground pin(s) | Engine block | 12 AWG | Primary ECU ground — use a ring terminal on a clean block bolt |
| Sensor ground | ECU sensor ground pin | Engine block | 16 AWG | Separate from power ground — never share with power ground return |
| Block to chassis | Engine block | Chassis/frame | 8 AWG | Factory location or better — this is the main engine ground strap |
| Head to firewall | Cylinder head | Firewall | 10 AWG | Critical for sensor accuracy — often corroded or missing entirely |
| Battery negative | Battery − | Chassis | Factory or 8 AWG | Inspect and re-terminate if corroded |

## Rules
- All sensor grounds return to the ECU sensor ground pin — never directly to chassis
- ECU power ground and ECU sensor ground must be separate wires to separate block bolts
- Chassis ground loops (sensor → chassis → block → ECU) cause false readings — avoid
- Ring terminals must be crimped and soldered, or use a quality ratcheting crimp — never crimp only on 10 AWG or larger
- Clean the block/chassis surface to bare metal before installing any ground ring terminal
- Apply anti-corrosion compound (OxGard or equivalent) after installing all ground connections

## Common symptom of bad grounds
- O2 sensor reads erratically despite new sensor
- CTS reads colder than actual (resistance in ground path adds apparent resistance)
- TPS voltage drifts or reads incorrect closed-throttle voltage
- Injectors fire intermittently (ground side resistance causes inconsistent pulse width)
- Random CEL codes with no consistent pattern
