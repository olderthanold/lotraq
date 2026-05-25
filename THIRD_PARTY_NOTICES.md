# Third-party notices

LoTraQ uses local AI model and runtime components distributed under their own
upstream licenses. These upstream components are not owned by this repository.

## Android

- LoTraQ Android uses Google AI Edge LiteRT-LM runtime components.
- Android model downloads use upstream model files such as:
  - `litert-community/gemma-4-E2B-it-litert-lm`
  - `barakplasma/translategemma-4b-it-android-task-quantized`
  - `litert-community/gemma-4-E4B-it-litert-lm`
- Model files are downloaded separately and remain under their upstream model
  licenses and terms.

## Windows MVP

- The Windows MVP archive includes self-contained Microsoft .NET runtime files for
  the WPF app.
- The Windows MVP archive includes `.pdb` debug symbol files because it is an MVP
  build.
- The Windows MVP archive includes pinned `llama.cpp` Windows x64 CPU and Vulkan
  runtime binaries:
  - `llama.cpp` release: `b9305`
  - `llama.cpp` commit: `63248fc3e33e6f3b579dce6a743fd6ce8939af9c`
- The Windows MVP archive does not include a GGUF model.
- The suggested local Windows MVP model is `TranslateGemma 4B IT Q4_K_S GGUF`,
  sourced separately from `mradermacher/translategemma-4b-it-GGUF`.

Check the upstream projects and model pages for their current licenses,
acceptable-use terms, and attribution requirements.
