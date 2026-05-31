# LoTraQ Windows Release Notes

## 1.2.0 Rerelease - 2026-05-31

Download:

- [lotraq-windows-v1.2.0-win-x64.7z](lotraq-windows-v1.2.0-win-x64.7z)
- SHA-256: `2f76a108f0c5174a6e872c0f4ba846dc0a0b53e116a455fe06316199625920fa`
- Windows 11 x64
- Portable 7z archive, no installer

This rerelease keeps the Windows 1.2 version number and replaces the earlier
Windows 1.2 archive.

Fixed / improved:

- Standard TranslateGemma GGUF download is available from Settings.
- `Add GGUF` references an existing local GGUF file without copying it.
- `Delete` deletes app-owned downloaded model files, while external GGUF files
  are only removed from LoTraQ model profiles.
- Streaming output is enabled by default.
- Thinking-capable chat models keep reasoning in a bounded collapsed Thinking
  panel and final text in Translation.
- Qwen-style thinking is usable; Nanbeige thinking is separated but low quality
  and should usually stay disabled.
- Changing sampling, streaming, or thinking mode does not reload the model.
- Changing model, backend, or context size still requires runtime reload.
- Matching source and target languages are valid rewrite/cleanup tasks.
- Leading model labels such as `Translation:` are stripped from final output.

Package notes:

- The archive does not include a GGUF model.
- The archive includes LoTraQ Windows, self-contained .NET runtime files, and
  pinned `llama.cpp` CPU/Vulkan runtimes.
- The archive is not code signed.
- The archive includes debug symbol `.pdb` files because this is still a
  preview build.

Known limits:

- No installer.
- No polished installer UX.
- In-app help/tooltips for model management, backend choice, context size,
  streaming, and thinking mode are deferred.
- CPU can be slow; Vulkan depends on local GPU and driver support.
