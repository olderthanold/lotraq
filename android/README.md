# LoTraQ Android

Current public Android build:

- [lotraq-v1.3.0-direct-release-signed.apk](lotraq-v1.3.0-direct-release-signed.apk)
- SHA-256: `b68b7fccd4a3e1a30236af7cae0f43859884355973836eb1a7970e5a077fa882`
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

## What's New In Android 1.3

- Photo OCR from saved images, editable extracted text, and Translate handoff.
- Local custom `.litertlm` model imports for non-standard LiteRT-LM models.
- Numeric per-model context setting with shown default and max.
- Swipe navigation between Main and Photo OCR.
- Screen and loaded-model state preserved across orientation changes.
- Shorter inline memory readout and Settings version display.
- Custom model import is local-file only; no custom URL or model registry is
  included in Android 1.3.

See [RELEASE_NOTES.md](RELEASE_NOTES.md) for the full Android release notes.

## Signing And Upgrades

The current Android direct-release APK is signed with:

`CN=LoTraQ Android Direct Release, O=olderthanold, C=CZ`

Certificate SHA-256:

`9442929100009509128be02aace10cae4be0fed5d678cc1408cd649e32288d5c`
