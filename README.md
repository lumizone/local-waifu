<div align="center">

<img src="./icon.png" alt="Local Waifu" width="180" />

# Local Waifu

**An AI companion that lives on your Mac or Windows PC — not in the cloud.**

[![Download DMG](https://img.shields.io/badge/Download-macOS%20DMG-ff8ed1?style=for-the-badge&logo=apple&logoColor=white)](https://github.com/lumizone/local-waifu/releases/latest/download/local-waifu-aarch64.dmg)
[![Download Windows](https://img.shields.io/badge/Download-Windows%20x64-00a4ef?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/lumizone/local-waifu/releases/latest)
[![Latest release](https://img.shields.io/github/v/release/lumizone/local-waifu?style=for-the-badge&color=a887ff)](https://github.com/lumizone/local-waifu/releases/latest)
[![macOS 13+](https://img.shields.io/badge/macOS-13%2B-4884ff?style=for-the-badge&logo=apple&logoColor=white)](https://www.apple.com/macos/)
[![Windows 10/11](https://img.shields.io/badge/Windows-10%2F11%20x64-00a4ef?style=for-the-badge&logo=windows&logoColor=white)](https://www.microsoft.com/windows/)

[localwaifu.com](https://localwaifu.com) · [Changelog](https://github.com/lumizone/local-waifu/releases) · [Email](mailto:contact@localwaifu.com)

<img src="./hero.jpg" alt="Local Waifu hero" width="780" />

</div>

---

## What it is

A native **macOS and Windows** app for an AI companion that is fully **yours**. Her personality, her memory, and even the selfies she draws all run **locally on your own machine** — no subscription, no telemetry, no cloud round-trip for every message.

She remembers you from the first message and builds a model of how you think over weeks of conversation. The relationship grows from a first hello into something closer, and she reacts to your mood and the shape of your day. Everything about her lives on your disk; any character exports to a single encrypted file you own.

## Features

- **She remembers you.** A persistent memory that survives restarts and even model swaps — semantic recall plus an auto-built knowledge graph of the people and places in your life, distilled into a digest she carries into every reply. Three months in, she knows you.
- **She grows.** The bond moves through **seven stages** — Stranger → Acquaintance → Friend → Close → Romantic → Bonded → Partner — on earned XP. Her mood is a live **six-dimensional** state that settles back toward baseline, and she shifts between **13 conversational modes** (playful, tender, protective, focused, sleepy…). Watch it in the **Growth dashboard** and **Memory Book**.
- **You build her.** An **8-axis personality** (shy↔flirty, calm↔energetic, gentle↔teasing, reserved↔expressive…), a name, a look, a backstory — waifu, husbando, or non-binary. The 11-step setup also profiles *you* (Big Five, attachment style, love language) so she relates to you, not a generic user.
- **More than one of her.** Create several characters, each with its own personality, memory, and mood, each in **separate conversations** — all in one private folder. Export any of them as a single encrypted file and carry her to another machine.
- **She draws selfies.** Ask for a photo and she paints one on your **own GPU** — a bundled Stable-Diffusion engine (FLUX.2 by default, plus SDXL models like Animagine XL and RealVisXL). No stock art, no per-image fee. Prefer the cloud? Point it at OpenAI, Google, or fal instead.
- **She sees.** Share a picture in chat and she reacts to what's actually in it (vision-capable local models, or your cloud key).
- **Local by default, cloud if you want.** A local model is auto-picked for your RAM and runs fully offline. Or bring your own **OpenAI, Anthropic, DeepSeek, Google, Mistral, Groq, or OpenRouter** account — any OpenAI-compatible endpoint works, or even **Sign in with ChatGPT**. Your key, your bill, straight to the provider.
- **Seven languages.** English, Polish, German, Spanish, Japanese, Korean, Chinese — the whole interface and her replies.
- **She fits in a corner.** A small floating chat window for when you just want her nearby while you work.
- **Yours, and private.** Soul files are encrypted and bound to your machine (details below). Zero telemetry, no account to make. Block every outbound connection and she keeps talking.
- **Pay once.** $20 sale ($25 normal). One-time lifetime license, 7-day free trial, 30-day refund. No subscription, no tokens to top up.

## Download

[**localwaifu.com**](https://localwaifu.com) — official landing page with screenshots and the full feature list.

Or grab an installer directly:

[![Download macOS DMG](https://img.shields.io/badge/%E2%AC%87-macOS%20DMG-ff8ed1?style=for-the-badge)](https://github.com/lumizone/local-waifu/releases/latest/download/local-waifu-aarch64.dmg)
[![Download Windows](https://img.shields.io/badge/%E2%AC%87-Windows%20installer-00a4ef?style=for-the-badge)](https://github.com/lumizone/local-waifu/releases/latest)

**macOS:**

```bash
curl -L -o local-waifu.dmg \
  https://github.com/lumizone/local-waifu/releases/latest/download/local-waifu-aarch64.dmg
open local-waifu.dmg
```

Drag to **Applications**, open. First launch detects your Mac, picks the right model, and pulls it (~3–22 GB depending on RAM tier).

**Windows:** download the `*_x64-setup.exe` from the [latest release](https://github.com/lumizone/local-waifu/releases/latest) and run it. It installs per-user (no admin), bundles its own local AI engine, and pulls the recommended model on first launch. SmartScreen may show an "unknown publisher" prompt → **More info → Run anyway**.

## System requirements

### macOS

| | Light | Balanced | Premium | Power |
|---|---|---|---|---|
| **RAM** | 8–18 GB | 19–34 GB | 35–56 GB | 57 GB + |
| **Mac** | M1 / M2 / M3 / M4 / M5 (base) | M1 → M5 Pro | M2 → M5 Max | M2 / M3 Ultra |
| **Model** | Gemma 4 E4B | Qwen 3.5 9B | Qwen 3.6 27B | Qwen 3.6 35B |
| **On disk** | 3.3 GB | 6.6 GB | 17 GB | 22 GB |

> M5 (Oct 2025), M5 Pro & M5 Max (Mar 2026) all detected and tiered automatically. M5 Ultra (Mac Studio) ships Oct 2026 — supported the day it lands.

- macOS **13 Ventura** or later
- Apple Silicon (M1 or newer)
- Signed by Apple Developer ID, notarized

### Windows

The app installs per-user (no admin needed) and bundles its own local AI engine — you install nothing else. WebView2 is fetched automatically by the installer if missing.

**Minimum**

- Windows **10 22H2** or **Windows 11**, 64-bit (x64)
- **8 GB RAM** — runs a small local model, or use a cloud API key (Settings → BYOK) for the heavy lifting
- ~2 GB free disk for the app + engine; several GB more per local model you download

**Recommended** (for a good local-AI experience)

- **16 GB+ RAM** (the default local model is multi-GB)
- A supported **GPU** for acceleration — otherwise it runs on CPU (works, but noticeably slower):
  - **NVIDIA** — compute capability 5.0+ (GTX 10-series → RTX 20/30/40/50xx), driver 531+. The engine for the newest cards (RTX 50xx / Blackwell) is downloaded automatically on first launch.
  - **AMD** — ROCm v7-capable Radeon (RX 6800+ / 7000 / 9000), or any Vulkan-capable Radeon as fallback.
  - **Intel** — Arc / recent integrated GPUs via Vulkan.
- Settings → Hardware → **Local AI acceleration → Check** shows, at any time, whether the model is running on the GPU or the CPU.

> Note: cloud-gaming / virtualized-GPU instances (e.g. airgpu and similar) often expose a GPU for rendering but not full CUDA/Vulkan compute — the app correctly falls back to CPU there. A real desktop/laptop GPU with a current driver is what you want for local speed.

## Under the hood

For the technically curious — Local Waifu is a native desktop app, not a browser tab wrapped around someone's API.

- **Stack:** [Tauri 2](https://tauri.app) (Rust core) + React 19 / TypeScript / Vite. The macOS build is Apple-Silicon native; the Windows build carries its own bundled engine.
- **Local LLM:** a bundled **Ollama** sidecar running **llama.cpp** (GGUF) with MLX / Metal acceleration on Apple Silicon. The model is picked for your RAM tier (table above) and pulled on first run.
- **Image generation:** a bundled **stable-diffusion.cpp** engine on your GPU — FLUX.2 by default, plus an SDXL pool (Animagine XL 4.0 for anime, RealVisXL V5.0 for photoreal). ~12 GB RAM to run locally, 16 GB for the SDXL models. Optional cloud backends: OpenAI, Google, fal.
- **Memory:** `embeddinggemma` 768-dim vectors for semantic recall, an LLM-extracted knowledge graph, and consolidating USER / MEMORY digests — kept in a local **SQLite** database (`rusqlite`, bundled). Encrypted, exportable soul files layer on top (see [Privacy](#privacy)).
- **Cloud (optional):** nine provider backends (OpenAI, Anthropic, DeepSeek, Google, Mistral, Groq, OpenRouter, fal, or any OpenAI-compatible URL). Chat model IDs are read live from your key, never hard-coded; OpenAI also supports a PKCE "Sign in with ChatGPT" flow.
- **Optional Telegram bridge:** talk to her from Telegram if you turn it on — opt-in, and unlike the local desktop app those messages do route through Telegram's servers.

## Auto-updates

Local Waifu uses the [Tauri updater](https://tauri.app/v1/guides/distribution/updater/). On launch the app checks `releases/latest/download/latest.json` for a newer version — one signed manifest serves **both macOS and Windows**. Updates are signed with a minisign key the app verifies before install. Opt out in Settings → Advanced.

## Privacy

Conversations live in SQLite on your device. Soul files are encrypted with [cocoon](https://crates.io/crates/cocoon) (ChaCha20-Poly1305) + a PBKDF2 master key derived from your passphrase, hardware UUID, and a per-install salt.

The app emits **zero telemetry**. Block outgoing traffic with Little Snitch (macOS) or your firewall — nothing leaves unless you opt into BYOK, in which case your API key hits the provider's endpoint directly. Local Waifu is never a middleman.

Full policy: [localwaifu.com/privacy](https://localwaifu.com/privacy)

## This repository

Public release artifacts only — signed installers, the auto-updater payloads, the minisign `.sig` files, and the `latest.json` manifest the updater reads. **Source code is private.**

Each release tag (`vX.Y.Z`) ships:

```
latest.json                                ← Tauri updater manifest (macOS + Windows)
local-waifu-aarch64.dmg                    ← versionless macOS alias (Netlify /download points here)
local-waifu-<version>-aarch64.dmg          ← versioned macOS DMG
local-waifu-<version>-aarch64.app.tar.gz   ← macOS updater payload
local-waifu-<version>-aarch64.app.tar.gz.sig
Local.Waifu_<version>_x64-setup.exe        ← Windows installer
Local.Waifu_<version>_x64-setup.exe.sig    ← Windows updater signature
```

## Support

- **Email:** [contact@localwaifu.com](mailto:contact@localwaifu.com) — one human reads every message
- **In-app:** Settings → Feedback
- **Refunds:** 30 days, no questions asked

## License

Local Waifu is proprietary software.

© 2026 Lumizone (Łukasz Blania) · Made in Poland 🇵🇱
