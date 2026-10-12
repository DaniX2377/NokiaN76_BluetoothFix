# Nokia N76 Bluetooth Volume Fix

A patch for the Nokia N76 that fixes Bluetooth headset volume control via AVRCP.

If the volume indicator changes when you press the phone's volume keys, but the actual Bluetooth headset volume does not change correctly, this patch may help.
> The files included in this patch are modified versions of the original Bluetooth system files from the Nokia N95 8GB firmware.

## Compatibility

- **Device:** Nokia N76 (RM-135)
- **Tested firmware:** v31.0.014
- **Protocol:** Bluetooth AVRCP

Other devices and firmware versions have not been tested.

## Requirements

- An unlocked Nokia N76 with full filesystem access.
- RomPatcher+ with the `Open4All` patch enabled.

## Installation

1. Download the files from this repository:
   - `btrcc.dll`
   - `btrcc.rsc`
   - `btaccserver.exe`
2. Transfer the files to your phone.(If you send them via Bluetooth, open X-plore and go to Tools → Messaging to access the received files.)
3. Copy the files to the following locations:

   | File | Destination |
   |---|---|
   | `btrcc.dll` | `C:\sys\bin\` |
   | `btaccserver.exe` | `C:\sys\bin\` |
   | `btrcc.rsc` | `C:\resource\plugins\` |

> 3.1. If the `C:\resource\plugins\` directory does not exist, create it.

4. Reboot your phone.

5. Connect your Bluetooth headset, play music using the built-in music player, and adjust the volume with the phone's volume keys.

Enjoy!

## Uninstall / Rollback

To uninstall the patch:
1. delete the files added by this patch:
   - `C:\sys\bin\btrcc.dll`
   - `C:\sys\bin\btaccserver.exe`
   - `C:\resource\plugins\btrcc.rsc`
2. Reboot your phone.

**Important:** Do not delete or modify files on the `Z:` drive. The original ROM files remain untouched by this patch. Removing the added files from `C:` allows the system to fall back to the original ROM files, provided no previous files on `C:` need to be restored.

## Disclaimer

Use at your own risk. Back up existing files before installation.
