# Privacy

LoTraQ is a local translation app.

The app does not require an account. It does not collect personal data,
analytics, telemetry, source text, translations, history, prompts, language
choices, model choices, or usage statistics.

LoTraQ does not send your source text or translations to a remote server.
Translation runs locally after you download or import a model.

Android can connect to the configured model host when you ask it to download a
model. Current Android standard model downloads use Hugging Face-hosted files.
That download host may see normal network metadata such as your IP address,
user agent, and requested file URL.

Android Photo OCR processes images you select from local storage or capture
through the system camera on the device. OCR runs locally, either through Latin
ML Kit OCR or an installed Gemma OCR model. LoTraQ does not upload selected
images, captured images, or extracted OCR text. Camera captures are temporary
app-private cache files by default; they are not saved to gallery/storage unless
you explicitly use Save pic. Extracted text is handled like normal source text
and remains local unless you copy or share it outside LoTraQ.

Windows 1.2 can download the standard TranslateGemma GGUF model when you ask it
to, or reference an existing local GGUF file through `Add GGUF`. The model
download host may see normal network metadata such as your IP address, user
agent, and requested file URL. During translation Windows starts a bundled
`llama-server.exe` process bound to `127.0.0.1` and sends the rendered prompt
to that local process only. Other local processes on the same machine may be
able to connect to that localhost process while it is running.

LoTraQ may store local app data such as settings, translation history, model
paths, downloaded model files, cache, temporary files, and runtime logs on your
device or in the extracted Windows app folder. If the Windows folder is not
writable, the app uses `%LOCALAPPDATA%\LoTraQ`. This data is not uploaded by
LoTraQ.

After a model is installed or imported, normal translation does not need a
network connection.
