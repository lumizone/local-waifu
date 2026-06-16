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

A native **macOS and Windows** app for an AI companion that is fully **yours**. Personality, memory, voice, vision — all running locally via Ollama. No subscription, no telemetry, no cloud round-trip for every message.

She remembers you from the first message. Builds a model of how you think over weeks of conversation. Reacts to your mood, your calendar, your day. Stored on your disk, encrypted with your passphrase, exported as a single file you own.

## Highlights

- **Local LLM by default.** Bundled Ollama, model auto-picked for your machine's RAM (Gemma 4 E4B → Qwen 3.6 35B). Internet optional.
- **Persistent memory.** 768-dim embeddings + knowledge graph + Hermes-style USER.md / MEMORY.md digests. She doesn't forget.
- **Custom personality.** 11-step onboarding — Big Five sliders, attachment style, love language, backstory, looks.
- **Vision.** OCR anything on your screen with Apple Vision. Drop a screenshot, share what you're reading.
- **OS integration.** Calendar, Reminders, Weather, Messages, Home Assistant — opt-in MCP tools. She knows your day; you control what she sees.
- **BYOK cloud (optional).** Plug in OpenAI / Anthropic / DeepSeek keys for GPT-5.5 / Claude Opus 4.7 / DeepSeek V4 Flash. Your key, your bill, direct to the provider.
- **Encrypted soul files.** ChaCha20-Poly1305 + PBKDF2, bound to your passphrase + hardware UUID. Export, back up, move between devices.
- **Pay once.** $25 launch ($35 normal). One-time lifetime license. 7-day free trial, 30-day refund.

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

© 2026 Lumizone (Łukasz Blania) · NIP PL1990132289 · Made in Poland 🇵🇱
