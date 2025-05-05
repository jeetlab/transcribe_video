# 🎙️ Whisper Video Transcriber

This repository provides a simple Python script to **automatically transcribe audio from video files** using [OpenAI's Whisper](https://github.com/openai/whisper) speech recognition model. It supports batch transcription of multiple video files in a directory and outputs plain-text transcripts.

---

## 📌 Features

- ✅ Automatically detects and uses GPU (CUDA) if available
- 📂 Batch processing of videos from a folder
- 🧠 Supports Whisper model variants: `tiny`, `base`, `small`, `medium`, `large`
- 🎥 Compatible with `.mp4`, `.mkv`, `.avi`, and `.mov` video formats
- 📄 Saves clean text transcripts in `.txt` format, named after each input video

---

## 🧰 Requirements

- Python 3.7 or higher
- [Whisper](https://github.com/openai/whisper)
- [PyTorch](https://pytorch.org/get-started/locally/)

### 🔧 Installation

First, install Whisper and PyTorch:

```bash
# Install Whisper from GitHub
pip install git+https://github.com/openai/whisper.git

# Install PyTorch (choose appropriate version for your system from https://pytorch.org/)
pip install torch
