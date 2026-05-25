# LoTraQ

**Free local AI translation. Android direct APK now, Windows MVP preview now.
No ads, no account, no cloud translation.**

LoTraQ is built for people who want a practical translator that runs on their
own device. Paste text, choose languages, load a local AI model, translate, and
copy the result. After a model is downloaded or imported, translation runs
locally.

<img src="assets/lotraq-android-main.png" alt="LoTraQ Android translating Czech text to English" width="360">

## Android Download

Current public Android build:

- [lotraq-v1.1.0-direct-release-signed.apk](android/lotraq-v1.1.0-direct-release-signed.apk)
- SHA-256: `c0a2d7d791d61604646213537967ef67e27017fdf848c732cc6f87f39c3eba08`
- Android 8.0+ / API 26+
- `arm64-v8a` phones only
- Package: `com.olderthanold.lotraq`

This is a direct-download APK, not a Play Store release.

See [android/README.md](android/README.md) for Android install, signing, and
upgrade notes.

## Windows MVP Download

Current Windows MVP build:

- [lotraq_win_MVP.7z](windows/lotraq_win_MVP.7z)
- SHA-256: `1d27507c918acd1837b4ca729466836e8ed20b746580955bdb6d3250ae51e7f8`
- Windows 11 x64
- Portable 7z archive, no installer
- Includes the LoTraQ WPF app and pinned local `llama.cpp` CPU/Vulkan runtimes
- Does not include a GGUF model

This is a very small MVP preview. It is useful for local GGUF testing, but it
is not a polished Windows product yet. The Windows MVP executables are not code
signed, so Windows SmartScreen or antivirus tools may warn before first run.

See [windows/README.md](windows/README.md) for Windows MVP setup and limits.

## What It Does

- Translates text locally on-device/on-machine.
- Supports English plus 55 target locales, including Czech, German, French,
  Spanish, Japanese, Korean, Chinese, Ukrainian, and more.
- Keeps local translation history.
- Lets you copy source text, translated text, and history items.
- Android supports LiteRT-LM `.litertlm` model download, import, delete, and
  visible load status.
- Windows MVP supports local GGUF import and local `llama.cpp` CPU/Vulkan
  inference through a private `127.0.0.1` process.
- Shows practical runtime feedback such as loaded/not loaded, generation time,
  first-token latency, output tokens, and speed where available.

## Android Quick Start

1. Download the current APK from the Android link above.
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

## Windows MVP Quick Start

1. Download `lotraq_win_MVP.7z`.
2. Extract the 7z archive to a normal writable folder.
3. Double-click `Run-LoTraQ.cmd`.
4. Open Settings.
5. Use `Import GGUF` and select a local TranslateGemma GGUF model.
6. Return to Main, choose languages, paste text, then translate.

Keep the extracted folder together. The MVP expects its app files and bundled
runtime folders to stay next to `Run-LoTraQ.cmd`.

## Models

Android 1.1 uses LiteRT-LM models:

| Model | Role | Size | Notes |
| --- | --- | ---: | --- |
| Gemma 4 E2B IT LiteRT-LM | Default | 2.59 GB | Fast LiteRT target for phone use. |
| TranslateGemma 4B INT4 LiteRT-LM | Optional | 2.01 GB | Translation-tuned; CPU fallback is slow on the tested phone. |
| Gemma 4 E4B IT LiteRT-LM | Optional | 3.66 GB | Larger memory-pressure test; may fail on smaller phones. |

Windows MVP uses GGUF through `llama.cpp` and does not bundle a model:

| Model | Role | Size | Notes |
| --- | --- | ---: | --- |
| TranslateGemma 4B IT Q4_K_S GGUF | Suggested MVP model | 2.38 GB | Validated local smoke candidate; import your own local file. |

## Privacy

LoTraQ does not require an account and does not send your source text or
translations to a server. Android can connect to model hosts when you download
a model. Windows MVP uses local model import and local `127.0.0.1` inference.
See [PRIVACY.md](PRIVACY.md).

## Source

This repository is only for public release downloads and notices. Development
source is maintained separately so this repo can stay small and focused.

See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for model, runtime, and
third-party notices.
