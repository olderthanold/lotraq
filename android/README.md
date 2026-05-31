# LoTraQ Android

Current public Android build:

- [lotraq-v1.5.0-direct-release-signed.apk](lotraq-v1.5.0-direct-release-signed.apk)
- SHA-256: `0562a0ac897562c03be1dfafd6d85903c1ff376bf485df299913feddabcde946`
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

## What's New In Android 1.5

- Model OCR path for installed Gemma 4 E2B/E4B vision-capable LiteRT-LM models.
- Persistent OCR engine dropdown: Latin OCR plus installed Gemma OCR engines.
- OCR model selection is independent from the selected translation model.
- OCR runtime status for ready, loading, extracting, and failure states.
- Latin OCR remains the default and is Latin-script only.
- Simple Settings keeps standard model Select, Download, and Delete actions.
- Same-language Source and Target now run rewrite mode using Translation
  instructions.
- Custom model OCR capability is not auto-detected in Android 1.5.

See [RELEASE_NOTES.md](RELEASE_NOTES.md) for the full Android release notes.

## Signing And Upgrades

The current Android direct-release APK is signed with:

`CN=LoTraQ Android Direct Release, O=olderthanold, C=CZ`

Certificate SHA-256:

`9442929100009509128be02aace10cae4be0fed5d678cc1408cd649e32288d5c`
