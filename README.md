# TTS-AND-VOICE_CLONING▶︎ 🗣️•၊၊||၊|။||||။‌‌‌‌‌၊|• 0:10
# Voice Cloning TTS with Mel Spectrogram Visualization 🎧

<div align="center">

A text-to-speech application using XTTS v2 with real-time mel spectrogram visualization and voice cloning capabilities.

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.68.0+-00a393.svg)](https://fastapi.tiangolo.com/)
[![TTS](https://img.shields.io/badge/TTS-v2.0+-red.svg)](https://github.com/coqui-ai/TTS)

</div>

---

## ✨ Features

- 🗣️ **Text to Speech Synthesis**: Powered by Coqui TTS XTTS v2 model
- 👥 **Voice Cloning**: Supports custom voice cloning using .wav files
- 📊 **Mel Spectrogram Generation**: Visualizes synthesized speech in real time
- 🌍 **Multi-Language Support**:
  - 🇺🇸 English
  - 🇪🇸 Spanish
  - 🇫🇷 French
  - 🇩🇪 German
  - 🇮🇹 Italian
- 💻 **Interactive Web Interface**: Modern UI with dark/light theme
- 🌊 **Real-time Audio Visualization**: Waveform animation during playback

## 🚀 Installation

1. Clone the repository:
```bash
git clone <your-repository-url>
cd <repository-name>
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the application:
```bash
uvicorn app:app --reload
```

## 📦 Requirements

```plaintext
fastapi
uvicorn
python-multipart
torch
torchaudio
TTS
numpy
librosa
matplotlib
```

## 💁️‍♂️ Project Structure

```plaintext
project/
├── app.py              # FastAPI application
├── mel_generator.py    # Mel spectrogram generation
├── templates/
│   └── index.html      # Web interface
├── generated_audio/    # Output directory
└── dataset/
    └── wavs/          # Default speaker samples
```

## 📝 Usage

1. Open `http://localhost:8000` in your browser.
2. Enter text in the input field.
3. Select the desired language.
4. (Optional) Upload a .wav file for voice cloning.
5. Click "Generate Speech."
6. View the generated mel spectrogram and play the synthesized audio.

## 🛠️ Technical Details

### Backend (app.py)
- ⚡ FastAPI framework
- 🧠 XTTS v2 model for speech synthesis
- 🛠️ DeepLab architecture implementation
- 🔦 Real-time mel spectrogram generation

### Frontend (index.html)
- 📱 Responsive design using TailwindCSS
- 🌄 Dark/Light theme toggle
- 🎵 Audio visualization
- 👍 File upload handling
- ⚡ Asynchronous API communication

### Mel Spectrogram Parameters
| Parameter | Value |
|-----------|-------|
| Sample rate | 22050 Hz |
| FFT size | 1024 |
| Hop length | 256 |
| Mel bands | 80 |

## 🔀 API Endpoints

### POST `/generate-speech`
Generates speech from text with optional voice cloning.

#### Parameters:
| Name | Type | Required | Description |
|------|------|----------|-------------|
| `text` | string | Yes | Input text |
| `language` | string | No | Target language (default: "en") |
| `speaker_wav` | file | No | Voice sample file (.wav) |

#### Response:
- Generated audio file (.wav)
- Mel spectrogram visualization (.png)

### GET `/health`
Health check endpoint returning model and system status.

## 🛠️ Development

- 🔥 PyTorch for deep learning
- 🎵 TorchAudio for audio processing
- 📊 LibROSA for mel spectrogram generation
- 📊 Matplotlib for visualization

## 🌐 Browser Support

- ✅ Chrome (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge

## ⚠ Known Limitations

- Requires a default speaker file at `dataset/wavs/1.wav`
- Supports only WAV format for voice cloning
- Processing time depends on text length

## 🔍 Error Handling

- 💾 File not found errors for missing speaker files
- 🎵 Audio processing errors
- 🤖 Model inference errors
- ✍️ Input validation errors

---

<div align="center">
  <p><strong>A powerful text-to-speech system with voice cloning capabilities</strong></p>
  <p>Made with ❤️ using FastAPI and PyTorch</p>
</div>

