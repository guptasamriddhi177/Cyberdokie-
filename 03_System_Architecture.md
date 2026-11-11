# System Architecture

## High-level architecture

```text
                 +-----------------------------+
                 |      Touchscreen Display    |
                 |   video + touch interface   |
                 +--------------+--------------+
                                |
                                |
+----------------+     +--------v---------+      +----------------+
| Keyboard /     | USB |                  | GPIO | Optional       |
| Pointing input +---->+ Raspberry Pi 5   +----->+ Sensors /      |
|                |     | 8GB RAM           |      | STM32 board    |
+----------------+     | Main computer    |      +----------------+
                       +---+----------+---+
                           |          |
                     +-----v--+   +---v-----------+
                     | Storage|   | Wireless      |
                     | microSD|   | Wi-Fi/Bluetooth|
                     | / NVMe*|   +---------------+
                     +--------+
```

`*` NVMe requires a compatible PCIe expansion solution and suitable physical installation.

## Functional blocks
1. **Compute:** Raspberry Pi 5 runs the operating system and applications.
2. **Display:** A compatible display receives video through its supported interface.
3. **Touch:** Touch events are transferred through the display's supported USB, I²C, or other interface.
4. **Input:** Keyboard and optional mouse/trackpad connect through USB or Bluetooth.
5. **Storage:** microSD is the simplest initial boot-storage option. NVMe is an optional expansion.
6. **Power:** A suitable regulated supply powers the Pi and peripherals according to their individual requirements.
7. **Expansion:** GPIO and external interfaces support optional modules.

## Design principle
Keep the Raspberry Pi 5 board intact. A custom PCB, if developed, should be an expansion, connector, or power-management board designed against verified specifications—not an assumed replacement for the Pi motherboard.
