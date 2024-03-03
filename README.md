# EC23U

Open source numpad Electrostatic Capacitive PCB.

## Introduction

This project is a continuation of my development of open source EC boards.

The supported layout options are the following:

![Layout option](/Assets/Layout_option.png)

## Technical information

- Layout size: 23U layouts with alternative options
- Compatible switches: EC switches (Topre and NIZ)
- Microcontroller: STM32F401
- Connector: Original OEM JST connector
- Firmware compatibility: QMK (with VIA/VIAL support)
- Protection hardware (present on both the mainboard and both controller versions):
  - Fused
  - ESD protection
- Addressable RGB LED support
- Numlock LED support

## Renders and Prototypes

### Render

![PCB Front Render](/Assets/PCB_render_front.png)

![PCB Back Render](/Assets/PCB_render_back.png)

### Prototypes

![PCB Front](/Assets/PCB_front.png)

![PCB Back](/Assets/PCB_back.png)

**NOTE**: The silkscreen text near the JST connector has the `GND` and `VBUS` label swapped. This is wrong and have been fixed in the latest revision.

## Revisions and relative features

### Rev1.0

This revision implements all the main features of the mainboard ad controllers mentioned in the specifications.

#### RGB header

![RGB header](/Assets/rgb_header.png)

The mainboard features an RGB header for connecting +5V addressable RGB strips. THe properties of the lighting can be controlled through Vial or by assigning RGB control keycodes on the board itself.

#### NumLock Indicator

The mainboard features a NumLock indicator LED. The LED is controlled by the MCU and reacts based on the system state. The LED used is a 3.0mm THT LED. Polarity is signalled by the silkscreen. The indicator is optional.

#### DFU

To access the DFU mode of the mainboard you can perform one of the following actions:

- press the key to which the `QK_BOOT` keycode is assigned (if available)
- while plugging in the board short the `Boot0` pins on the mainboard

![Boot0 pins](/Assets/boot0_pins.png)

## PCB order procedure

### Production files

The production can be found in the [Production folder](/Production).

In there you'll find the main PCB files and the JIS and HHKB plates.

As usual the `*.zip` files are the gerber files, `BOM-*.csv` are the BOM (Bill Of Material) files and `POS-*.csv` are the POS/CPL (Footprint POSition/Component Placement List) files.

### Assembly options

Here follows the options to be used for assembly:

- Assembly Side: Bottom
- Confirm Parts Placement: `yes`

## Copyright notice

This project is not endorse nor sponsored in any way by Topre Corporation and PFU Limited. The HHKB Logo and Topre logo are trademarks of their respective owners.

## License

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.
