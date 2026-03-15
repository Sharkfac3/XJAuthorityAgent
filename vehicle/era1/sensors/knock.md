# Era 1: Knock Sensor

## Specs
- Present on: 1987–1990 Renix 4.0L
- Type: Piezoelectric resonant type
- Location: Driver's side of engine block
- Output: AC voltage signal when knock frequency detected
- Signal: Sent to the Renix ignition module (ICM), not the fuel ECU

## Function
The knock sensor allows the ignition module to retard timing when knock is detected, protecting the engine during low-octane fuel use or high load conditions.

## Swap notes
- The stock knock sensor signal goes to the ICM, which is being removed in the swap
- Open source ECUs with knock input support can use the stock sensor — wire knock signal to the ECU knock input and configure the retard strategy in software
- If the open source ECU does not support knock input, the sensor can be left disconnected — the engine runs safely on conservative timing, but loses knock protection
- Knock sensing is recommended for any build that will run varied fuel quality or push timing aggressively
