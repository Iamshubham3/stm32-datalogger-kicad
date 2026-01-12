# STM32 Datalogger PCB (KiCad)

This project started from an STM32 dev-board baseline and was extended into a datalogger-oriented PCB.
Main additions: external EEPROM (I2C), LSE crystal for RTC accuracy, and backup cell support to keep RTC running when main power is off.

## What I changed (conversion summary)
- Added I2C EEPROM block (address pins, decoupling, write-protect as applicable)
- Added I2C pull-up resistors sized for 3.3V logic
- Added 32.768 MHz crystal (LSE) for stable RTC timekeeping
- Added backup power cell circuitry (VBAT/RTC domain support)
- Updated connectors/test points for logging/debug (UART/I2C as required)
- Verified ERC/DRC and updated net labels + power domains

## Datalogger use-case
- Logs sensor/measurement data via I2C/SPI/UART peripherals
- Stores samples into EEPROM and timestamps using RTC (battery-backed)

## Tools
- KiCad v9 (or your version)
