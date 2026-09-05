# yt-dlp Advanced Downloader & Streamer GUI

A feature-packed Windows desktop GUI for [yt-dlp](https://github.com/yt-dlp/yt-dlp), built with Python and Tkinter. It wraps the yt-dlp command line into a full application: search, queue, download, live-stream to your media player, schedule recurring jobs, and manage everything through profiles — all without touching a terminal.

![Version](https://img.shields.io/badge/version-2.4-544BD2)
![Platform](https://img.shields.io/badge/platform-Windows-0078D6)
![Python](https://img.shields.io/badge/python-3.x-blue)

> **Disclaimer:** This open-source tool is built strictly for personal use. The developer is not responsible for any illegal use.

---

## ✨ Features

### 🎯 Download & Streaming
- **Three input modes:** single URL/playlist, a batch `.txt` file of links, or a queue built from search results
- **Drag & drop** support for URLs and batch files directly onto the input field (via `tkinterdnd2`, optional)
- **Live streaming** straight into **MPV** or **VLC** — auto-detects installed players and lets you choose when both are present, no download required
- **Pause / Resume / Cancel** controls for active jobs
- **"Copy as yt-dlp Command"** — generates and copies the exact equivalent command-line invocation for any configuration
- Resume interrupted downloads (`--continue`), configurable retries, and delay-between-downloads (including random ranges like `2-5`)
- Speed limiting and full proxy support
- Auto-open the destination folder when a job finishes
- Smart completion detection that distinguishes real errors from "already downloaded" / warning-only exits

### 🔍 Search Explorer
- Built-in YouTube search (`ytsearch`) with a configurable result limit
- Thumbnail Support
- Suggestions Support
- Sortable, resizable results table with persistent column widths
- Fetch metadata/contents directly from a pasted link (no search needed)
- Add selected or all results to a manageable **download queue** (reorder, remove, clear)
- Search and URL history with quick recall, and one-click history clearing

### 🎛️ Format & Quality Control
- Media type selector: **video**, **audio**, **thumbnail only**, or **subtitles only**
- Quality target and container/extension pickers tailored to the selected media type
- Independent **video codec** (H.264, H.265/HEVC, AV1, VP9, VP8) and **audio codec** (AAC, MP3, Opus, Vorbis, FLAC, AC3, EAC3) re-encode selection
- Fine-grained audio track quality control (up to "None" for video-only output)
- Automatic `--format-sort` construction based on your selections
- Conflict detection that warns you before running a job with contradictory settings

### 📝 Subtitles, Metadata & Extras
- Subtitle modes: none, or "smart" (prefers manual subs, falls back to auto-generated), with multi-language codes (`en,es,fr`)
- Embed thumbnails into the output file
- Save raw description metadata, write `info.json`/NFO sidecar files
- Chapter splitting, comment downloading, and live chat download (YouTube)
- **SponsorBlock** integration — remove or mark sponsor/self-promo/intro/outro/filler segments by category, or use `all`
- Cookie support: load a `cookies.txt` profile or pull cookies directly from your browser (Chrome, Firefox, Edge, Brave, Opera, etc.)
- Configurable JS runtime (node / quickjs / deno) for sites requiring JS challenge solving
- Free-text field to append any extra raw yt-dlp arguments to the final command

### 🗂️ Profiles & Scheduler
- Save your entire configuration as a named **profile** and reload it instantly; mark one as default
- **Scheduled jobs** tab: create recurring or one-off download jobs with their own target, output folder, and playlist options
- Batch execution: multiple due jobs run back-to-back with a single combined summary popup instead of spamming notifications
- **Run at Windows startup** support, plus an option to run pending jobs immediately when the app launches
- Manually trigger, edit, enable/disable, or delete any scheduled job

### 🖥️ Interface & Quality of Life
- **Dark mode** toggle applied across the entire interface
- Full keyboard shortcut set (start job, stream, pause/resume, search focus, URL focus, select all, copy, clear queue, reorder queue, and more — see in-app **F1** help)
- Scrollable, resizable tabs that stay usable at any window size
- Right-click context menu, live execution log console (with in-place progress line updates), and a persistent status bar
- Built-in **Requirements Checker** that verifies yt-dlp, ffmpeg, Python, and JS runtime availability across PATH, the app folder, and the Windows registry
- **Self-update checker** — checks GitHub Releases for newer app versions (separate from yt-dlp's own `-U` updater) with optional automatic check on startup
- Config, profiles, history, and column layout all persist between sessions, with automatic migration from legacy config file locations
- The console window is automatically hidden on launch for a clean, GUI-only experience

---

## 📋 Requirements

- **Windows 10 or later** (this app is Windows-only)
- [Python 3](https://www.python.org/) — to run from source (EXE version doesn't need python to be installed)
- [yt-dlp](https://github.com/yt-dlp/yt-dlp) — the core download engine
- [ffmpeg](https://ffmpeg.org/) — required for merging, re-encoding, thumbnail embedding, chapter splitting
- A JavaScript runtime such as [Node.js](https://nodejs.org/) — recommended, used by yt-dlp for some sites' JS challenges
- [mpv](https://mpv.io/) or [VLC](https://www.videolan.org/vlc/) — optional, only needed for the live-streaming feature

Use the in-app **🔍 Check Requirements** button (Advanced Settings tab) at any time to verify what's detected on your system.

---

## 🚀 Installation

1. **Clone the repository**
```bash
   git clone https://github.com/rayhanorigin/yt-dlp-Advanced-Downloader-Streamer-GUI.git
   cd yt-dlp-Advanced-Downloader-Streamer-GUI
```

2. **Install Python dependencies**
```bash
   pip install tkinterdnd2
```

3. **Install the required tools**
   - [Download yt-dlp.exe](https://github.com/yt-dlp/yt-dlp/releases) and make sure it's on your PATH, or placed next to the script
   - [Download ffmpeg](https://ffmpeg.org/download.html) (Windows builds) and add it to your PATH
   - (Optional) Install [Node.js](https://nodejs.org/) for the JS runtime
   - (Optional) Install [mpv](https://mpv.io/) and/or [VLC](https://www.videolan.org/vlc/) for streaming

4. **Run the app**
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
pyinstaller --onefile --windowed --name "yt-dlp Advanced Downloader" --icon=icon.ico yt-dlp.Advanced.Downloader.py --onefile
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
