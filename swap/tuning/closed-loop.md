# Tuning: Closed Loop Operation

## What closed loop means
The ECU reads the narrowband O2 sensor and trims fuel delivery in real time to keep the mixture near stoichiometric (14.7:1 AFR). When the sensor reads rich (>0.7V), the ECU reduces fuel. When it reads lean (<0.3V), the ECU adds fuel. The sensor oscillates — closed loop is working correctly when it cycles smoothly between rich and lean approximately once per second at warm idle.

## Two trim types
**Short-term fuel trim (STFT):** Instantaneous correction applied right now. Should stay within ±10% during normal operation. Large STFT values mean the VE table is significantly off in that region.

**Long-term fuel trim (LTFT):** Running average of STFT over time. Should sit near 0% when the VE table is well-tuned. Persistent positive LTFT means the table is consistently lean. Persistent negative LTFT means it is consistently rich.

## When closed loop is active
Enable closed loop only under these conditions:
- Coolant temperature above ~160°F
- Engine at steady cruise or idle (not accelerating hard)
- Not at WOT

## When to disable closed loop
- WOT — always run open loop at full throttle
- Cold engine (below 160°F)
- Active deceleration fuel cut
- During initial base map development — tune open loop first, enable closed loop after

## Tuning with closed loop enabled
1. Enable closed loop with conservative correction limits (±10%)
2. Datalog steady cruise — watch STFT and LTFT per RPM/load cell
3. Cells with large positive LTFT need more fuel in the VE table — increase VE value
4. Cells with large negative LTFT need less fuel — decrease VE value
5. After adjusting VE table, reset LTFT and datalog again
6. Repeat until LTFT sits near 0% across all cruise conditions
7. Goal: closed loop trims are small corrections, not large compensations

## O2 sensor requirements
Closed loop requires a functioning narrowband O2 sensor that oscillates at warm idle. A lazy or failed sensor will cause the ECU to trim incorrectly. Test the O2 sensor before enabling closed loop — see era-specific O2 sensor file.
