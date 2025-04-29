# 🤖 Automated-and-Intelligent-Note-Making

This repository contains Python scripts for automating note-making tasks:
1. Converting recorded presentation videos into PDF slide decks.
2. Speech recognition and emotion detection on audio input.

---

## 📁 Repository Structure

```
Automated-and-Intelligent-Note-Making/
├── input/                      # Sample videos for slide conversion
│   ├── Test Video 1.mp4
│   └── Test Video 2.mp4
├── output/                     # Generated outputs (screenshots, PDFs)
├── video2pdfslides.py          # Script to convert video into PDF slides
├── Speech_Recognition.py       # Script for speech-to-text transcription
├── Speech_Emotion_Recognition.py # Script for extracting speech emotion features
├── requirements.txt            # Python dependencies
├── .gitignore                  # Git ignore rules
└── README.md                   # This file
```

---

## 🧰 Setup

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ⚙️ Scripts

### 1. Video to PDF Slides (`video2pdfslides.py`)

Captures unique frames from a presentation video and compiles them into a PDF slide deck.

**Usage:**

```bash
python video2pdfslides.py <video_path>
```

- **Input**: Path to an MP4 video.
- **Process**:
  1. Extracts frames where significant scene changes occur.
  2. Pauses for manual review to delete duplicate or unwanted frames.
  3. Generates a PDF of the remaining frames.
- **Output**: PDF saved in `output/` directory (e.g., `slides.pdf`).

### 2. Speech Recognition (`Speech_Recognition.py`)

Transcribes speech from an audio source to text.

**Usage:**

```bash
python Speech_Recognition.py --audio <audio_path> --output <transcript.txt>
```

- **Dependencies**: Requires `speech_recognition` library.
- **Features**:
  - Supports WAV and MP3 formats.
  - Outputs plain text transcription.

### 3. Speech Emotion Recognition (`Speech_Emotion_Recognition.py`)

Extracts emotion-related features from speech audio.

**Usage:**

```bash
python Speech_Emotion_Recognition.py --audio <audio_path> --output <features.csv>
```

- **Dependencies**: Requires libraries like `librosa` and `numpy`.
- **Features**:
  - Extracts pitch, energy, MFCCs.
  - Saves features to a CSV for further analysis.

---

## 📝 Example

Convert a demo video into slides:

```bash
python video2pdfslides.py "./input/Test Video 1.mp4"
```

Transcribe audio:

```bash
python Speech_Recognition.py --audio "./input/sample_audio.wav" --output transcript.txt
```

Extract emotion features:

```bash
python Speech_Emotion_Recognition.py --audio "./input/sample_audio.wav" --output features.csv
```

---

## 👤 Author

**Abhishek Narayan**  
IIT Delhi
