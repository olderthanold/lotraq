# Third-party notices

LoTraQ uses local AI model and runtime components distributed under their own
upstream licenses. These upstream components are not owned by this repository.

## Android

- LoTraQ Android uses Google AI Edge LiteRT-LM runtime components.
- Android Photo OCR uses Google ML Kit Text Recognition
  (`com.google.mlkit:text-recognition`) for selected local images.
- Android 1.5 Model OCR uses installed Gemma 4 E2B/E4B LiteRT-LM models through
  Google AI Edge LiteRT-LM image input.
- Android Photo OCR camera capture uses AndroidX Core `FileProvider` for
  app-private temporary camera image files.
- Android model downloads use upstream model files such as:
  - `litert-community/gemma-4-E2B-it-litert-lm`
  - `barakplasma/translategemma-4b-it-android-task-quantized`
  - `litert-community/gemma-4-E4B-it-litert-lm`
- Model files are downloaded separately and remain under their upstream model
  licenses and terms.

## Windows 1.2

- The Windows 1.2 archive includes self-contained Microsoft .NET runtime files for
  the WPF app.
- The Windows 1.2 archive includes `.pdb` debug symbol files because it is still
  a preview build.
- The Windows 1.2 archive includes pinned `llama.cpp` Windows x64 CPU and Vulkan
  runtime binaries:
  - `llama.cpp` release: `b9305`
  - `llama.cpp` commit: `63248fc3e33e6f3b579dce6a743fd6ce8939af9c`
- The Windows 1.2 archive does not include a GGUF model.
- Windows 1.2 can download or reference `TranslateGemma 4B IT Q4_K_S GGUF`,
  sourced separately from `mradermacher/translategemma-4b-it-GGUF`.

Check the upstream projects and model pages for their current licenses,
acceptable-use terms, and attribution requirements.
