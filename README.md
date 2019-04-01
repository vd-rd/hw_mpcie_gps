## Hardware Repo for GPS Module 
![board](/assets/board_view1.PNG)
Open Hardware Mini PCI Express GPS module for embedded telemetry or DIY projects.
The module can be used with both passive and active antennas, supports various GPS modules in the widely used uBlox NEO footprint and is easy to assemble at home.
Check the releases section for Gerber files and updated BOM.

### Resources
You can find all necesary information to build or evaluate the module here:
   - [View layout and schematic](https://cadlab.io/project/1666) 
   - [View 3D board render](https://a360.co/2FOFA9d)
   - [Firmware and libraries](https://github.com/vd-rd/fw_mpcie_gps)
   - [Fabrication files](https://github.com/vd-rd/hw_mpcie_gps/releases)

### Module Features
   * compatible with multiple GPS modules (tested with Fibocom GTS-4E and uBLOX NEO-M6)
   * compliant with the half mPCI Express mechanical and electrical specifications (rev 2.1)
   * relatively easy to assemble at home (some experience with SMD soldering required)
   * no special driver required under Linux (exposed as CDC interface)
   * separate .1inch breakout header for UART interfacing
   * compliant with most cheap mPCI to USB solutions

### System architecture
The GPS receiver architecture consists of a receiver for different constellations (GNSS, Beidou, Glonass, GPS) and a microcontroller for interfacing with the mPCIe bus.

The module expects a +3V3 input capable of sustaining at least 100mA peak currents. Typical consumption is ~20mA for active positioning and reporting and <1mA for sleep state.
The STM32F042 microcontroller is used as a USB to UART bidirectional bridge for converting the data from the GPS module to the USB signals required by the mPCI port and for advanced control over the GPS module.

