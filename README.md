# Flipper Zero Animation Assets

This repository contains animation assets prepared for Flipper Zero firmware layouts.

Current folders in this repo:

- `o_firmare/` for the official-firmware style bundle
- `momentum/` for Momentum asset-pack layouts

The folder names above are the real paths in this repository. They are kept as-is so the copy steps below match the files on disk exactly.

## Supported layouts

- Flipper Official Firmware
- Momentum Firmware
- Other third-party firmwares that use either:
  - an `asset_packs`-style layout
  - a `dolphin` animation layout

RogueMaster is included here as a third-party example, but this repository does not define a RogueMaster-specific path. Check your firmware documentation before replacing files.

## Repository layout

### Official firmware bundle

Source folder: `./o_firmare/`

Current contents:

- `manifest.txt`
- `Voidfrida/`
- `RFVillageMx/`

Important: the official bundle currently ships with one shared `manifest.txt`. Back up your existing `SD Card/dolphin/manifest.txt` before replacing it.

### Momentum packs

Source root: `./momentum/`

Current packs:

- `momentum/voidfrida/`
- `momentum/rf_village_mx/`

Each pack already includes its own `Anims/` folder and animation files.

## Install on Flipper Official Firmware

Destination on SD card: `SD Card/dolphin/`

Steps:

1. Connect the SD card to your computer.
2. Open `SD Card/dolphin/`.
3. Back up your current `manifest.txt` and any animation folders you plan to replace.
4. Copy `./o_firmare/manifest.txt` into `SD Card/dolphin/`.
5. Copy the animation folder you want from `./o_firmare/`, such as `Voidfrida/` or `RFVillageMx/`, into `SD Card/dolphin/`.
6. Safely eject the SD card and restart the device if the animation does not refresh immediately.

## Update or replace on Flipper Official Firmware

1. Back up `SD Card/dolphin/manifest.txt`.
2. If the animation folder already exists on the SD card, remove the old folder first or overwrite it completely.
3. Copy the replacement folder from `./o_firmare/`.
4. Replace `SD Card/dolphin/manifest.txt` with `./o_firmare/manifest.txt` if you want to use the bundle definition included in this repository.
5. Reboot the Flipper if the old animation still appears.

## Install on Momentum

Destination on SD card: `SD Card/asset_packs/`

Steps:

1. Connect the SD card to your computer.
2. Open `SD Card/asset_packs/`.
3. Choose one pack directory from `./momentum/`, for example `voidfrida/` or `rf_village_mx/`.
4. Copy that full directory into `SD Card/asset_packs/`.
5. Safely eject the SD card.
6. Select or refresh the asset pack from Momentum if needed on the device.

## Update or replace on Momentum

1. Open `SD Card/asset_packs/`.
2. If a pack with the same name already exists, back it up first.
3. Delete the old pack folder or overwrite it fully with the matching directory from `./momentum/`.
4. Reinsert the SD card and reload the pack from the firmware menu if it does not update automatically.

## Generic third-party firmware instructions

Use these steps for third-party firmware such as RogueMaster when the exact layout is not defined in this repository.

- If your firmware uses `asset_packs`, follow the Momentum steps.
- If your firmware uses `dolphin` animation folders plus `manifest.txt`, follow the official firmware steps.
- If your firmware uses a different asset location, check its documentation first and then copy the files from the matching repo layout in this project.

Do not assume every third-party firmware uses the same folder structure.

## Quick verification checklist

After copying files:

- Confirm the destination folder contains the new animation files.
- Confirm `meta.txt` and `frame_*.bm` files are present inside the copied animation folder.
- Confirm `manifest.txt` was replaced only when you intended to replace it.
- Restart the device if the old animation still appears.

## Naming notes

This repository currently uses the path names `o_firmare/` and `momentum/`.

- `o_firmare/` is the current official-firmware source path in this repo.
- Older references such as `o_firmware` or `momemtum` are incorrect for this repository and should not be used when copying files.
