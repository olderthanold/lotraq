# LoTraQ Android Release Notes

## 1.5.1 - 2026-07-20

Download:

- [lotraq-v1.5.1-direct-release-signed.apk](lotraq-v1.5.1-direct-release-signed.apk)
- SHA-256: `6290937ff3516a3a7b37198e9758475a60690dae7fdc81e7fca6c8704418ccd6`
- Android `versionName`: `1.5.1`
- Android `versionCode`: `151`
- Package: `com.olderthanold.lotraq`

New in Android 1.5.1:

- Upgraded the Android LiteRT-LM runtime dependency from `0.12.0` to `0.14.0`.
- Kept the Android 1.5 app behavior and model set unchanged.
- Smoke-tested signed install, model auto-load, and TranslateGemma 4B CPU
  translation on the connected Samsung SM-S911B.

Signing:

Android 1.5.1 is signed with the same direct-download release certificate:

`CN=LoTraQ Android Direct Release, O=olderthanold, C=CZ`

Certificate SHA-256:

`9442929100009509128be02aace10cae4be0fed5d678cc1408cd649e32288d5c`

## 1.5.0 - 2026-05-31

Download:

- [lotraq-v1.5.0-direct-release-signed.apk](lotraq-v1.5.0-direct-release-signed.apk)
- SHA-256: `0562a0ac897562c03be1dfafd6d85903c1ff376bf485df299913feddabcde946`
- Android `versionName`: `1.5.0`
- Android `versionCode`: `150`
- Package: `com.olderthanold.lotraq`

New in Android 1.5:

- Added Model OCR for installed Gemma 4 E2B/E4B vision-capable LiteRT-LM
  models.
- Kept fast Latin ML Kit OCR as the default OCR engine.
- Added persistent OCR engine dropdown: Latin OCR plus installed Gemma OCR
  engines.
- Made OCR model selection independent from the selected translation model.
- Added OCR runtime status for ready, loading, extracting, and failure states.
- Configured LiteRT-LM vision backend and image input for Gemma 4 E2B/E4B OCR.
- Kept standard model Select, Download, and Delete actions visible in Simple
  Settings.
- Allowed same-language Source and Target as rewrite mode driven by Translation
  instructions.

Signing:

Android 1.5.0 is signed with the same direct-download release certificate:

`CN=LoTraQ Android Direct Release, O=olderthanold, C=CZ`

Certificate SHA-256:

`9442929100009509128be02aace10cae4be0fed5d678cc1408cd649e32288d5c`

## 1.4.0 - 2026-05-29

Download:

- [lotraq-v1.4.0-direct-release-signed.apk](lotraq-v1.4.0-direct-release-signed.apk)
- SHA-256: `6210f372ee122e7cda644d2c5ee9e3477345a623201bb6948560442063d4cc75`
- Android `versionName`: `1.4.0`
- Android `versionCode`: `140`
- Package: `com.olderthanold.lotraq`

New in Android 1.4:

- Added persistent Simple/Advanced Settings mode.
- Kept Main unchanged.
- Kept Advanced as the default so setup controls remain visible on fresh
  installs.
- Simple Settings shows only mode, theme, translation instructions, and the
  three standard model rows with Select.
- Added Photo OCR camera capture through the system camera.
- Kept captured OCR photos temporary in app-private cache by default.
- Added explicit Save pic action for preserving the current OCR image.
- Added daily cleanup for old temporary OCR camera files.
- Reworked app help dialogs into short readable sections.
- Made Settings help mode-aware for Simple and Advanced.

Signing:

Android 1.4.0 is signed with the same direct-download release certificate:

`CN=LoTraQ Android Direct Release, O=olderthanold, C=CZ`

Certificate SHA-256:

`9442929100009509128be02aace10cae4be0fed5d678cc1408cd649e32288d5c`

## 1.3.0 - 2026-05-29

Download:

- [lotraq-v1.3.0-direct-release-signed.apk](lotraq-v1.3.0-direct-release-signed.apk)
- SHA-256: `b68b7fccd4a3e1a30236af7cae0f43859884355973836eb1a7970e5a077fa882`
- Android `versionName`: `1.3.0`
- Android `versionCode`: `130`
- Package: `com.olderthanold.lotraq`

New in Android 1.3:

- Added Photo OCR for saved images.
- Added image attach, preview, persistent preview collapse state, OCR text
  extraction, editable extracted text, and Translate handoff to Main.
- Added local custom `.litertlm` model imports for non-standard LiteRT-LM
  models.
- Imported/unknown `.litertlm` models use default context `2048`, app cap
  `32768`, and no model-specific MTP toggle.
- Added numeric per-model runtime context setting.
- Shows per-model context default and maximum in Settings.
- Validates context input before saving.
- Passes the effective context size to LiteRT-LM before model initialization.
- Added swipe navigation between Main and Photo OCR.
- Preserves current screen and loaded model state across orientation changes.
- Keeps the loaded runtime when Android only reports `TRIM_MEMORY_UI_HIDDEN`.
- Added Settings version display.
- Shortened the inline memory readout.

Signing:

Android 1.3.0 is signed with the same direct-download release certificate:

`CN=LoTraQ Android Direct Release, O=olderthanold, C=CZ`

Certificate SHA-256:

`9442929100009509128be02aace10cae4be0fed5d678cc1408cd649e32288d5c`

## 1.2.0 - 2026-05-27

Download:

- [lotraq-v1.2.0-direct-release-signed.apk](lotraq-v1.2.0-direct-release-signed.apk)
- SHA-256: `2209cdc079c42b8b14c42b76f3af3f165646cdf0ff7fce5fbcf88394c6c026b5`
- Android `versionName`: `1.2.0`
- Android `versionCode`: `120`
- Package: `com.olderthanold.lotraq`

New in Android 1.2:

- Added per-model backend preference: `AUTO`, `GPU`, or `CPU`.
- Added effective backend badge on Main: `GPU`, `CPU slow!`, or `NPU`.
- Added per-model MTP/speculative decoding checkbox for supported Gemma 4
  models.
- Added runtime capability checks for speculative decoding.
- Kept MTP off by default after phone tests showed slower output and higher
  memory use on the tested device.
- Added inline memory readout on Main.
- Added detailed memory diagnostics around load and generation.
- Added E2B/E4B memory preflight and clearer low-memory messages.
- Released the native runtime immediately when model, backend, or MTP changes.
- Released the loaded model on Android memory trim.
- Improved status speed to prefer `tok/s`.
- Added token speed to new history entries.
- Clarified Help text for low memory and MTP behavior.

Signing:

Android 1.2.0 is signed with the same direct-download release certificate:

`CN=LoTraQ Android Direct Release, O=olderthanold, C=CZ`

Certificate SHA-256:

`9442929100009509128be02aace10cae4be0fed5d678cc1408cd649e32288d5c`
