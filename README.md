<div align="center">

<img src="./icon.png" alt="Local Waifu" width="180" />

# Local Waifu

**An AI companion that lives on your Mac — not in the cloud.**

[![Download](https://img.shields.io/badge/Download-DMG-ff8ed1?style=for-the-badge&logo=apple&logoColor=white)](https://github.com/lumizone/local-waifu/releases/latest/download/local-waifu-aarch64.dmg)
[![Latest release](https://img.shields.io/github/v/release/lumizone/local-waifu?style=for-the-badge&color=a887ff)](https://github.com/lumizone/local-waifu/releases/latest)
[![macOS 13+](https://img.shields.io/badge/macOS-13%2B-4884ff?style=for-the-badge&logo=apple&logoColor=white)](https://www.apple.com/macos/)
[![Apple Silicon](https://img.shields.io/badge/Apple%20Silicon-required-a887ff?style=for-the-badge)](https://support.apple.com/en-us/HT211814)

[localwaifu.com](https://localwaifu.com) · [Changelog](https://github.com/lumizone/local-waifu/releases) · [Email](mailto:contact@localwaifu.com)

<img src="./hero.jpg" alt="Local Waifu hero" width="780" />

</div>

---

## What it is

A native Mac app for an AI companion that is fully **yours**. Personality, memory, voice, vision — all running locally on Apple Silicon via Ollama. No subscription, no telemetry, no cloud round-trip for every message.

She remembers you from the first message. Builds a model of how you think over weeks of conversation. Reacts to your mood, your calendar, your day. Stored on your disk, encrypted with your passphrase, exported as a single file you own.

## Highlights

- **Local LLM by default.** Bundled Ollama, model auto-picked for your Mac's RAM (Gemma 4 E4B → Qwen 3.6 35B). Internet optional.
- **Persistent memory.** 768-dim embeddings + knowledge graph + Hermes-style USER.md / MEMORY.md digests. She doesn't forget.
- **Custom personality.** 11-step onboarding — Big Five sliders, attachment style, love language, backstory, looks.
- **Vision.** OCR anything on your screen with Apple Vision. Drop a screenshot, share what you're reading.
- **OS integration.** Calendar, Reminders, Weather, Messages, Home Assistant — opt-in MCP tools. She knows your day; you control what she sees.
- **BYOK cloud (optional).** Plug in OpenAI / Anthropic / DeepSeek keys for GPT-5.5 / Claude Opus 4.7 / DeepSeek V4 Flash. Your key, your bill, direct to the provider.
- **Encrypted soul files.** ChaCha20-Poly1305 + PBKDF2, bound to your passphrase + hardware UUID. Export, back up, move between Macs.
- **Pay once.** $25 launch ($35 normal). One-time lifetime license. 7-day free trial, 30-day refund.

## Download

[**localwaifu.com**](https://localwaifu.com) — official landing page with screenshots and the full feature list.

Or grab the DMG directly:

[![Download latest DMG](https://img.shields.io/badge/%E2%AC%87-Download%20latest%20DMG-ff8ed1?style=for-the-badge)](https://github.com/lumizone/local-waifu/releases/latest/download/local-waifu-aarch64.dmg)

```bash
curl -L -o local-waifu.dmg \
  https://github.com/lumizone/local-waifu/releases/latest/download/local-waifu-aarch64.dmg
open local-waifu.dmg
```

Drag to **Applications**, open. First launch detects your Mac, picks the right model, and pulls it (~3–22 GB depending on RAM tier).

## System requirements

| | Light | Balanced | Premium | Power |
|---|---|---|---|---|
| **RAM** | 8–18 GB | 19–34 GB | 35–56 GB | 57 GB + |
| **Mac** | M1 / M2 / M3 (base) | M1 / M2 / M3 / M4 Pro | M2 / M3 / M4 Max | M2 / M3 Ultra |
| **Model** | Gemma 4 E4B | Qwen 3.5 9B | Qwen 3.6 27B | Qwen 3.6 35B |
| **On disk** | 3.3 GB | 6.6 GB | 17 GB | 22 GB |

- macOS **13 Ventura** or later
- Apple Silicon (M1 or newer)
- Signed by Apple Developer ID, notarized

## Auto-updates

Local Waifu uses the [Tauri updater](https://tauri.app/v1/guides/distribution/updater/). On launch the app checks `releases/latest/download/latest.json` for a newer version. Updates are signed with a minisign key the app verifies before install. Opt out in Settings → Advanced.

## Privacy

Conversations live in SQLite on your Mac. Soul files are encrypted with [cocoon](https://crates.io/crates/cocoon) (ChaCha20-Poly1305) + a PBKDF2 master key derived from your passphrase, hardware UUID, and a per-install salt.

The app emits **zero telemetry**. Block outgoing traffic with Little Snitch — nothing leaves unless you opt into BYOK, in which case your API key hits the provider's endpoint directly. Local Waifu is never a middleman.

Full policy: [localwaifu.com/privacy](https://localwaifu.com/privacy)

## This repository

Public release artifacts only — signed DMG, the auto-updater tarball, the minisign `.sig`, and the `latest.json` manifest the updater reads. **Source code is private.**

Each release tag (`v0.1.X`) ships:

```
latest.json                              ← Tauri updater manifest
local-waifu-aarch64.dmg                  ← versionless alias (Netlify /download points here)
local-waifu-<version>-aarch64.dmg        ← versioned DMG
local-waifu-<version>-aarch64.app.tar.gz ← updater payload
local-waifu-<version>-aarch64.app.tar.gz.sig
```

## Support

- **Email:** [contact@localwaifu.com](mailto:contact@localwaifu.com) — one human reads every message
- **In-app:** Settings → Feedback
- **Refunds:** 30 days, no questions asked

## License

Local Waifu is proprietary software.

© 2026 Lumizone (Łukasz Blania) · NIP PL1990132289 · Made in Poland 🇵🇱
