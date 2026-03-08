<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=FF0000&height=200&section=header&text=YouTube%20Video%20Downloader&fontSize=40&fontColor=ffffff&fontAlignY=38&desc=Simple%20%7C%20Fast%20%7C%20Lightweight&descAlignY=58&descAlign=50" width="100%"/>

<br/>

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![pytube](https://img.shields.io/badge/Library-pytube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://pytube.io)
[![Tkinter](https://img.shields.io/badge/GUI-Tkinter-4CAF50?style=for-the-badge&logo=python&logoColor=white)](https://docs.python.org/3/library/tkinter.html)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)]()

<br/>

> **A lightweight Python desktop utility to download YouTube videos in the highest available MP4 resolution — with a clean folder-selection dialog and robust error handling.**

<br/>

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Error Handling](#-error-handling)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [Author](#-author)
- [License](#-license)

---

## 🎯 Overview

**YouTube Video Downloader** is a beginner-friendly yet capable Python utility that simplifies downloading YouTube videos to your local machine. It combines the power of `pytube` for video fetching with `tkinter`'s native folder dialog for a smooth, minimal user experience — no browser extensions, no bloated software.

Built for developers, students, and power users who prefer a clean, code-first tool over third-party downloaders.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🎥 **Highest Resolution** | Automatically selects the best available MP4 stream |
| 🖥️ **GUI Folder Picker** | Native OS dialog via `tkinter` for save location selection |
| ⚡ **Fast & Lightweight** | No heavy frameworks — minimal dependencies |
| 🛡️ **Error Handling** | Gracefully handles invalid URLs, network issues, and bad paths |
| 🐍 **Beginner Friendly** | Clean, readable codebase — great for learning |

---

## 🛠 Tech Stack

| Technology | Purpose |
|---|---|
| **Python 3.x** | Core programming language |
| **pytube** | YouTube video streaming & downloading |
| **tkinter** | GUI folder selection dialog (built-in with Python) |

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- Python 3.x — [Download here](https://www.python.org/downloads/)
- pip (comes with Python)

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/loisekk/youtube-downloader.git
cd youtube-downloader
```

**2. Install the required dependency**

```bash
pip install pytube
```

> `tkinter` comes pre-installed with all standard Python distributions — no extra setup needed.

---

## ▶️ Usage

Run the script from your terminal:

```bash
python main.py
```

**Workflow:**

```
1. A prompt appears → Enter your YouTube video URL
2. A folder dialog opens → Select your desired download location
3. Download begins automatically → Progress logged to terminal
4. ✅ Done! Video saved to your chosen folder.
```

**Example terminal output:**

```
Please enter a YouTube URL: https://www.youtube.com/watch?v=dQw4w9WgXcQ
Started download...
Video downloaded successfully!
```

---

## 📁 Project Structure

```
youtube-downloader/
│
├── main.py          # Entry point — handles input, download logic & GUI dialog
├── README.md        # Project documentation
└── requirements.txt # Project dependencies
```

---

## 🔐 Error Handling

The application gracefully handles the following failure scenarios:

- ❌ **Invalid YouTube URL** — Notifies the user and exits cleanly
- 🌐 **Network/Connection Issues** — Catches exceptions and prints a helpful message
- 📂 **Invalid Save Location** — Handles bad or inaccessible directory paths
- ⛔ **Download Interruption** — Catches mid-download failures without crashing

All errors are printed directly to the terminal for easy debugging.

---

## 📈 Roadmap

- [ ] Add real-time download progress bar
- [ ] Resolution selector (144p → 4K)
- [ ] Full GUI app with input fields & buttons
- [ ] Audio-only download (MP3 extraction)
- [ ] Playlist & batch download support
- [ ] Dark mode UI

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 👨‍💻 Author

<div align="center">

**Yash Brahmankar**

[![GitHub](https://img.shields.io/badge/GitHub-loisekk-181717?style=for-the-badge&logo=github)](https://github.com/loisekk)
[![Email](https://img.shields.io/badge/Email-yashbrahmankar95%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:yashbrahmankar95@gmail.com)

</div>

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) — feel free to use, modify, and distribute.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=FF0000&height=120&section=footer" width="100%"/>

*Made with ❤️ by Yash Brahmankar*

</div>
