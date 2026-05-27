# LoTraQ Android

Current public Android build:

- [lotraq-v1.2.0-direct-release-signed.apk](lotraq-v1.2.0-direct-release-signed.apk)
- SHA-256: `2209cdc079c42b8b14c42b76f3af3f165646cdf0ff7fce5fbcf88394c6c026b5`
- Android 8.0+ / API 26+
- `arm64-v8a` phones only
- Package: `com.olderthanold.lotraq`

This is a direct-download APK, not a Play Store release.

## Install

1. Download the current APK above.
2. On Android, allow installing apps from your browser or file manager when
   prompted.
3. Install the APK.
4. Open LoTraQ.
5. Open Settings, then download or import a model.
6. Return to the main screen, choose source and target languages, paste text,
   then tap Translate. You can also tap Load first to prepare the selected
   model.

Model files are large, so use Wi-Fi or unlimited data for the first download.
After a model is installed, translation runs locally.

## What's New In Android 1.2

- Per-model backend preference: `AUTO`, `GPU`, or `CPU`.
- Main-screen backend badge for the effective runtime: `GPU`, `CPU slow!`, or
  `NPU` when reported by the runtime.
- Per-model MTP/speculative decoding checkbox for supported Gemma 4 models.
- Inline memory readout and low-memory guidance before large model loads.
- More detailed runtime diagnostics around load and generation.
- Token speed in status and new history entries.
- Safer runtime release when model, backend, MTP, or Android memory state
  changes.

See [RELEASE_NOTES.md](RELEASE_NOTES.md) for the full Android release notes.

## Signing And Upgrades

The current Android direct-release APK is signed with:

`CN=LoTraQ Android Direct Release, O=olderthanold, C=CZ`

Certificate SHA-256:

`9442929100009509128be02aace10cae4be0fed5d678cc1408cd649e32288d5c`
