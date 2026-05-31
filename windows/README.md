# LoTraQ Windows 1.2

Current Windows 1.2 build:

- [lotraq-windows-v1.2.0-win-x64.7z](lotraq-windows-v1.2.0-win-x64.7z)
- SHA-256: `2f76a108f0c5174a6e872c0f4ba846dc0a0b53e116a455fe06316199625920fa`
- Windows 11 x64
- Portable 7z archive, no installer

This is a Windows preview focused on local Windows translation with GGUF and
`llama.cpp`.

The executables are not code signed. Windows SmartScreen or antivirus tools may
warn before first run.

This rerelease replaces the earlier Windows 1.2 archive. It keeps the same
version number and fixes model-management, streaming/thinking, and
same-language rewrite gaps from the first Windows 1.2 package.

## Run

1. Download `lotraq-windows-v1.2.0-win-x64.7z`.
2. Extract the 7z archive to a normal writable folder.
3. Double-click `Run-LoTraQ.cmd`.
4. Open Settings.
5. Use `Download` for the standard TranslateGemma GGUF, or `Add GGUF` to
   reference an existing local GGUF file.
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
- No bundled model file.
- No polished installer UX.
- No code signing.

## Model

The intended Windows 1.2 model is a local TranslateGemma GGUF file:

- Model: `TranslateGemma 4B IT Q4_K_S GGUF`
- Expected file name: `translategemma-4b-it.Q4_K_S.gguf`
- Expected size: `2,377,945,600` bytes
- Expected SHA-256: `95c62e1c29f977c84fe5a5d9602a91213fd03a2c7b63f2884abab2ed7b5c5f57`

The archive does not include this model. Download it in Settings, or add your
own local copy.

## Rerelease Notes

- Standard TranslateGemma GGUF download is available from Settings.
- `Add GGUF` references an existing local file without copying or renaming it.
- `Delete` removes app-owned downloaded models; external GGUF files are removed
  from LoTraQ profiles only and are not deleted from disk.
- Streaming output is enabled by default.
- Thinking-capable chat models keep reasoning in a collapsed Thinking panel and
  final text in Translation.
- Sampling, streaming, and thinking changes do not reload the model; model,
  backend, and context changes still require reload.
- Matching source and target languages are valid rewrite/cleanup tasks driven
  by the active instructions.
- Leading model labels such as `Translation:` are stripped from final output.

## Privacy

The Windows build runs translation locally. It starts a bundled `llama-server.exe`
process on `127.0.0.1` and sends the rendered prompt to that local process. It
does not send source text or translations to a remote server.

Other local processes on the same machine may be able to connect to that
localhost process while it is running.

The app may create local settings, history, cache, temporary, and log files
inside the extracted app folder while it runs. If that folder is not writable,
the app uses `%LOCALAPPDATA%\LoTraQ`.

## Known Limits

- Settings can download the standard TranslateGemma GGUF, reference an external
  GGUF file, and remove/delete model profiles.
- Streaming output is enabled by default.
- Thinking mode is model-specific. Qwen-style thinking is usable; Nanbeige
  thinking is separated but low quality and should usually stay disabled.
- Matching source and target languages are allowed for rewrite/cleanup tasks.
- In-app help/tooltips for model management, backend, context, streaming, and
  thinking are still deferred.
- CPU can be slow; Vulkan depends on local GPU and driver support.
- The archive includes debug symbol `.pdb` files because this is still a preview
  build.
