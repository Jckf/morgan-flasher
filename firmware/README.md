# Bundled firmware

## Meshtastic 2.8.3.7aba92f — Heltec V4 R8 TFT (unofficial)

Built locally on 2026-11-25 with PlatformIO, env `heltec-v4-r8-tft`. Not an official
Meshtastic release.

| File | Address | Purpose |
| --- | --- | --- |
| `firmware-heltec-v4-r8-tft-2.8.3.7aba92f.factory.bin` | `0x0` | Bootloader, partition table and app (full install) |
| `mt-esp32s3-ota.bin` | `0x650000` | Meshtastic unified OTA loader, [esp32-unified-ota v1.0.1](https://github.com/meshtastic/esp32-unified-ota/releases/tag/v1.0.1), unmodified |
| `littlefs-heltec-v4-r8-tft-2.8.3.7aba92f.bin` | `0xc90000` | Filesystem image (full install) |
| `firmware-heltec-v4-r8-tft-2.8.3.7aba92f.bin` | `0x10000` | App only (update) |

### Source

All of it is public:

1. [`Jckf/mt-firmware@4d5a36f`](https://github.com/Jckf/mt-firmware/commit/4d5a36ff6ec74b8b5c41cded5389a4c7a9b93840)
   (`jckf/powerlimit`): upstream [`meshtastic/firmware@b3215ce`](https://github.com/meshtastic/firmware/commit/b3215cefe489f8682663f66822154d6c9ce746b3)
   with the EU_868 / EU_866 / EU_N_868 power limit raised from 27 to 30 dBm.
2. Merged with [meshtastic/firmware#11559](https://github.com/meshtastic/firmware/pull/11559)
   at [`7fe1bd7`](https://github.com/meshtastic/firmware/commit/7fe1bd733172f06837a6511f100440459459a5bb).
3. device-ui pinned to [meshtastic/device-ui#502](https://github.com/meshtastic/device-ui/pull/502)
   at [`t-miura/device-ui@f7c8d40`](https://github.com/t-miura/device-ui/commit/f7c8d4029adf916d15fe470b884cd64e774bc203)
   in place of `fb3c069` (#502 is `fb3c069` plus three commits). These two PRs fix the displayed
   frequency on narrow presets in Meshtastic UI.

The `7aba92f` in the version string is the local commit combining these, which was not published.

Meshtastic is GPL-3.0; the sources above are the corresponding source for these binaries.

**Compliance with local radio regulations is the operator's responsibility.**
