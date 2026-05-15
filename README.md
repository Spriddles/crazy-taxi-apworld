# Crazy Taxi APWorld

Crazy Taxi GameCube/Dolphin APWorld for Archipelago.

This is a public beta for **Crazy Taxi GameCube** running through **Dolphin Emulator**.

## Requirements

- Archipelago 0.6.7
- Dolphin Emulator
- Crazy Taxi GameCube
- Python package: `dolphin-memory-engine`

## Install dependency

### Windows

```powershell
py -m pip install dolphin-memory-engine

Ubuntu / Linux
python3 -m pip install --user --break-system-packages dolphin-memory-engine

Install APWorld

Place the .apworld file in your Archipelago custom worlds folder.

Windows

Usually:

C:\ProgramData\Archipelago\custom_worlds

Ubuntu / Linux

Using the Archipelago Appimage:

~/.local/share/Archipelago/worlds

GCI save path setup

The client needs access to Dolphin's GameCube memory card save folder.

Windows

Example:

$env:CRAZY_TAXI_GCI_PATH="C:\Users\<YourName>\AppData\Roaming\Dolphin Emulator\GC\USA\Card A"

Then launch Archipelago from the same PowerShell window.

Ubuntu / Linux Flatpak Dolphin

Example:

export CRAZY_TAXI_GCI_PATH="$HOME/.var/app/org.DolphinEmu.dolphin-emu/data/dolphin-emu/GC/USA/Card A"

Then launch Archipelago from the same terminal.

Client commands
/ct_attach

Attach or re-attach to Dolphin.

/ct_status

Show current Crazy Taxi memory values.

/ct_gci

Show the detected GCI save file and Crazy Box flags.

/ct_mode crazybox

Use before playing Crazy Box stages. This disables fare checks while Crazy Box is active.

/ct_mode arcade

Use when returning to Arcade fare checks.

/ct_switch 4
/ct_range 4
/ct_switch Fare License 4

Switch to a specific Fare License range if unlocked.

Features
Fare checks
Crazy Box checks
GCI save polling for Crazy Box completion
Crazy Box AP-unlock send gate
Scalable fare block count
Scalable Crazy Box goal requirement
Progressive and non-progressive Fare License modes
Manual fare range switching
Automatic jump to next unlocked incomplete fare range
Timer extension/reduction items
Known beta limitations
Crazy Box stage lockout is not enforced in-game yet.
Use /ct_mode crazybox before playing Crazy Box stages.
Use /ct_mode arcade before returning to Arcade fares.
Failed fare / DeathLink behavior is currently disabled or experimental.
This is a beta release and needs wider testing across Dolphin versions.
