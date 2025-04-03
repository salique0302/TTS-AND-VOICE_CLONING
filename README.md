# TTS-AND-VOICE_CLONING▶︎ 🗣️•၊၊||၊|။||||။‌‌‌‌‌၊|• 0:10
Voice Cloning TTS with Mel Spectrogram Visualization 🎙️
A text-to-speech application using XTTS v2 with real-time mel spectrogram visualization and voice cloning capabilities.

Python FastAPI TTS

##✨ Features
🗣️ Text to Speech Synthesis: Using Coqui TTS XTTS v2 model
👥 Voice Cloning: Support for custom voice through .wav file upload
📊 Mel Spectrogram Generation: Real-time visualization of speech synthesis
🌍 Multi-Language Support:
🇺🇸 English
🇪🇸 Spanish
🇫🇷 French
🇩🇪 German
🇮🇹 Italian
💻 Interactive Web Interface: Modern UI with dark/light theme
🌊 Real-time Audio Visualization: Waveform animation during playback
##🚀 Installation
Clone the repository:
git clone <repository-url>
Install dependencies:
pip install -r requirements.txt
Run the application:
uvicorn app:app --reload
##📦 Requirements
fastapi
uvicorn
python-multipart
torch
torchaudio
TTS
numpy
librosa
matplotlib
##📁 Project Structure
project/
├── app.py              # FastAPI application
├── mel_generator.py    # Mel spectrogram generation
├── templates/
│   └── index.html     # Web interface
├── generated_audio/    # Output directory
└── dataset/
    └── wavs/          # Default speaker samples
##📝 Usage
Access the web interface at http://localhost:8000
Enter text in the input field
Select desired language
Optionally upload a .wav file for voice cloning
Click "Generate Speech"
View the generated mel spectrogram and play the synthesized audio
##🔧 Technical Details
Backend (app.py)
🚀 FastAPI framework
🧠 XTTS v2 model for speech synthesis
🏗️ DeepLab architecture implementation
⚡ Real-time mel spectrogram generation
##Frontend (index.html)
📱 Responsive design using TailwindCSS
🌓 Dark/Light theme toggle
🎵 Audio visualization
📤 File upload handling
⚡ Asynchronous API communication
Mel Spectrogram Generation
Parameter	Value
Sample rate	22050 Hz
FFT size	1024
Hop length	256
Mel bands	80
##🔌 API Endpoints
POST /generate-speech
Generates speech from text with optional voice cloning.

##Parameters:
Name	Type	Required	Description
text	string	Yes	Input text
language	string	No	Target language (default: "en")
speaker_wav	file	No	Voice sample file (.wav)
Response:
Audio file (.wav)
Mel spectrogram visualization (.png)
GET /health
Health check endpoint returning model and system status.

##🛠️ Development
The application leverages:

🔥 PyTorch for deep learning
🎵 TorchAudio for audio processing
📊 LibROSA for mel spectrogram generation
📈 Matplotlib for visualization
##🌐 Browser Support
✅ Chrome (recommended)
✅ Firefox
✅ Safari
✅ Edge
##⚠️ Known Limitations
Requires a default speaker file at dataset/wavs/1.wav
Audio files must be in WAV format
Processing time varies based on text length
##🔍 Error Handling
📁 File not found errors for missing speaker files
🎵 Audio processing errors
🤖 Model inference errors
✍️ Invalid input validation
A sophisticated text-to-speech system with voice cloning capabilities

Made with ❤️ using FastAPI and PyTorch
