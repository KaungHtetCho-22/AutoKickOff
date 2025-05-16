# AutoKickOff
**AutoKickOff** is an AI-powered, fully automated video generation pipeline that converts football (soccer) analysis scripts into short-form, social-media-ready videos — including voiceovers, tactical animations, captions, and music. Designed for creators who want to go faceless, fast, and viral.

---

## Features

- **AI Voiceover** (ElevenLabs)
- **Auto-generated tactical visuals** (matplotlib / RunwayML)
- **Auto captions** via Whisper
  **Video composition** via FFmpeg
- **UI Frontend** to input scripts, voice styles, animation preferences
- **FastAPI backend** for processing
- **Dockerized** for local or cloud deployment

---

## Tech Stack

- **Frontend**: React + TailwindCSS (via Lovable.dev)
- **Backend**: FastAPI + Python services
- **Voice**: ElevenLabs API
- **Subtitles**: Whisper (local or API)
- **Video Editing**: FFmpeg, MoviePy
- **Deployment**: Docker + Docker Compose

---

##  Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/yourusername/tactigen.git
cd tactigen
```

### 2. Environment Setup
Create `.env` file in root:
```env
ELEVENLABS_API_KEY=your-key-here
```

### 3. Run with Docker Compose
```bash
docker compose up --build
```

- Frontend → `http://localhost:3000`
- Backend API → `http://localhost:8000`

---

## 📬 API
### `POST /generate`
Generates a football tactics video.

**Payload schema:**
```json
{
  "script": "Here's how Arsenal broke City's mid-block...",
  "voiceStyle": "Energetic",
  "voiceSpeed": 1.1,
  "voiceTone": "Excited",
  "pauseBeforeTactic": true,
  "tacticType": "Build-Up",
  "teamPerspective": "Attacking",
  "highlightPlayer": "Odegaard",
  "fieldStyle": "2D Tactics Board",
  "arrowStyle": "Dashed",
  "highlightZones": true,
  "addCaptions": true,
  "addMusic": true,
  "duration": 45,
  "resolution": "1080p",
  "outputFormat": "mp4"
}
```

---

##  Project Structure
```
frontend/         # React UI
backend/
  ├── app.py       # FastAPI main app
  ├── services/    # Modular video/audio generation services
  └── routes/      # API routes
Dockerfile.*      # Frontend & backend containers
docker-compose.yml
```


---

## Author
**Kaung Htet cho** — AI/ML Engineer | Football Content Creator

---
