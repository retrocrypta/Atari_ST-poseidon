# Atari_ST-poseidon
Atari_ST-poseidon


# Information
Atari ST core based on the MiSTery core that can be found [here](https://github.com/gyurco/MiSTery)

Ported to Calypso by Teiram [here](https://github.com/teiram/calypso-ports/tree/master/mist)

Ported to Poseidon by ron retrocrypta

# Current status
Fully Working


# How to run
You need at least a TOS image. By default it must be named TOS.IMG and placed on the SD card root directory. If you don't want to wait for the TOS to timeout on no diskette inserted on drive A you should also provide a DISK_A.ST file on the root directory of the SD card.


# MiSTery - An Atari ST/STe core for FPGAs

## Features:

- Cycle accurate STe GLUE+MMU combo (re-created from the [original schematics](https://www.chzsoft.de/asic-web/))
- Cycle accurate [FX68K CPU core](https://github.com/ijor/fx68k)
- Cycle accurate Blitter offered by Jorge Cwik
- Mostly cycle accurate shifter based on [schematics made from reverse engineering](http://www.atari-forum.com/viewtopic.php?t=29658)
- MegaSTe 16 MHz CPU mode
- Turbo bus - double RAM access speed
- RAM size up to 14MB
- Support for all TOS versions
- 2 Floppy disc drives
- ACSI hard disc support
- Viking compatible hi-res monochrome card support
- [Real IKBD](https://github.com/harbaum/ikbd) with HD63701 MCU
- Real MIDI input/output using MiST's UART pins
- Serial/parallel port redirect to USB
- Internal Cubase dongle
- Gauntlet type 4 joystick interface support
- STe controller port support
- RP5C15 RTC Chip
- Ethernet interface in cartridge port (Ethernec) support
- [USB-RTC](https://github.com/mist-devel/mist-board/wiki/UsbRtc) support
- Optional scandoubled/YPbPr video output
- Currently it runs on the [MiST board](https://github.com/mist-devel/mist-board/wiki), but the code is modular, so it's possible to add other boards

## Usage for [MiST](https://github.com/mist-devel/mist-board/wiki):

Put the core.rbf and the TOS as tos.img to the SD-Card. TOS/hard disc/floppy images are selectable in the OSD (F12).
With F11, you can toggle between normal and STe joystick ports.

## Current issues/limitations:

- No RAM cache for Mega STe (but the cache control selects turbo bus speed)
- Only fake LMC1992
- PAL clock only (32.084 MHz)
- Since Jagpads have 21 buttons, not all are mapped to MiST controllers when using STe game ports
- No STe paddle handling (but it has 0 software support)

## Thanks to:

- Till Harbaum for the MiST board, original MiST core, new IKBD code
- Jorge Cwik for the FX68K CPU core, FX ST Blitter code and shifter decap
- Christian Zietz for recovering the schematics of the GSTMCU
