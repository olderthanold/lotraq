# LoTraQ Windows MVP

Current Windows MVP build:

- [lotraq_win_MVP.7z](lotraq_win_MVP.7z)
- SHA-256: `1d27507c918acd1837b4ca729466836e8ed20b746580955bdb6d3250ae51e7f8`
- Windows 11 x64
- Portable 7z archive, no installer

This is a minimal MVP preview. It is intentionally rough and focused on proving
local Windows translation with GGUF and `llama.cpp`.

The executables are not code signed. Windows SmartScreen or antivirus tools may
warn before first run.

## Run

1. Download `lotraq_win_MVP.7z`.
2. Extract the 7z archive to a normal writable folder.
3. Double-click `Run-LoTraQ.cmd`.
4. Open Settings.
5. Use `Import GGUF` and select a local TranslateGemma GGUF model.
6. Return to Main, choose languages, paste text, then translate.

Keep the extracted folder together. The app, runtime files, and
`Run-LoTraQ.cmd` are expected to stay in the same extracted package.

## What Is Included

- LoTraQ Windows WPF app.
- Self-contained .NET runtime files.
- Pinned `llama.cpp` Windows x64 CPU runtime.
- Pinned `llama.cpp` Windows x64 Vulkan runtime.

## What Is Not Included

- No GGUF model file.
- No installer.
- No automatic model download flow.
- No polished Windows release UX.

## Model

The intended MVP model is a local TranslateGemma GGUF file:

- Model: `TranslateGemma 4B IT Q4_K_S GGUF`
- Expected file name: `translategemma-4b-it.Q4_K_S.gguf`
- Expected size: `2,377,945,600` bytes
- Expected SHA-256: `95c62e1c29f977c84fe5a5d9602a91213fd03a2c7b63f2884abab2ed7b5c5f57`

The archive does not include this model. Import your own local copy in Settings.

## Privacy

The Windows MVP runs translation locally. It starts a bundled `llama-server.exe`
process on `127.0.0.1` and sends the rendered prompt to that local process. It
does not send source text or translations to a remote server.

Other local processes on the same machine may be able to connect to that
localhost process while it is running.

The MVP may create local settings, history, cache, temporary, and log files
inside the extracted app folder while it runs. If that folder is not writable,
the app uses `%LOCALAPPDATA%\LoTraQ`.

## Known MVP Limits

- Import/select local GGUF is present.
- Model download, delete, partial resume, and checksum verification are not the
  Windows MVP flow yet.
- Output streaming is not polished yet.
- CPU can be slow; Vulkan depends on local GPU and driver support.
- The archive includes debug symbol `.pdb` files because this is an MVP build.
