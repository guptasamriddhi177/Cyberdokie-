# Platform Research — Raspberry Pi 5 (8GB)

## Main platform
The planned main computer is the Raspberry Pi 5 with 8GB RAM. It is a single-board computer designed to run a full operating system and general-purpose applications.

### Key platform characteristics
- Broadcom BCM2712 application processor
- Quad-core 64-bit Arm Cortex-A76 CPU
- 8GB LPDDR4X memory in the selected configuration
- Dual micro-HDMI display outputs
- USB 3.0 and USB 2.0 ports
- 40-pin GPIO header
- Wi-Fi and Bluetooth connectivity
- microSD storage, with supported PCIe expansion options

Check the official Raspberry Pi product documentation for exact board revisions, supported accessories, power guidance, and interface details before finalizing the design.

## Why this platform?
Compared with a small microcontroller, the Raspberry Pi 5 can run Linux, multitask, host a graphical desktop, and support common programming tools. This makes it suitable as the main computer for a touchscreen cyberdeck.

## Raspberry Pi versus STM32
| Area | Raspberry Pi 5 | STM32 microcontroller |
|---|---|---|
| Main role | General-purpose computer | Embedded controller |
| Typical software | Linux and applications | Firmware |
| Multitasking | Full operating-system processes | Firmware tasks / RTOS |
| User interface | Desktop and GUI applications | Usually controls a separate interface |
| Real-time control | Not its primary strength | Better suited to deterministic peripheral control |
| Cyberdokie role | Main computer | Optional dedicated controller |

An STM32 is optional. It can be added later for dedicated sensor or peripheral control, communicating with the Pi through a suitable interface such as UART or I²C.

## Software direction
Initial recommendation: Raspberry Pi OS (64-bit). It provides a straightforward starting point for hardware support, desktop use, and development. Other operating systems should be selected only after checking compatibility with the intended peripherals and use case.
