# AegisCare AI — Modern Web Frontend

AegisCare AI is a high-performance web interface designed for eldercare monitoring, video-based fall verification, and family alert synchronization. Built with semantic HTML5, Vanilla CSS3 (Dark Glassmorphism), and modern ES6+ JavaScript, it connects seamlessly with the AegisCare FastAPI vision engine.

---

## Key Features

- **Video Analysis Lab:**
  - Benchmark test selector (`sample_fall.mp4`, `sample_walking.mp4`) and drag-and-drop custom video uploader.
  - Dual-mode video player toggle (`AI Skeleton View` with 3D joint highlights vs. `Raw Stream`).
  - Interactive calibrated Risk Gauge showing model likelihood $P(\text{fall}) \in [0, 100\%]$.
  - Temporal synchronization between video playback time and probability telemetry.
- **Live Vision Monitor:**
  - Real-time webcam feed with CCTV surveillance HUD and digital clock.
  - Camera flip controls (front / rear camera support for mobile devices).
  - Single-frame snapshot analysis via Google Gemini Vision.
  - Quick scenario simulations (Resting, Sleeping in Chair, Dropped Cane, Restroom, Inactivity).
- **Patient Emergency SOS:**
  - High-visibility one-touch emergency call trigger that sounds a local audio alarm and immediately dispatches a Telegram notification to registered caregivers.
- **Activity & Incident Timeline:**
  - Chronological activity ledger displaying timestamps, hazard severity tags, and alert dispatch confirmations.
  - Daily Caregiver Digest synthesizing mobility patterns into plain English summaries.
- **Telegram Alert Synchronization:**
  - In-app configuration modal to connect Bot Tokens and Chat IDs with live verification test pings.

---

## Directory Structure

```
├── index.html           # Main application interface and sections
├── styles.css           # Dark-mode glassmorphism design system & responsive rules
├── app.js               # Client controller, video sync, telemetry, and API integration
├── assets/              # Benchmark clips and annotated demo streams
│   ├── sample_fall.mp4
│   ├── sample_fall_annotated.mp4
│   ├── sample_walking.mp4
│   └── sample_walking_annotated.mp4
├── .gitignore
└── README.md
```

---

## Getting Started

### Local Setup
1. **Clone the repository:**
   ```bash
   git clone https://github.com/nandinin822/hackathon-2-nandani-frontend.git
   cd hackathon-2-nandani-frontend
   ```

2. **Serve the static files:**
   Any static HTTP server can host the frontend:
   ```bash
   # Using Python
   python -m http.server 3000
   
   # Or using Node.js / npx
   npx serve .
   ```

3. **Backend Connection:**
   By default, the client communicates with the FastAPI backend on `http://127.0.0.1:8000`. If hosted alongside the backend, it serves directly from `/static`.

---

## Compliance & Medical Safety Disclaimer

AegisCare AI provides automated visual monitoring and heuristic motion classification designed to assist caregivers and family members. It is not an FDA-approved medical diagnostic device and does not replace professional emergency healthcare services.
