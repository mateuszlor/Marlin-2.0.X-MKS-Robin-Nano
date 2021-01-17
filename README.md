# Marlin Firmware adapted for the MKS Robin Nano 1.1/1.2 (Sapphire PRO)

![Marlin logo](buildroot/share/pixmaps/logo/marlin-250.png)

## Marlin 2.0

Marlin 2.0 takes this popular RepRap firmware to the next level by adding support for much faster 32-bit and ARM-based boards while improving support for 8-bit AVR boards.

## Building Marlin 2.0

To build Marlin 2.0 you'll need [PlatformIO](http://docs.platformio.org/en/latest/ide.html#platformio-ide). Detailed build and install instructions are posted at: [Installing Marlin (VSCode)](http://marlinfw.org/docs/basics/install_platformio_vscode.html).

### Supported Platforms

  Platform|MCU| Board
  --------|---|-------
  [MKS Robin Nano](https://makerbase.com.cn/en/)|ARM® Cortex-M3 / STM32F103VET6| MKS Robin Nano 1.1
  [MKS Robin Nano](https://makerbase.com.cn/en/)|ARM® Cortex-M3 / STM32F103VET6| MKS Robin Nano 1.2
  
### Features of the Preset Configuration of Branch MKS Robin Nano

Default configuration in this repo is set to Sapphire PRO with some additional changes mentioned in ##Changes

  Features|Active|Value
  --------|------|-----
  Fast Config Switch Sapphire Pro/Plus/Bluer|True|-
  UI Type|-|Classic Marlin
  TFT Color Selection|True|-
  EEPROM|True|-
  G0 Support|True|-
  G2/G3 Arc Support|True|-
  Classic Jerk|True|15
  Bézier curve acceleration|False|-
  Junction Deviation|False|0.019
  Mesh Bed Leveling|True|-
  Filament sensor|True|-
  TMC UART|-|Ready
  TMC SPI|-|Ready
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
  RAM:   |  44.8% (used 29368 bytes from 65536 bytes)
  Flash: | 44.9% (used 235476 bytes from 524288 bytes)

## UI Preview

![UI preview](docs/UI.png)
  
## Changes

- Sapphire PRO by default
- Enabled case temperature sensor
  - connected to TH2 (PC2)
  - displayed as chamber temperature

## License

Marlin is published under the [GPL license](/LICENSE) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.
