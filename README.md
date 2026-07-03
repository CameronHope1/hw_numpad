# hw_numpad
A handwired numpad build with 4 extra buttons at the top of the board to be mapped to suit. Built using a Pro Micro (ATmega32U4) and QMK Firmware.

<img width="1416" height="1346" alt="completed" src="https://github.com/user-attachments/assets/709b25dd-ab9a-4620-b407-40786a0bf460" />

# Overview
This project is a fully custom 4x6 handwired numpad designed and built from scratch. It uses a Pro Micro as the controller and runs QMK firmware for key mapping and configuration. Set up to use with VIA for remapping etc.

My goals for this build were to learn more about:
* Keyboard matrices
* Handwiring and soldering
* QMK firmware
* USB HID devices
* Hardware debugging
* CAD and 3D modeling

# Features
* 4 column x 6 row handwired matrix
* Pro Micro controller
* QMK Firmware
* USB HID support
* VIA support
* Fully custom wiring and layout

# Design and CAD
The case and switch plate were designed in Shapr3D to fit the handwired 4×6 matrix and Pro Micro layout. The models were exported for 3D printing and fabricated on a Bambu Lab A1 Mini using PLA filament.
Multiple smaller prints of various sections were iterated and printed to test tolerances and alignments.

# Wiring and Build Process
After building/handwiring a few existing handwired designs I decided to design and create something of my very own.
The process first began by deciding on a layout of the switches, created using the popular Keyboard-Layout-Editor tool at https://www.keyboard-layout-editor.com/

Then I drew up the wiring schematic in KiCAD, I have found that having a clear schematic drawn can help greatly to avoid mistakes during physical soldering.
<img width="855" height="794" alt="schematic" src="https://github.com/user-attachments/assets/4445a8b1-b2a4-4da5-b856-e78bca29e842" />

Switches are wired in a 4x6 Matrix, with 1N4148 diodes soldered to each switch (used as rows) to prevent ghosting and ensure correct key scanning. Wiring was completed first column-by-column then row-by-row, with the matrix then being connected/soldered to the controller all according to the wiring schematic.

<img width="384" height="512" alt="colsandrows" src="https://github.com/user-attachments/assets/1771881d-841c-4aca-b220-23275b0b493f" />
<img width="384" height="512" alt="wired" src="https://github.com/user-attachments/assets/57e0cef1-32f8-4049-ba41-bc1710a4c118" />


Before final assembly each key was tested on the matrix and firmware was finalized and flashed.

# Firmware
The created firmware for this project is located in the '/qmk_firmware/hw_numpad' directory
Please see the firmware README for build and flashing instructions:
- [Firmware README](./qmk_firmware/hw_numpad/readme.md)

# Lessons Learned
* Iterative prototyping is necessary to validate tolerances and ensure components fit correctly
* Debugging a handwired matrix requires a systematic testing process
* Small mistakes in firmware can cascade into issues such as key failures (e.g. incorrect matrix mapping/ pin definitions)
* Accurate wiring schematic is crucial prior to assembly and greatly reduces time spent troubleshooting further on in the build process.

# Author
Built by Cameron Hope as a personal hardware and firmware learning project.

