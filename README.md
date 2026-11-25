# Morgan Flasher

A single-page web app for writing firmware images to ESP32-S3 boards over Web Serial,
built on Espressif's [esptool-js](https://github.com/espressif/esptool-js).

**Use it:** https://jckf.github.io/morgan-flasher/

Requires Chrome, Edge or Opera on desktop (Web Serial), served over `https://` or `http://localhost`.

## Features

- Connect over Web Serial; works with both USB-UART bridges and the ESP32-S3's native USB.
- Flash one or more `.bin` images at chosen addresses, with compression and MD5 verification.
- Optional full-chip erase, plus erase-only and reset buttons.
- Bundled firmware presets, listed in [`firmware/manifest.json`](firmware/manifest.json).

## Bundled firmware

Unofficial Meshtastic builds for the Heltec V4 R8 TFT. See [`firmware/README.md`](firmware/README.md)
for exactly what is in them and how they were built.

## Running locally

```sh
python3 -m http.server 8000
# open http://localhost:8000/
```
