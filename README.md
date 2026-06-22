<div align="center">

<img src="assets/velqi.png" width="110" alt="Velqi Logo"/>

# Velqi — Free Music Streaming

**Stream YouTube Music with no ads, no login, and no limits.**

[![Release](https://img.shields.io/github/v/release/dieegoleo/Velqi-Music-App?color=7C3AED&label=Latest%20Release&style=for-the-badge)](https://github.com/dieegoleo/Velqi-Music-App/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/dieegoleo/Velqi-Music-App/total?color=22c55e&style=for-the-badge)](https://github.com/dieegoleo/Velqi-Music-App/releases/latest)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue?style=for-the-badge)](https://www.gnu.org/licenses/gpl-3.0)
[![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://github.com/dieegoleo/Velqi-Music-App/releases/latest)

---

### Download

<a href="https://github.com/dieegoleo/Velqi-Music-App/releases/download/v1.0.0/Velqi-arm64.apk">
  <img src="https://img.shields.io/badge/Download-arm64%20%E2%80%94%20Modern%20Phones-7C3AED?style=for-the-badge&logo=android&logoColor=white" alt="Download arm64"/>
</a>

<a href="https://github.com/dieegoleo/Velqi-Music-App/releases/download/v1.0.0/Velqi-armeabi-v7a.apk">
  <img src="https://img.shields.io/badge/Download-armeabi--v7a%20%E2%80%94%20Older%20Phones-6D28D9?style=for-the-badge&logo=android&logoColor=white" alt="Download armeabi-v7a"/>
</a>

<a href="https://github.com/dieegoleo/Velqi-Music-App/releases/download/v1.0.0/Velqi-x86_64.apk">
  <img src="https://img.shields.io/badge/Download-x86__64%20%E2%80%94%20Emulators-4C1D95?style=for-the-badge&logo=android&logoColor=white" alt="Download x86_64"/>
</a>

> **Not sure which to pick?** Download **arm64** — it works on virtually all modern Android phones (2018+).

</div>

---

## Features

- 🎵 **Ad-free streaming** — No interruptions, ever.
- 🔓 **No login required** — Open and listen immediately.
- 💾 **Smart caching** — Songs buffer automatically for smooth playback.
- 📥 **Offline downloads** — Save tracks and listen without internet.
- 🎤 **Synced lyrics** — Word-by-word animated lyrics (LRCLIB) + plain text.
- 🎨 **Dynamic Material You** — UI adapts its colors to the album art.
- 🎚️ **Built-in equalizer** — Full hardware EQ support.
- 🔀 **Crossfade** — Smooth transitions between tracks.
- 📻 **Radio / Queue** — Auto-generated queues from any song, album, or artist.
- 🔔 **Background playback** — Notification controls + lock screen integration.
- 🧭 **Flexible navigation** — Bottom Bar or Side Navigation Bar.
- 😴 **Sleep timer** — Stops playback after a set duration.
- ⏩ **Silence skipping** — Automatically skips silent gaps.
- 📚 **Library management** — Playlists, bookmarks, artists, albums.
- 🔗 **Import from YouTube** — Share any YouTube / YT Music link into Velqi.
- ⚙️ **Streaming quality control** — Choose your audio bitrate.
- 🍪 **YouTube cookies** — Use your own cookies for restricted content.

---

## Architecture

Velqi runs a local Python microservice inside the app process — no external servers, no cloud dependency.

```
Flutter UI  ←— HTTP (localhost) —→  Python Backend
                                        ├── yt-dlp      → audio stream resolution
                                        └── ytmusicapi  → search, browse, metadata
```

This design keeps the UI thread always fast and responsive. Heavy decryption and networking happen in the Python layer, isolated from rendering.

---

## Installation

1. Go to [**Releases**](https://github.com/dieegoleo/Velqi-Music-App/releases/latest)
2. Download the APK for your device:

| APK | Device |
|-----|--------|
| `Velqi-arm64.apk` | Modern phones — **recommended** (2018+) |
| `Velqi-armeabi-v7a.apk` | Older 32-bit phones |
| `Velqi-x86_64.apk` | Emulators (BlueStacks, etc.) |

3. Allow installation from unknown sources in your Android settings
4. Install the APK and open Velqi

---

## Troubleshooting

**Playback stops when the screen turns off:**
Go to your device's battery settings and set Velqi to **Unrestricted**, or enable **Ignore Battery Optimizations** inside the app settings.

**Long loading screen on first launch:**
Normal — the embedded audio engine initialises on first run (~15–30s depending on device). Subsequent launches are near-instant.

**Content not loading:**
Check your internet connection. For region-restricted content, add YouTube cookies via **Settings → Advanced → YouTube Cookies**.

---

## License

Velqi is free software licensed under the **GNU GPL v3.0**.

- Modified versions must remain free and open-source.
- Cannot be published on closed-source stores (Google Play, App Store, etc.).
- Cannot be used commercially without explicit permission.

---

## Disclaimer

This project is developed for educational purposes and is not affiliated with, sponsored by, or endorsed by YouTube or Google. All media content accessed through this application belongs to its respective rights holders. The software is provided "as-is", without warranty of any kind.
