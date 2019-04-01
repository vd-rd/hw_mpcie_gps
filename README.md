## Hardware Repo for GPS Module 

Open Hardware Mini PCI Express GPS module for embedded telemetry or DIY projects.
The module can be used with both passive and active antennas, supports various GPS modules in the widely used uBlox MAX footprint and is easy to assemble at home.
The firmware is available in a separate [repository](https://github.com/vd-rd/fw_mpcie_gps).
Check the releases section for Gerber files and updated BOM.

### Module Features
    * compatible with multiple GPS modules
    * compliant with the half mPCI Express mechanical specifications
    * relatively easy to assemble at home
    * no special driver required under Linux
    * separate .1inch breakout header for UART interfacing
    * compliant with most cheap mPCI to USB solutions

### Hardware overview

The module expects a +3V3 input capable of sustaining at least 100mA peak currents. Typical consumption is ~20mA for active positioning and reporting and <1mA for sleep state.
The STM32F042 microcontroller is used as a USB to UART bidirectional bridge for converting the data from the GPS module to the USB signals required by the mPCI port and for advanced control over the GPS module.

