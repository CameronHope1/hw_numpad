# Firmware

Firmware for the HW Numpad, a custom handwired mechanical numpad that has 4 extra remappable keys built using QMK Firmware.

* Keyboard Maintainer: [Cameron Hope](https://github.com/CameronHope1)
* Hardware Supported: Pro Micro (ATmega32U4)
* Matrix: 4x6 (4 columns x 6 rows)
After setting up your QMK build environment, compile firmware with:

    make handwired/hw_numpad:default

Flashing example for this keyboard:

    make handwired/hw_numpad:default:flash
    
Alternatively, use QMK Toolbox if you prefer a GUI tool.

## Bootloader
Enter the bootloader by briefly shorting the RST and GND pins on the controller while keyboard is connected via USB.
