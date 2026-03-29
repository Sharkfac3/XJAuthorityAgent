# Driveshaft Fabrication and Installation

Measurement, ordering, and installation procedures for front and rear driveshafts on an XJ Cherokee one-ton axle build (Dana 60 front / Sterling 10.50 rear).

For U-joint series, shaft specs, and SYE details, see: [`../../../../sourcing/interchange/axles/one-ton-driveshaft-specs.md`](../../../../sourcing/interchange/axles/one-ton-driveshaft-specs.md)

---

## When to measure

Driveshafts are measured **after** the axles are fully installed under the XJ at ride height:
- Housing narrowing is complete
- Spring perches are welded
- Axles are bolted to leaf springs
- Vehicle is at ride height (on the tires or on jack stands simulating ride height)
- SYE is installed on the transfer case (if applicable)

Do not measure before the axles are in — any change to lift height, spring perch position, or housing width will change the shaft length.

## Rear driveshaft

### Measurement procedure
1. Vehicle at ride height
2. Measure from the center of the transfer case rear output flange (or SYE output flange) to the center of the Sterling pinion flange
3. This is the center-to-center distance — the driveshaft shop uses this to build the shaft
4. Note the transfer case output yoke type and size (1310 stock, or SYE flange)
5. Note the Sterling pinion flange bolt pattern and count

### Configuration
- **SYE + double-cardan (CV) joint at the transfer case end** — mandatory for 6"+ lift. The CV joint handles the steep operating angle.
- **Single U-joint at the pinion end** — standard, because the pinion angle is set to minimize the operating angle at this end.
- **U-joint series:** 1350 minimum at both ends. If the Sterling pinion uses a 1410 flange, run 1350x1410 combination or full 1410.

### SYE (Slip Yoke Eliminator)
- Install on the NP231 transfer case rear output before driveshaft measurement
- Replaces the stock slip yoke with a fixed flange
- The slip joint moves to the driveshaft body (built into the shaft by the driveshaft shop)
- Without an SYE, the stock slip yoke operates at extreme extension at 6"+ lift, causing vibration and premature wear

## Front driveshaft

### Measurement procedure
1. Vehicle at ride height
2. Measure from the center of the transfer case front output yoke to the center of the Dana 60 front pinion yoke
3. Note the transfer case output yoke size (1310 stock)
4. Note the Dana 60 pinion yoke size (typically 1350)

### Configuration
- **Double-cardan (CV) joint at the transfer case end** — required for the steep front driveshaft angle at 6"+ lift
- **Single U-joint at the pinion end** — standard
- The front shaft is shorter than the rear and operates at a steeper angle
- **U-joint series:** 1350 at the axle end. Transfer case end is limited by the output yoke (1310 unless upgraded).

## Pinion angle verification

After driveshafts are installed, verify pinion angles with a digital inclinometer:

### Rear
1. Place the inclinometer on the Sterling pinion flange face — record the angle
2. Place the inclinometer on the transfer case rear output flange face — record the angle
3. The difference is the operating angle
4. **Target: 2–4 degrees** total operating angle

### Front
1. Same procedure on the Dana 60 front pinion yoke and transfer case front output yoke
2. **Target: 2–4 degrees** total operating angle
3. Front angles are typically steeper than rear due to the shorter shaft — the CV joint compensates

### Correction
- If the operating angle is too steep: adjust the spring perch position to rotate the pinion upward (for the rear) or use an axle shim (wedge) between the spring and perch
- If the operating angle is too shallow (near zero): the U-joints will not self-lubricate and will wear prematurely. Increase the angle slightly by adjusting the perch.

## Ordering from a driveshaft shop

Provide the shop with:
1. Center-to-center measurement (both shafts)
2. Transfer case output type and flange/yoke size
3. Pinion end type (yoke or flange) and size for both axles
4. Desired U-joint series
5. Whether you need a CV joint at the transfer case end (yes, for both shafts)
6. Whether you need a slip joint built into the shaft (yes, for the rear if using SYE)

### Recommended shops (mail-order)
- Tom Woods Custom Driveshafts
- Adams Driveshaft
- JE Reel Driveshaft

Local driveshaft shops can also build custom shafts — bring your measurements and the old shafts for reference.

## Post-install vibration diagnosis

If vibration occurs after driveshaft installation:
1. **Verify pinion angles** — most vibration is from incorrect pinion angle
2. **Check U-joint phasing** — the U-joints at each end of the shaft must be in phase (yoke ears aligned)
3. **Check shaft balance** — a new shaft should be balanced by the shop. If you feel vibration at speed but not at low RPM, the shaft may be out of balance.
4. **Check for binding** — cycle the suspension through full travel and verify the shaft does not bind or bottom out at any point

---

## Related
- Driveshaft specs and U-joint series: [`../../../../sourcing/interchange/axles/one-ton-driveshaft-specs.md`](../../../../sourcing/interchange/axles/one-ton-driveshaft-specs.md)
- Front spring perch (affects pinion angle): [`../one-ton-front/spring-perch-relocation.md`](../one-ton-front/spring-perch-relocation.md)
- Rear spring perch (affects pinion angle): [`../one-ton-rear/spring-perch-welding.md`](../one-ton-rear/spring-perch-welding.md)
