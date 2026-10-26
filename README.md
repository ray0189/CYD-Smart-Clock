# CYD Smart Clock ⏰🌦️

A touchscreen smart clock and weather dashboard for the **ESP32 Cheap Yellow Display (CYD)**.

> Firmware package: **v2.5.3**. This repository documents the device used for the project. The firmware binaries and full source package still need to be uploaded.

## Hardware used

| Component | Details |
| --- | --- |
| Board | ESP32-2432S028R (Cheap Yellow Display) |
| Display | 2.8-inch TFT touchscreen, 320 × 240 pixels |
| USB connections | **USB-C and Micro-USB** (dual-USB CYD / CYD2USB) |
| Enclosure | White plastic case |
| Correct firmware build | `firmware/cyd-clock-cyd-2usb-merged.bin` |
| Development | PlatformIO / ESP32 |

**Important:** This is the **dual-USB** board. Do not flash the single-USB image without checking your hardware revision. No external GPS module is used.

## Planned dashboard features

- Clock and date, weather conditions and forecasts
- Sunrise and sunset information
- Air quality and pollen information where supported by data providers
- Touch navigation, brightness and night-mode controls
- Wi-Fi setup, web configuration and over-the-air updates
- Optional Ring doorbell notifications via a separately configured relay

Feature availability depends on the firmware build, connected services, and configuration. Ring integration is **not** a fully offline or direct ESP32-to-camera video stream.

## Flashing

1. Identify your board: **ESP32-2432S028R, dual USB**.
2. Back up any settings you need.
3. Obtain the matching **CYD2USB** merged firmware image from the project package.
4. Flash the merged image at address `0x0` with a compatible ESP32 flasher.
5. Reboot, connect to Wi-Fi, and configure your preferred weather location.

**Power note:** Some inexpensive CYD boards do not negotiate USB-C-to-USB-C power correctly. If a USB-C PD charger leaves the board completely off, try USB-A to USB-C or Micro-USB power.

## Security

Never commit personal Wi-Fi passwords, API keys, Ring OAuth tokens, Cloudflare secrets, or real device credentials. Configure secrets locally or through the appropriate deployment secret manager.

## Status

Documentation initialised. Full source code, simulator assets and firmware binaries are **not yet committed**.
