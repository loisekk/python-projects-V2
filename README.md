<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=32&duration=3000&pause=1000&color=FF0000&center=true&vCenter=true&width=700&lines=📺+YouTube-Search-Quirer;Search.+Click.+Watch.;Zero+Shorts.+Zero+Noise.;Powered+by+Selenium+%2B+AI)](https://git.io/typing-svg)

<br/>

<img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Streamlit-1.37-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white"/>
<img src="https://img.shields.io/badge/Selenium-4.22-43B02A?style=for-the-badge&logo=selenium&logoColor=white"/>
<img src="https://img.shields.io/badge/YouTube%20Data%20API-v3-FF0000?style=for-the-badge&logo=youtube&logoColor=white"/>
<img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge"/>

<br/><br/>

> **A YouTube automation & clone toolkit — search smarter, watch faster, skip the noise.**

</div>

---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 🧠 What Is This?

**YouTube-Search-Quirer** is a multi-mode YouTube automation project built with Python, Selenium, Streamlit, and the YouTube Data API v3. It gives you a faster, cleaner YouTube experience — without algorithmic noise, without Shorts, and without friction.

It ships in **three distinct modes**, each serving a different use case:

<br/>

<div align="center">

| 🔢 | Mode | Entry Point | Description |
|:--:|------|-------------|-------------|
| 01 | 🖥️ **Terminal Agent** | `main.py` | InquirerPy CLI — pick genre, year, GP, anime, game, or topic and auto-play |
| 02 | 🌐 **Streamlit Smart Watch** | `main_v1.py` | Minimalist UI that auto-searches and opens the first full video via Selenium |
| 03 | 📺 **YouTube Clone UI** | `app2.py` | Full YouTube-style dark clone with video grid, Shorts, voice search & sidebar |

</div>

<br/>

---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## ✨ Features

<br/>

```
🎯  Category-driven Search    →   F1 / Anime / Gaming / Movies / Web Series / Cartoons / Study
⚡  Shorts-Free Playback      →   Automation skips Shorts and plays full-length videos only
🎙️  Voice Search              →   Speak your query via microphone using SpeechRecognition
📺  YouTube Clone UI          →   Dark-mode interface with video grid, tag filters & sidebar
🔌  YouTube Data API v3       →   Real video and Shorts search powered by Google APIs
🗄️  SQLite Persistence        →   Watch-later list, playlists, and user auth — all local
🤖  Selenium Automation       →   Launches Chrome, searches YouTube, clicks the first result
💡  AI/LLM-Ready              →   OpenAI + LangChain included for future agent upgrades
```

<br/>

---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 🗂️ Project Structure

```bash
📦 YouTube-Search-Quirer/
│
├── 🧠 main.py              # Terminal agent — InquirerPy category flow + Selenium playback
├── 🌐 main_v1.py           # Streamlit Smart Watch UI
├── 📺 app2.py              # Full YouTube Clone UI (API-powered)
│
├── 🔌 youtube_api.py       # YouTube Data API v3 — search_videos() & search_shorts()
├── ▶️  youtube_player.py    # Selenium playback module
├── 🎙️ voice_search.py      # Microphone voice input via SpeechRecognition
├── 💡 recommender.py       # Recommendation engine (history-based, expandable)
│
├── 🔐 auth.py              # SQLite user authentication — register / login
├── 🗄️ database.py          # SQLite watch-later & playlists storage
│
├── 📋 requirements.txt     # All Python dependencies
└── 📖 README.md
```

---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## ⚙️ Setup & Installation

### `Step 1` — Clone the repo

```bash
git clone https://github.com/loisekk/YouTube-Search-Quirer.git
cd YouTube-Search-Quirer
```

### `Step 2` — Install dependencies

```bash
pip install -r requirements.txt
```

### `Step 3` — Add your YouTube API Key

Open `youtube_api.py` and replace:

```python
API_KEY = "YOUR_YOUTUBE_DATA_API_KEY_HERE"
```

> 🔑 Get your free key at [Google Cloud Console](https://console.cloud.google.com/) → Enable **YouTube Data API v3**

### `Step 4` — ChromeDriver (Selenium modes only)

```bash
pip install webdriver-manager
```

> ✅ ChromeDriver is auto-managed. Just make sure **Google Chrome** is installed.

---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 🚀 Usage

<br/>

**▶ Terminal Agent**
```bash
python main.py
```
> Follow prompts → Select category → Sub-category → Auto-plays in Chrome

<br/>

**▶ Streamlit Smart Watch**
```bash
streamlit run main_v1.py
```

<br/>

**▶ YouTube Clone UI**
```bash
streamlit run app2.py
```

---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 🛠️ Tech Stack

<br/>

<div align="center">

| Layer | Technology |
|:------|:-----------|
| 🖥️ UI Framework | Streamlit |
| 🤖 Browser Automation | Selenium + WebDriver Manager |
| 📡 Video Data | YouTube Data API v3 |
| 🎙️ Voice Input | SpeechRecognition |
| 💬 CLI Prompts | InquirerPy |
| 🗄️ Database | SQLite3 |
| 🌐 HTTP / Async | requests, aiohttp |
| 🔐 Environment | python-dotenv |
| 🧠 Future AI Layer | OpenAI, LangChain |

</div>

<br/>

---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 🗺️ Roadmap

```
 ✅  Terminal agent with category flow
 ✅  Streamlit Smart Watch UI
 ✅  YouTube Clone with API integration
 ✅  Voice search support
 🔲  LLM-powered natural language query processing
 🔲  Watch history tracking & smart recommendations
 🔲  Playlist management UI
 🔲  User login with SHA-256 hashed passwords
```

---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 👨‍💻 Author

<br/>

<div align="center">

**Yash Brahmankar**
<br/>
B.Tech AI & ML · OIST (2024–2028) · Oracle & Cisco Certified

<br/>

[![GitHub](https://img.shields.io/badge/GitHub-loisekk-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/loisekk)
[![Email](https://img.shields.io/badge/Gmail-yashbrahmankar95@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:yashbrahmankar95@gmail.com)

</div>

<br/>

---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## 📄 License

This project is licensed under the **[MIT License](LICENSE)** — free to use, modify, and distribute.

---

<div align="center">

<br/>

![](https://komarev.com/ghpvc/?username=loisekk&color=FF0000&style=for-the-badge&label=PROFILE+VIEWS)

<br/>

*Built for learning, automation, and portfolio-level presentation* ⚡

<br/>

**If you found this useful, consider giving it a ⭐**

</div>
