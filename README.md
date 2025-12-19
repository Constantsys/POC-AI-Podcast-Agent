# AI Podcast Generator Agent – Backend (POC)

## About
This project is a **Proof of Concept (POC)** for an **AI Podcast Generator Agent** built using **Node.js**.

The system automatically generates podcast-style audio content using **Large Language Models (LLMs)** and **Text-to-Speech (TTS)** services powered by **Google Gemini** and **OpenAI**.  
Generated podcasts are saved as audio files and can be used for experimentation, demos, or future production pipelines.

---

## Tech Stack
- **Node.js** – Backend runtime
- **Google Gemini API** – Content generation (LLM)
- **OpenAI API** – AI-assisted text & audio processing
- **Google Cloud Text-to-Speech** – Audio generation
- **dotenv** – Environment variable management
- **fs / path** – File handling
- **REST API** – Trigger-based generation

---

## Project Structure

ai-podcast-backend-gen
│
├── node_modules/
│
├── output/
│ ├── podcast_1761803733404.mp3
│ └── podcast_1761803850722.mp3
│
├── env/
│ └── .env
│
├── checkModels.js
├── server.js
│
├── .gitignore
├── package.json
├── package-lock.json
└── README.md


---

## Folder & File Details

### `output/`
Stores generated podcast audio files in **MP3 format**.  
Each file is timestamped to ensure uniqueness.

---

### `env/.env`
Contains all environment variables required to connect with external AI services.

---

### `checkModels.js`
Utility script used to:
- Validate available AI models
- Test Gemini / OpenAI connectivity
- Ensure proper configuration before podcast generation

---

### `server.js`
Main application entry point:
- Initializes the server
- Handles API requests
- Orchestrates AI prompt generation
- Converts generated content to podcast audio
- Saves output files

---

## Environment Configuration

Create a `.env` file inside the `env` folder:

```env
GOOGLE_API_KEY=your_google_gemini_api_key
PORT=5000

USE_GOOGLE_TTS=1
GOOGLE_TTS_CREDENTIALS=your_google_tts_credentials_json

OPENAI_API_KEY=your_openai_api_key
