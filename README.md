# yt-dlp Advanced Downloader & Streamer GUI

A feature-packed Windows desktop GUI for [yt-dlp](https://github.com/yt-dlp/yt-dlp), built with Python and Tkinter. It wraps the yt-dlp command line into a full application: search, queue, download, live-stream to your media player, schedule recurring jobs, and manage everything through profiles — all without touching a terminal.

![Version](https://img.shields.io/badge/version-3.0-544BD2)
![Platform](https://img.shields.io/badge/platform-Windows-0078D6)
![Python](https://img.shields.io/badge/python-3.x-blue)

> **Disclaimer:** This open-source tool is built strictly for personal use. The developer is not responsible for any illegal use.

---
## Screenshots
<img width="522" height="422" alt="image" src="https://github.com/user-attachments/assets/e65e3323-e796-431f-a60f-9191d712b380" />
<img width="522" height="422" alt="image" src="https://github.com/user-attachments/assets/84d711d9-908b-438a-86c1-4e987edf77fc" />
<img width="522" height="422" alt="image" src="https://github.com/user-attachments/assets/0df96253-c21a-4a66-beb7-094ddfc6358c" />
<img width="522" height="422" alt="image" src="https://github.com/user-attachments/assets/75a0fbc2-2c40-49d7-95bc-19e01d42345b" />
<img width="522" height="422" alt="image" src="https://github.com/user-attachments/assets/8c65b160-c82e-47b2-a99a-321b9b928b82" />
<img width="522" height="422" alt="image" src="https://github.com/user-attachments/assets/91cfd148-8116-4e81-b7ad-499da439472b" />


## ✨ Features

### 🎬 Advanced Downloads
- Download videos, audio, thumbnails, or subtitles.
- Select video and audio quality, codecs, and containers.
- Support for custom yt-dlp arguments.
- Browser cookies and cookies-file support.
- Subtitle and thumbnail configuration.
- SponsorBlock and other advanced yt-dlp options.
- Retry, delay, speed-limit, and concurrent-fragment controls.
- Pause and resume downloads.

### 🔎 Search Explorer
- Search supported websites directly through yt-dlp.
- Browse search results inside the application.
- View available thumbnails when supported.
- Queue selected search results for downloading.
- Stream selected results directly through a supported media player.

### 📥 Download Queue
- Add multiple URLs or media items to a queue.
- Process batch downloads in the background.
- Remove, reorder, or clear queued items.
- Handle download results and errors without blocking the interface.

### ▶️ Media Streaming
- Stream supported media directly through **MPV** or **VLC**.
- Automatically detect available players.
- Stream individual URLs or selected search results.
- Supports the same cookie options used for downloading.

### 👤 Profiles & Scheduler
- Save frequently used download configurations as profiles.
- Set a default profile that loads automatically.
- Duplicate, update, import, and export profiles.
- Schedule downloads to run once, daily, weekly, or at application startup.
- Run, duplicate, enable, disable, or delete scheduled jobs.

### 🎨 Themes
- Customize the application's appearance.
- Built-in theme presets.
- Create and save custom themes.
- Import, export, duplicate, and delete themes.
- Theme configurations are stored separately for easy management.

### ⚙️ Advanced Settings
Provides detailed control over yt-dlp and application behavior, including:
- Video and audio formats
- Codecs and containers
- Subtitles
- Cookies
- SponsorBlock
- JavaScript runtime
- Comments and live chat
- Chapters and metadata
- Thumbnail embedding
- Retries and delays
- Concurrent fragments
- Custom yt-dlp arguments

### 📋 Execution Logs
A dedicated execution log tab with Custom command box provides access and visibility into application and yt-dlp activity.

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
