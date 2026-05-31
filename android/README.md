# LoTraQ Android

Current public Android build:

- [lotraq-v1.4.0-direct-release-signed.apk](lotraq-v1.4.0-direct-release-signed.apk)
- SHA-256: `6210f372ee122e7cda644d2c5ee9e3477345a623201bb6948560442063d4cc75`
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

## What's New In Android 1.4

- Simple/Advanced Settings mode.
- Simple Settings keeps only theme, translation instructions, and standard
  model Select buttons.
- Advanced Settings keeps model download/import/delete, backend, context, MTP,
  sampling, and status controls.
- Photo OCR can now capture a temporary camera photo.
- Captured OCR photos stay in app-private cache by default.
- Save pic explicitly preserves the current OCR image.
- Old temporary OCR camera cache is cleaned automatically.
- Help dialogs are structured into short readable sections.

See [RELEASE_NOTES.md](RELEASE_NOTES.md) for the full Android release notes.

## Signing And Upgrades

The current Android direct-release APK is signed with:

`CN=LoTraQ Android Direct Release, O=olderthanold, C=CZ`

Certificate SHA-256:

`9442929100009509128be02aace10cae4be0fed5d678cc1408cd649e32288d5c`
