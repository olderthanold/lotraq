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

Windows MVP does not include model download. You import a local GGUF model file.
During translation it starts a bundled `llama-server.exe` process bound to
`127.0.0.1` and sends the rendered prompt to that local process only. Other
local processes on the same machine may be able to connect to that localhost
process while it is running.

LoTraQ may store local app data such as settings, translation history, model
paths, cache, temporary files, and runtime logs on your device or in the
extracted Windows app folder. If the Windows folder is not writable, the app
uses `%LOCALAPPDATA%\LoTraQ`. This data is not uploaded by LoTraQ.

After a model is installed or imported, normal translation does not need a
network connection.
