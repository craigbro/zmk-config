My ZMK firmware configuration for corne wirelss keyboards.

I am running two nice nano based wirelsss cornes (6 col) with a QWERTY
layout, and 4 layers.

To create the keymaps, I used
https://nickcoutsos.github.io/keymap-editor/ as a keymap editor, in
Chrome, which let me use local files.  The 'config/corne.keymap' file
contains the keymap.

I have an experimental miryoku based kaymap defined as well, but it's
build is commented out in the 'build.yaml' file.

## Bluetooth pairing

Layer 3 has BT Profile Selectors on the far left row, starting with 0
at the top, and 2 at the bottom.

## Building Firmware

There is a github workflow, which is triggered on puished to main,
which will build the firmware artifacts.  Under the 'Actions' tab you
can see theworkflows, and download the 'firmware.zip' artifact.

## Installing Firmware

### OSX

Connect the left corne to a usb cable, and hit the reset button twice.
It will show up as a drive in the Finder.  You can then drag and drop
the appropriate *.uf2 file from the firmware.zip artifact.

An error about not completing the copy may be shown, but this is due
to the chip switching back to normal mode from target mode, and the
Finder being confused. 

Repeat the process for the other half of the keyboard.
