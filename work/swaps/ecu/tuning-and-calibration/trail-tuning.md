# Tuning: Trail Tuning

## How trail use differs from street use
A trail XJ operates in conditions that street tuning never encounters:
- Sustained low RPM (500–1,500 RPM) under heavy load while crawling
- Extreme angles (30°+ tilt) that affect fuel delivery and oil pressure
- Heat soak after a hard run with the engine idling or off
- Altitude changes — running at 2,000 ft in the morning, 9,000 ft by afternoon
- Dusty/dirty intake conditions

Each of these affects how the engine management system needs to be set up.

## Low-speed crawl tuning
The low RPM / mid-MAP cells in the VE table are critical for trail use. A lean stumble at 1,200 RPM while inching over a rock ledge is a real hazard.

- Target 14.0–14.5:1 AFR in the 800–1,500 RPM / 40–70 kPa region
- Do not chase fuel economy in these cells — reliability matters more
- Test by driving technical sections and watching wideband AFR in real time

## Idle quality at angle
At extreme angles the throttle body sees inconsistent airflow. A slightly higher base idle (850–900 RPM vs 750 RPM) provides more margin before the engine stalls on a sidehill.

## Hot restart
After a hard run the engine heat-soaks the fuel system. Fuel in the injectors and fuel rail partially vaporizes. The cranking enrichment table must provide enough extra fuel to compensate.

- Increase the hot cranking enrichment (high coolant temp, low cranking pulsewidth) by 10–20% above the base value
- Test by shutting the engine off after a hard run, waiting 10 minutes, and restarting

## Altitude compensation
MAP-based fuel control compensates for altitude automatically — as barometric pressure drops, MAP drops, and the ECU injects proportionally less fuel. No manual adjustment is needed for altitude. This is a significant advantage over carburetor-equipped vehicles.

However: Verify that the ECU's barometric correction (baro correction) feature is enabled and that the MAP sensor is reading barometric pressure correctly at key-on before driving to altitude.

## Fan and cooling
If an electric fan is ECU-controlled, configure a fan idle-up strategy — bump idle target by 50–75 RPM when the fan activates to prevent idle dip.

## Trail reliability checklist
Before any significant trail run:
- [ ] Fuel pressure at spec
- [ ] No active fault codes
- [ ] Wideband reading sensibly at idle
- [ ] Hot restart tested
- [ ] ECU tune file backed up to laptop
- [ ] Spare fuses and relay for ASD/fuel pump circuit carried in the vehicle
