# Supported hardware

## Tested project target

- **Board:** ESP32-2432S028R, commonly called the 2.8-inch Cheap Yellow Display (CYD)
- **USB:** Both USB-C and Micro-USB ports (**CYD2USB / dual-USB variant**)
- **Display:** 320 × 240 TFT touchscreen
- **Enclosure:** White plastic
- **GPS:** No external GPS module
- **Firmware image from supplied v2.5.3 archive:** `cyd-clock-cyd-2usb-merged.bin`

The presence of two USB ports identifies the intended build family, but board revisions can differ in display/touch wiring. Verify the exact PCB markings if a flash results in a blank screen.

## Firmware and power

The dual-USB build is distinct from the single-USB build. A USB-C PD charger may not supply power over a C-to-C cable if the board lacks proper USB-C CC detection circuitry; this is a hardware issue, not a firmware setting.
