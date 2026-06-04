# 🎬 yt-dlp Advanced Downloader & Streamer

An advanced, feature-rich, and easy-to-use Windows desktop application built with Python (`tkinter`) to make video downloading and live-streaming effortless. 

This tool serves as a powerful graphical interface (GUI) wrapper for **yt-dlp**, allowing you to bypass complicated command-line setups. Search for videos, watch live streams in your favorite player, configure subtitles, and download content in high quality—all with a few simple clicks!

---
## 🖼 Screenshots
<img width="702" height="712" alt="image" src="https://github.com/user-attachments/assets/eff0b3a2-5c36-4366-b727-88542c8700f6" />
<img width="702" height="712" alt="image" src="https://github.com/user-attachments/assets/d10b5bbd-8f32-4d45-85ce-88a25248030a" />
<img width="702" height="712" alt="image" src="https://github.com/user-attachments/assets/bee63302-38ae-4b87-ba89-c3f8e11c40db" />
<img width="702" height="712" alt="image" src="https://github.com/user-attachments/assets/e86db291-a8ad-475f-affc-51c5362a8878" />
---

## ✨ Features

* **📺 Seamless Live Streaming:** Stream individual videos or playlist items directly into **MPV** or **VLC Media Player** without downloading them first.
* **🔍 Built-in Search Explorer:** Look up videos directly inside the app using keywords. Scrape titles, channel links, and URLs without opening a web browser.
* **📦 Advanced Selection Queue:** Send your searched results straight into the main downloader loop.
* **📋 Intelligent Channel/Playlist Controls:** Found a Channeel/Playlist with 6969 videos? No worries! The app lets you read the list and choose exactly which index numbers you want to download or stream.
* **🛠️ Pro Configurations Made Simple:** Automatic resolution selection (from 144p baseline up to 8K Ultra-HD).
    * Separate Video + Audio extraction or Audio-only mode (MP3, M4A, WAV, OPUS).
    * Embedded thumbnails, subtitles (manual or auto-generated), and chapter markers.
    * Browser cookies integration to easily bypass format restrictions or age-gated blocks.
* **🚀 Built for Modern Web:** Integrated JavaScript Runtime support (`node`) enabled by default to smoothly execute modern extraction scripts.
* **🧾 Real-time Logging Console:** Watch the raw download speed, ETA percentage, and background steps unfold live.
* **🌃 Dark-Mode :** Ensuring Eye-comfort!
* **⏯ Resume ability:** For flexible download session.
* **🏭 Advanced Download Queue Management:** Downloading Multiple videos/playlists is as easy as being unemployed!
---

## 🛠️ Pre-Requirements (Important)

To run this tool smoothly on Windows, you need three core helper components installed on your computer. Don't worry—they are simple to set up!

1.  **Python 3.x:** [Download Python](https://www.python.org/downloads/) (Make sure to check the box that says **"Add Python to PATH"** during installation).
2.  **FFmpeg:** Required for merging high-quality audio and video tracks together. [Download ffmpeg](https://ffmpeg.org/download.html).
    * *Tip:* You can place `ffmpeg.exe` and `ffprobe.exe` directly into the script's folder, or add them to your Windows System PATH.
3.  **Node.js (Recommended):** Used as the JavaScript runtime engine to extract complex video links. [Download Node.js](https://nodejs.org/).

### Media Players (Optional for Streaming)
* **MPV Player:** Place `mpv.exe` in the script's folder or add it to your PATH.
* **VLC Media Player:** Ensure VLC is installed in its default location (`C:\Program Files\VideoLAN\VLC`).

---

## 🚀 How to Run the App

1.  **Download the release script:** Download the script file from releases and put it into the same folder where yt-dlp is.
2.  **Get yt-dlp:** * The script will automatically check if `yt-dlp` is installed globally on your PC. 
    * *Easiest Method:* Download the Windows executable file (`yt-dlp.exe`) from the [Official yt-dlp Releases](https://github.com/yt-dlp/yt-dlp/releases) and drop it right into the same folder as this script.
3.  **Launch the tool:** Double-click the script file or run this command in your terminal/command prompt inside the folder:
    ```bash
    python "Drag n Drop the script file"
    ```

---

## 💡 Quick Tips for Your Ease

> 🥷 **Bypassing Access/Sign-in Blocks:**
> If you encounter download blocks or errors on certain websites, place your exported `cookies.txt` file directly into the script's folder. The app will automatically detect it and instantly activate the **"Inject cookies.txt parameter profile"** option to bypass restrictions securely! Alternatively, use the **"Cookies from browser"** option from Advanced section.

---
## 😴 For Lazy People

If you don't want to go through Python stuff, you can still try my Same script but based on Windows VBS [HERE](https://github.com/rayhanorigin/ytdlp-gui-windows)

---
## ⚖️ Disclaimer & License
### 📌 I vibe coded the project but I'm pretty confident with this tool. ###
This open-source tool is engineered strictly for personal educational and archival use. Please respect the copyright terms of the respective platforms you interact with. The author holds no responsibility for any misuse or policy violations.

---
Created with ❤️ by **rayhanorigin**
