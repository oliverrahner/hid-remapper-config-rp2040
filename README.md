# HID Remapper Config for Feather RP2040 USB Host

USB keyboard remapper using [HID Remapper](https://github.com/jfedor2/hid-remapper) on an [Adafruit Feather RP2040 USB Host](https://www.adafruit.com/product/5723).

Turns a "dumb" USB keyboard (Periboard 535) into a fully remappable one — no software running on the computer needed.

```
Periboard 535 → [USB-A] Feather RP2040 USB Host [USB-C] → Computer
```

## Firmware

The GitHub Actions workflow builds `remapper_feather.uf2` automatically on every push. Download it from the workflow artifacts.

Alternatively, grab a pre-built release from [HID Remapper releases](https://github.com/jfedor2/hid-remapper/releases) (`remapper_feather.uf2`).

## Flashing

1. Hold the **Boot** button on the Feather
2. Press **Reset** while holding Boot
3. A USB drive named `RPI-RP2` appears
4. Copy `remapper_feather.uf2` to the drive
5. The board reboots automatically with the new firmware

## Configuration

1. Plug the keyboard into the Feather's USB-A port
2. Connect the Feather's USB-C port to your computer
3. Open [remapper.org/config](https://remapper.org/config) in Chrome
4. Click **Open device** and select the remapper
5. Set up your key remappings
6. Export your config JSON into the `config/` directory for version control
