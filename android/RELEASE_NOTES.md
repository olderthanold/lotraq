# LoTraQ Android Release Notes

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

Still intentionally not exposed in Android 1.3:

- No user-facing max-output control.
- No thinking-mode UI.
- No Android NPU backend selector.
- No camera capture; OCR uses saved image attach only.
- OCR is Latin-script text recognition only in Android 1.3.
- No custom URL, Hugging Face resolver, or custom model registry.
- No Word/document translation.
- No translation memory/session context.

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

Still intentionally not exposed in Android 1.2:

- No user-facing context-size slider.
- No user-facing max-output control.
- No thinking-mode UI.
- No Android NPU backend selector.
- No camera/image translation.
- No Word/document translation.
- No translation memory/session context.

Signing:

Android 1.2.0 is signed with the same direct-download release certificate:

`CN=LoTraQ Android Direct Release, O=olderthanold, C=CZ`

Certificate SHA-256:

`9442929100009509128be02aace10cae4be0fed5d678cc1408cd649e32288d5c`
