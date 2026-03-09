<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0f0f,50:1a1a2e,100:16213e&height=240&section=header&text=Python%20Utility%20Scripts%20V2&fontSize=48&fontColor=ffffff&fontAlignY=36&desc=YouTube%20Downloader%20%7C%20Auto%20Backup%20Scheduler&descAlignY=56&descAlign=50" width="100%"/>

<br/>

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![pytube](https://img.shields.io/badge/pytube-YouTube%20Download-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://pytube.io)
[![Tkinter](https://img.shields.io/badge/Tkinter-GUI%20Dialog-4B8BBE?style=for-the-badge&logo=python&logoColor=white)](https://docs.python.org/3/library/tkinter.html)
[![Schedule](https://img.shields.io/badge/Schedule-Task%20Automation-00C896?style=for-the-badge)](https://schedule.readthedocs.io)
[![License](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-00FF88?style=for-the-badge)](.)

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=24&duration=3000&pause=1000&color=00C896&center=true&vCenter=true&width=700&lines=🎬+YouTube+Downloader;💾+Auto+Backup+Scheduler;Automate+the+boring+stuff.;Built+with+Python.)](https://git.io/typing-svg)

<br/>

> *Two scripts. Two problems solved. Zero manual effort.*
> A YouTube video downloader with folder picker GUI and a scheduled daily backup automation — both built with pure Python.

<br/>

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Key Capabilities](#-key-capabilities)
- [How It Works](#-how-it-works)
- [Tech Stack](#-tech-stack)
- [Quick Start](#-quick-start)
- [Project Structure](#-project-structure)
- [Configuration](#-configuration)
- [Design Decisions](#-design-decisions--trade-offs)
- [Roadmap](#-roadmap)
- [Author](#-author)

---

## 📖 Overview

Two focused, production-ready Python utility scripts — each solving a real everyday problem with clean, minimal code.

**Script 1 — YouTube Downloader (`youtube.py`)**
Paste a YouTube URL, pick a save folder via a GUI dialog, and download the highest available resolution MP4 automatically. No browser extensions, no sketchy websites.

**Script 2 — Auto Backup Scheduler (`backup.py`)**
Set a source folder and a destination, and a scheduled job runs every day at a fixed time — silently copying your files into a dated backup folder without you lifting a finger.

> Built to demonstrate real-world Python utility scripting: GUI integration, file I/O, task scheduling, and automation with zero external infrastructure.

---

## ⚡ Key Capabilities

| Capability | Details |
|---|---|
| 🎬 **YouTube Video Download** | Downloads highest resolution MP4 using pytube |
| 📂 **GUI Folder Picker** | Tkinter file dialog — no hardcoded paths, no terminal path typing |
| 💾 **Daily Backup Automation** | Scheduled daily folder copy using the `schedule` library |
| 🗓️ **Date-Stamped Backups** | Each backup is saved in a folder named by today's date automatically |
| 🔁 **Always-On Scheduler** | Runs in a loop — set it once, forget it forever |
| 🛡️ **Duplicate Guard** | Skips backup if today's folder already exists — no accidental overwrites |

---

## 🧠 How It Works

### YouTube Downloader Pipeline

```
1. User runs youtube.py
       │
2. Terminal prompts for a YouTube URL
       │
3. Tkinter opens a GUI folder picker dialog
       │
4. pytube fetches all available streams for the URL
   └── Filters: progressive=True, file_extension=mp4
       │
5. Highest resolution stream is selected and downloaded
       │
6. File saved to the chosen directory
```

### Auto Backup Scheduler Pipeline

```
1. User runs backup.py
       │
2. schedule library registers a daily job at the set time (e.g. 18:57)
       │
3. Every 60 seconds, schedule.run_pending() checks if it's time
       │
4. At trigger time → copy_folder_to_directory() fires
   ├── Gets today's date → builds destination path
   ├── shutil.copytree() copies the entire source folder
   └── If folder already exists → skips gracefully (FileExistsError)
       │
5. Loop continues — runs every day until process is stopped
```

---

## 🔧 Tech Stack

| Layer | Technology | Role |
|---|---|---|
| **Video Download** | pytube | Fetch and download YouTube streams |
| **GUI Dialog** | Tkinter (tkinter.filedialog) | Folder selection without hardcoding paths |
| **File Operations** | shutil, os | Copy folders and build destination paths |
| **Scheduling** | schedule | Register and trigger daily timed jobs |
| **Date Handling** | datetime | Generate date-stamped backup folder names |
| **Loop Control** | time | 60-second polling interval for the scheduler |
| **Language** | Python 3.10+ | Core runtime |

---

## 🚀 Quick Start

```bash
# 1. Clone the repository
git clone https://github.com/loisekk/python-utility-scripts-v2.git
cd python-utility-scripts-v2

# 2. Install dependencies
pip install pytube schedule

# 3. Run the YouTube Downloader
python youtube.py

# 4. Run the Auto Backup Scheduler
python backup.py
```

### YouTube Downloader — Example

```
Please enter a YouTube url: https://www.youtube.com/watch?v=dQw4w9WgXcQ
[GUI folder picker opens → user selects folder]
Started download...
Video downloaded successfully!
```

### Auto Backup — Example Output

```
Folder copied to: C:/Users/yashb/Desktop/Backups/2026-03-10
```

---

## 📂 Project Structure

```
📦 python-utility-scripts-v2/
│
├── youtube.py         # YouTube video downloader — pytube + Tkinter GUI
├── backup.py          # Scheduled daily folder backup — schedule + shutil
│
└── README.md          # You are here
```

---

## ⚙️ Configuration

### YouTube Downloader
No configuration needed — folder path is selected via GUI dialog at runtime.

### Auto Backup Scheduler

Open `backup.py` and update these two lines to match your machine:

```python
source_dir = "C:/Users/yourname/path/to/source/folder"
destination_dir = "C:/Users/yourname/path/to/backup/destination"
```

Update the daily trigger time:

```python
schedule.every().day.at("18:57").do(...)  # Change to your preferred time (HH:MM)
```

> ✅ The script will create a new dated subfolder (e.g. `Backups/2026-03-10`) each day automatically.

---

## 🛡️ Design Decisions & Trade-offs

| Decision | Chosen Approach | Alternative Considered | Rationale |
|---|---|---|---|
| **Download Library** | pytube | yt-dlp, requests + scraping | pytube is lightweight, pure Python, and simple to use for basic downloads |
| **Folder Selection** | Tkinter filedialog | Hardcoded path / argparse | GUI picker is user-friendly and works cross-platform without any setup |
| **Scheduling** | schedule library | APScheduler, cron (Linux) | `schedule` is minimal, readable, and runs in pure Python with no OS dependency |
| **Backup Method** | shutil.copytree | rsync, cloud sync | Zero external dependencies — works on any machine without additional tools |
| **Duplicate Handling** | FileExistsError catch | Overwrite / timestamp suffix | Silent skip is safest — prevents accidental data loss on re-runs |
| **Date Naming** | `datetime.date.today()` | UUID / timestamp | Human-readable date folders are easy to navigate and sort |

---

## 🗺️ Roadmap

| Enhancement | Priority |
|---|---|
| 🖥️ Streamlit UI for YouTube Downloader | High |
| 📊 Download progress bar with tqdm | High |
| 🎵 Audio-only (MP3) download option | Medium |
| 📧 Email notification after backup completes | Medium |
| 🗂️ Backup multiple source folders at once | Medium |
| ☁️ Cloud backup support — Google Drive / S3 | Low |
| 🐳 Docker support for backup scheduler | Low |

---

## 👨‍💻 Author

<div align="center">

**Yash Brahmankar**

*Python Developer · Automation · AI & ML*

<br/>

[![GitHub](https://img.shields.io/badge/GitHub-loisekk-181717?style=for-the-badge&logo=github)](https://github.com/loisekk)
[![Email](https://img.shields.io/badge/Email-yashbrahmankar95%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:yashbrahmankar95@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/)

<br/>

⭐ **If this project was useful, a star goes a long way — thank you.**

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:16213e,50:1a1a2e,100:0f0f0f&height=140&section=footer" width="100%"/>

*Built with automation and Python by Yash Brahmankar*

</div>
