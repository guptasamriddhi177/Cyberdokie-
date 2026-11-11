# Power and Thermal Design Notes

## Power planning
The Raspberry Pi 5 and its attached peripherals need a stable power source. The official Raspberry Pi 5 power guidance should be checked for the exact board and accessory combination. A 5V/5A USB-C supply is a commonly recommended choice for a full-featured setup, but the final supply must be selected based on the actual load and official documentation.

Create a power budget before selecting a battery or regulator.

| Load | Voltage | Typical current | Peak current | Evidence |
|---|---:|---:|---:|---|
| Raspberry Pi 5 | Verify | Verify | Verify | Official documentation |
| Touchscreen | Verify | Verify | Verify | Display datasheet |
| NVMe HAT + SSD | Verify | Verify | Verify | Manufacturer datasheets |
| USB peripherals | Verify | Verify | Verify | Device datasheets |
| Audio / accessories | Verify | Verify | Verify | Device datasheets |

Do not add current estimates without a source. Account for startup peaks and simultaneous operation.

## Battery system
Battery operation is a future design item until the display, peripherals, runtime target, and power budget are known. A battery design requires:
- Cells or a certified battery pack with suitable ratings
- Protection against over-current, over-discharge, and over-charge
- Appropriate charging circuitry
- A regulator capable of the required output voltage and current
- Safe connectors, insulation, enclosure, and thermal design

Do not connect a raw battery directly to the Raspberry Pi. Use a properly designed power solution.

## Thermal design
- Use a compatible active cooler or heatsink solution as required by workload and enclosure.
- Provide intake and exhaust paths.
- Avoid blocking the Pi's cooling components.
- Keep the display, battery, and storage within their rated temperature ranges.
- Test temperatures under sustained workload with the enclosure closed.
