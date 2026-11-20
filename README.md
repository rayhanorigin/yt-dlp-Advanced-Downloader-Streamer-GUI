# yt-dlp Advanced Downloader & Streamer GUI

A feature-rich Windows desktop application built with Python and Tkinter that provides a graphical interface for [yt-dlp](https://github.com/yt-dlp/yt-dlp). Designed to make downloading, searching, streaming, and managing media easier without having to manually work with command-line arguments.

<p align="center">
  <img src="https://img.shields.io/badge/Version-3.6-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Platform-Windows-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Python-3.x-yellow?style=for-the-badge">
  <img src="https://img.shields.io/badge/Powered%20By-yt--dlp-red?style=for-the-badge">
</p>

---

## Overview

**yt-dlp Advanced Downloader & Streamer GUI** is a Windows application designed to simplify media downloading and streaming through a customizable graphical interface.

It provides advanced download controls, video search, queue management, batch processing, streaming playback, profiles, scheduling, filtering, and a wide range of yt-dlp configuration options — all accessible from a single application.

Whether you're downloading a single video, managing multiple downloads, searching for content, processing playlists, or streaming directly to a media player, the application provides a flexible workflow without requiring you to manually construct yt-dlp commands.

## Features

### 📥 Download Manager
- Download videos, audio, and other supported media.
- Batch download using multiple URLs.
- Download queue with add, remove, reorder, and undo operations.
- Queue persistence across application restarts.
- Pause, resume, and cancel active download jobs.
- Download progress and queue-level progress tracking.
- Custom output directory.
- Custom filename templates.
- Concurrent fragment downloading.
- Copy generated yt-dlp commands to the clipboard.
- Optional post-download actions.

### 🔍 Search Explorer
- Search for videos directly within the application.
- Browse search results without opening a browser.
- View video information and metadata.
- Add individual search results to the download queue.
- Add multiple or all search results to the queue.
- Stream selected search results directly.
- Fetch and inspect content from supported URLs.

### 🎬 Video & Audio Controls
- Select media type and quality.
- Configure video and audio formats.
- Choose preferred codecs.
- Customize container and file extensions.
- Configure audio quality and bitrate.
- Fetch available formats and qualities from individual URLs.
- Select subtitle languages.
- Download subtitles independently.
- Configure thumbnail downloading.
- Control format selection and media processing.

### 📡 Live Streaming & Playback
- Stream supported media directly to external players.
- Live-stream URLs without downloading the entire media file.
- Support for MPV and VLC playback.
- Select a preferred media player when multiple players are detected.

### ⚙️ Advanced Configuration
- Extensive yt-dlp configuration options.
- Download speed limits.
- Proxy configuration.
- Browser impersonation settings.
- Retry and delay controls.
- Network and connection settings.
- Download filters based on upload date, file size, duration, and other criteria.
- SponsorBlock configuration for supported YouTube content.
- Cookie configuration and browser cookie integration.
- Custom ffmpeg location.
- Configuration conflict detection.
- Filter testing before downloading.

### 👤 Profiles & Settings
- Save and load download configurations.
- Maintain multiple download profiles.
- Quickly switch between different download setups.
- Persistent application settings.
- Configuration management without manually editing command arguments.

### 🎨 Themes & Interface
- Multiple interface themes.
- Customizable appearance.
- Theme configuration and management.
- A dedicated Themes tab.
- Compact interface mode.
- Scrollable configuration areas for easier navigation.

### 📅 Scheduling
- Schedule recurring or predefined download jobs.
- Configure scheduled tasks using saved settings.
- Automate download operations.
- Manage scheduled jobs through the graphical interface.

### 📋 Logging & Diagnostics
- Execution logs.
- Download activity tracking.
- Error reporting and diagnostic information.
- Dependency and requirement checking.
- Logging of previously silent failures.
- Built-in update checking.
- Keyboard shortcuts for common operations.

---

## Screenshots
<img width="359" height="322" alt="image" src="https://github.com/user-attachments/assets/6d598114-b777-4874-b657-f837b2011081" />
<img width="359" height="322" alt="image" src="https://github.com/user-attachments/assets/9c3ddee1-1a2e-4bac-a7a2-91e6fb10dde2" />
<img width="359" height="322" alt="image" src="https://github.com/user-attachments/assets/a493ccef-33e5-4d57-8d8c-606f0688acb7" />
<img width="359" height="322" alt="image" src="https://github.com/user-attachments/assets/5f6d8eda-4076-4456-9ef3-dd92615ff950" />
<img width="359" height="322" alt="image" src="https://github.com/user-attachments/assets/eb1d4b3d-bee5-48b2-a0fe-10c864ee9b8a" />
<img width="359" height="322" alt="image" src="https://github.com/user-attachments/assets/3074f4b2-3403-4862-91f5-b70f48774415" />

<!-- Add screenshots here when available -->

---

## Requirements

The application is designed exclusively for **Windows**.

| Component | Requirement | Purpose |
|---|---|---|
| Python | Python 3.x | Runs the application |
| yt-dlp | Required | Media downloading, extraction, and streaming |
| ffmpeg | Recommended | Media processing, merging, conversion, and related operations |
| JavaScript Runtime | Recommended/required for certain extraction features | Supports yt-dlp JavaScript-dependent extraction |
| MPV | Optional | Media streaming and playback |
| VLC | Optional | Media streaming and playback |

Some features may require additional dependencies or specific versions of the components above.

The application includes a dependency checker to help identify missing or improperly configured components.

---

## 🚀 Installation

1. **Download the tool**
2. **Install the required tools**
   - [Download yt-dlp.exe](https://github.com/yt-dlp/yt-dlp/releases) and make sure it's on your PATH, or placed next to the script
   - [Download ffmpeg](https://ffmpeg.org/download.html) (Windows builds) and add it to your PATH
   - (Optional) Install [Node.js](https://nodejs.org/) for the JS runtime
   - (Optional) Install [mpv](https://mpv.io/) and/or [VLC](https://www.videolan.org/vlc/) for streaming

2. **Run the app**
```bash
   python yt-dlp.Advanced.Downloader.py
```

   Or grab a pre-built `.exe` from the [Releases page](https://github.com/rayhanorigin/yt-dlp-Advanced-Downloader-Streamer-GUI/releases), if available, to run it without installing Python.

---

## 🕹️ Usage

1. Paste a URL, load a batch `.txt` file, or search and queue videos from the **Search Explorer** tab.
2. Configure your desired media type, quality, codecs, and container in **Download & Stream**.
3. Fine-tune subtitles, SponsorBlock, cookies, retries, and other behavior in **Advanced Settings**.
4. Hit **START DOWNLOAD JOB** to download, or **STREAM LIVE IN PLAYER** to watch instantly without saving.
5. Save your setup as a **Profile**, or schedule it to run automatically from the **Profiles & Scheduler** tab.
6. Watch progress and full command output live in the **Full Execution Logs** tab.

Press **F1** inside the app at any time for the full keyboard shortcut reference.

---

## ⚙️ Configuration & Data

The app stores its configuration, profiles, scheduled jobs, search/URL history, and column layout in a config folder next to the executable/script, and migrates automatically from older legacy file locations when detected. Use the **History & Saved Logs Persistence Controls** section in Advanced Settings to clear search or URL history at any time.

---
## 🪡 Build Executable
### 1. Open CMD ###
### 2. Install Pyinstaller ###
```bash
pip install pyinstaller
```
### 3. Build EXE ###
```bash
pyinstaller --onefile --windowed --name "yt-dlp Advanced Downloader" --icon=icon.ico --add-data "icon.ico;." Downloader_Script.py
```
---

## 🙏 Credits

- [yt-dlp](https://github.com/yt-dlp/yt-dlp) — the download engine this GUI wraps
- [ffmpeg](https://ffmpeg.org/) — media processing and remuxing
- [Python](https://www.python.org/) & Tkinter — application framework
- [Node.js](https://nodejs.org/) (or other JS runtimes) — JS challenge solving support

---

## 👤 Author

**Rayhan Azad**
📧 knifeswifter57@gmail.com
🔗 [GitHub Repository](https://github.com/rayhanorigin/yt-dlp-Advanced-Downloader-Streamer-GUI)
