🎬 YouTube Video Downloader (Python GUI)
<div align="center">

A simple Python-based YouTube Video Downloader that allows users to download high-quality MP4 videos using a clean file selection dialog.

<img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python" /> <img src="https://img.shields.io/badge/Library-pytube-red?style=for-the-badge" /> <img src="https://img.shields.io/badge/GUI-Tkinter-green?style=for-the-badge" /> <img src="https://img.shields.io/badge/Project-Type%20Utility-orange?style=for-the-badge" /> </div>
📌 Overview

This project is a lightweight desktop utility built using:

🐍 Python

🎥 pytube for YouTube video downloading

🖥 tkinter for folder selection dialog

Users can:

Enter a YouTube video URL
Choose a download directory
Automatically download the video in the highest available MP4 resolution

🚀 Features

✅ Download YouTube videos in highest available resolution
✅ Simple terminal-based interaction
✅ Folder selection via GUI dialog
✅ Error handling for invalid links or download issues
✅ Lightweight and beginner-friendly codebase

🛠 Technologies Used

Python 3.x

pytube

tkinter (built-in with Python)


⚙️ Installation
1️⃣ Clone the repository
git clone https://github.com/your-username/youtube-downloader.git
cd youtube-downloader

2️⃣ Install required dependency
pip install pytube


tkinter comes pre-installed with standard Python distributions.

▶️ How to Run
python main.py


Then:

Enter the YouTube video URL

Select a folder using the file dialog

The video will download automatically

💡 Example Workflow
Please enter a YouTube url: https://youtube.com/...
Started download...
Video downloaded successfully!

🔐 Error Handling

The program handles:

Invalid YouTube URLs

Network issues

Invalid save location

Download interruptions

Errors are printed to the terminal for debugging.

📈 Future Improvements

Add download progress bar

Add resolution selection option

Convert to full GUI app (with buttons & input fields)

Add audio-only download option

Add playlist download support

👨‍💻 Author

Yash Brahmankar


