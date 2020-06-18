# Marlin Firmware adapted for the MKS Robin Nano 1.1/1.2


## Marlin 2.0<img align="right" width=175 src="buildroot/share/pixmaps/logo/marlin-250.png" />


Marlin 2.0 takes this popular RepRap firmware to the next level by adding support for much faster 32-bit and ARM-based boards while improving support for 8-bit AVR boards. Read about Marlin's decision to use a "Hardware Abstraction Layer" below.

Download earlier versions of Robin Nano Firmware on the [Releases page](https://github.com/le3tspeak/Marlin-2.0.X-Sapphire-PRO/releases).

## Building Marlin 2.0

To build Marlin 2.0 you'll need [PlatformIO](http://docs.platformio.org/en/latest/ide.html#platformio-ide). Detailed build and install instructions are posted at:

 
  - [Installing Marlin (VSCode)](http://marlinfw.org/docs/basics/install_platformio_vscode.html).

### Supported Platforms

  Platform|MCU| Board
  --------|---|-------
  [MKS Robin Nano](https://makerbase.com.cn/en/)|ARM® Cortex-M3 / STM32F103VET6| MKS Robin Nano 1.1 
  [MKS Robin Nano](https://makerbase.com.cn/en/)|ARM® Cortex-M3 / STM32F103VET6| MKS Robin Nano 1.2
  
### Features of the Preset Configuration of Branch MKS Robin Nano

  Features|Active|Value
  --------|------|-----
  Fast Config Switch Sapphire Pro/Plus/Bluer|True|-
  UI Type|-|Classic Marlin
  TFT Color Selection|True|-
  EEPROM|True|SDCARD EEPROM EMULATION
  G0 Support|True|-
  G2/G3 Arc Support|True|-
  Classic Jerk|True|15
  Bézier curve acceleration|False|-
  Junction Deviation|False|0.019
  Mesh Bed Leveling|True|-
  Filament sensor|True|-
  TMC UART|-|Ready
  TMC SPI|-|in progress
  TMC 2209 HW Serial|-|Ready
  Neopixel|-|Ready
  Cancel Objects|True|-


  Axes|Sapphire Pro|Sapphire Plus|Bluer
  ----|----|----|----
  X|TMC2208 Standalone|TMC2208 Standalone|TMC2208 Standalone
  Y|TMC2208 Standalone|TMC2208 Standalone|TMC2208 Standalone
  Z|A4988|A4988|A4988
  E|A4988|TMC2208 Standalone|A4988

  Memory consumption|Value
  --------------------|-------------------------------------------
  RAM:    |47.8% (used 36944 bytes from 65536 bytes)
  Flash:  |43.2% (used 223380 bytes from 524288 bytes)

## UI Preview
<img align="center" width=650 src="/docs/UI.png" />
  
## Submitting Changes

- Please submit your questions and concerns to the [Issue Queue](https://github.com/le3tspeak/Marlin-2.0.X-MKS-Robin-Nano/issues).


## Changelog

Version|Changes & Fixes
-------|-------
1.0.5b
  -|TMC SW Serial extension E1 & Z2
  -|Add Adv. Preset Custom PID
  -|Add JD_HANDLE_SMALL_SEGMENTS option
  -|Russian language fix
1.0.5a
  -|Add Adv. Preset Custom Axis Steps Per MM
  -|Extension of BLTouch Preset
  -|Add Adv. Preset Custom Stepper Motor Drivers
  -|Add Status Logo TT
  -|Add Adv. Preset Optical Endstops XY
1.0.5| Major Update & Reworking
  -| Add Adv. Preset Linear Pressure Control
  -| Add Adv. Preset Motion Modes
  -| Add Adv. Preset BLTouch
  -| Move SD Settings to Pins
  -| Minor TFT Fixes
1.0.4|Touch support for Marlin Menus
  -|errors moved in Sanity Check
  -|new TFT scale up
  -|improve G2/3 movement buffer
  -|STM32F1: Fix SDIO read errors
  -|Improve SD Card Read Speed
  -|Add Cura/Prusa Start/End Codes
  -|Add Cura/Prusa Profiles
1.0.3|Add Bluer Fast Config Switch Preset 
  -|Error messages separated
1.0.2|Add TMC HW Serial
  -|Add documentation TMC HW Serial
  -|Add TFT Color Selection
  -|Fix SD Read Errors
1.0.1a|Initial commit
  

## License

Marlin is published under the [GPL license](/LICENSE) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.
