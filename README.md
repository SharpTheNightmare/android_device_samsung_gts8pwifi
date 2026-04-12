# Device Tree for Samsung Galaxy Tab S8+ WiFi

## Device specifications

| Feature | Specification |
|---------|---------------|
| Chipset | Qualcomm Snapdragon 8 Gen 1 (SM8450) |
| CPU | 1x Cortex-X2 @ 3.0 GHz + 3x Cortex-A710 @ 2.5 GHz + 4x Cortex-A510 @ 1.8 GHz |
| GPU | Adreno 730 |
| Memory | 8 GB LPDDR5 |
| Storage | 128/256 GB UFS 3.1 |
| Display | 12.4" Super AMOLED, 2800x1752, 120Hz |
| Battery | 10090 mAh |
| Rear Camera | 13 MP |
| Front Camera | 12 MP |
| Android Version | Android 12 (launched), upgradeable to Android 14 |

## Device codename
`gts8pwifi`

## Supported models
- SM-X800 (Galaxy Tab S8+ WiFi)

## Encryption support
This tree supports FBE (File-Based Encryption) decryption using the Qualcomm inline crypto stack (`aes-256-xts:aes-256-cts:v2+inlinecrypt_optimized+wrappedkey_v0`).

Required vendor binaries at runtime:
- `/vendor/bin/qseecomd`
- `/vendor/bin/hw/android.hardware.security.keymint-service`
- `/vendor/bin/hw/android.hardware.gatekeeper@1.0-service`

## Flashing
Flash via Odin using the `.tar` output, or via `adb sideload` / `fastboot flash recovery recovery.img`.

## Notes
- Prebuilt kernel, DTB, and recovery DTBO are from stock Samsung firmware (build `X800XXS9CYB1`)
- Boot image uses header v2 with board string `SRPUH24B002` and appends `SEANDROIDENFORCE` for Samsung bootloader compatibility
- Download mode: hold **Volume Down + Power** until the device reboots into download mode

## Credits
- [afaneh92](https://github.com/afaneh92) — original device tree base
