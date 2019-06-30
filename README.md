# Luma3DS
*Noob-proof (N)3DS "Custom Firmware"*

## What is this fork

Many of you probably know the NTR CFW that enabled streaming the 3DS' screen to the computer over the debugger.  
This fork implements this functionality into rosalina.  
It's still higly WIP and not intended for public use since framerates are quite slow.  
But it's more stable than the NTR firmware. You can switch games and the games I tested worked flawlessly.  
Some of the code is inspired by NTR but most of it is a complete reimplementation, because I wanted to figure out where the annoying bugs with the NTR firmware are. (e.g. 3DS hanging when switching processes)

## Usage of the streaming capability

1. Go to the rosalina menu->streaming->start strea
2. Type the IP of your 3DS into the python script
3. Install the dependencies with `pip3 install pygame pillow numpy`
4. Start the script with `python3 streaming.py 4`

(Click the image for a video demo)
[![Click for video demo](preview.png)](https://youtu.be/SAhSV_xUGCc)

---

## What it is

**Luma3DS** is a program to patch the system software of (New) Nintendo 3DS handheld consoles "on the fly", adding features (such as per-game language settings and debugging capabilities for developers) and removing restrictions enforced by Nintendo (such as the region lock).
It also allows you to run unauthorized ("homebrew") content by removing signature checks.
To use it, you will need a console capable of running homebrew software on the ARM9 processor. We recommend [Plailect's guide](https://3ds.hacks.guide/) for details on how to get your system ready.

Since Luma3DS v8.0, Luma3DS has its own in-game menu, triggerable by `L+Down+Select` (see the [release notes](https://github.com/AuroraWright/Luma3DS/releases/tag/v8.0)).

---

## Compiling

First you need to clone the repository with: `git clone https://github.com/AuroraWright/Luma3DS.git`  
To compile, you'll need a recent commit of [makerom](https://github.com/profi200/Project_CTR) added to your PATH. You'll also need to install [firmtool](https://github.com/TuxSH/firmtool), its README contains installation instructions.
You'll also need to update your libctru and devkitARM installation to their latest releases.
Then, run `make`.
The produced file is called `boot.firm` and is meant to be copied to the root of your SD card, for usage with boot9strap.

---

## Setup / Usage / Features

See https://github.com/AuroraWright/Luma3DS/wiki

---

## Credits

See https://github.com/AuroraWright/Luma3DS/wiki/Credits

---

## Licensing

This software is licensed under the terms of the GPLv3.
You can find a copy of the license in the LICENSE.txt file.

Files in the GDB stub are instead double-licensed as MIT or "GPLv2 or any later version", in which case it is specified in the file header.
