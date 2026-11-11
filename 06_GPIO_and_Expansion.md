# GPIO and Expansion Notes

The Raspberry Pi 5 provides a 40-pin GPIO header. GPIO operates at 3.3V logic levels.

## Safety and compatibility
- Never apply 5V directly to a GPIO input.
- Confirm each pin's alternate function before assigning it.
- Check whether a peripheral is 3.3V-compatible.
- Use suitable level shifting when required.
- Check current limits and avoid powering high-current loads directly from GPIO.
- Disconnect power before changing wiring.
- Use manufacturer documentation for the board pinout and peripheral connections.

## Possible expansion interfaces
- I²C for supported sensors and modules
- SPI for compatible displays and peripherals
- UART for serial communication with another controller
- USB for general peripherals
- Camera/display connectors for compatible modules

## Optional STM32 expansion
An STM32 board may be used as a dedicated real-time peripheral controller. A UART link is one possible communication method. Confirm voltage levels, UART pin assignments, grounding, and firmware settings on both boards before connection.
