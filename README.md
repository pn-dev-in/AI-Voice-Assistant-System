# 🎙️ Personal Voice-First AI Assistant

A **local, privacy-first, voice-driven AI assistant** designed for personal daily use.

This project focuses on **usability, safety, and human control**, rather than automation hype or always-on surveillance.

Unlike cloud-based chatbots, this assistant acts as a **personal AI mediator** that runs locally and responds only when explicitly invoked.

---

## ✨ Key Features

- 🎤 **Push-to-talk voice interaction** (no always-on listening)
- 🧠 **LLM-based reasoning** powered by Groq
- 🔊 **Voice responses** via Text-to-Speech
- 🧭 **Intent classification & safety guardrails**
- 🗂️ **Explicit long-term memory** (user-controlled, opt-in only)
- 🛠️ **Sandboxed task execution** (notes, simple utilities)
- 🧩 **Modular and extensible architecture**

---

## 🏗️ Architecture Overview

Voice Input
↓
Speech-to-Text (Whisper)
↓
Intent & Safety Layer
↓
LLM Reasoning (Groq)
↓
Tool / Memory / Response
↓
Text-to-Speech


This layered design ensures **clear separation of concerns**, predictable behavior, and strong safety boundaries.

---

## 🔐 Privacy & Safety Principles

This assistant is designed to be **trustworthy by default**.

- No always-on microphone
- No silent memory storage
- No OS-level or shell command execution
- No user data stored remotely
- All personal data remains local to the machine
- LLM access is used strictly for reasoning and language generation

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
2. Create a virtual environment
python -m venv venv
venv\Scripts\activate
3. Install dependencies
pip install -r requirements.txt
4. Configure environment variables
Create a .env file in the project root:

GROQ_API_KEY=your_api_key_here
Note: API keys and personal data are never committed to the repository.

5. Run the assistant
python src/main.py
Press Ctrl + Alt + Space to speak

Press ESC to exit

🧠 Why This Project Exists
This assistant was built to reduce friction in daily thinking and productivity by providing a private, voice-first interface to intelligence, instead of repeatedly opening web-based chat applications.

The goal is not autonomy.
The goal is useful presence with human control.

📌 Notes
This project is intended primarily for personal use

Users must supply their own API keys

Personal memory and notes are stored locally and never shared

Future improvements are guided by real usage, not feature bloat

🔮 Future Work (Optional)

Performance tuning

Config-driven behavior

Optional open-source framework version (without personal data)

⚠️ Disclaimer

This project is provided for personal and educational use.
No guarantees are made regarding fitness for production or commercial deployment.

📁 Project Structure

voice_ai_agent/
├── src/
│   ├── main.py            # Application entry point
│   │
│   ├── audio/             # Speech-to-text (Whisper)
│   ├── brain/             # LLM reasoning logic
│   ├── safety/            # Intent classification & guardrails
│   ├── tools/             # Sandboxed task execution
│   ├── memory/            # Explicit, user-controlled memory
│   ├── modes/             # Interaction modes (normal, briefing)
│   └── voice/             # Text-to-speech
│
├── user_data/             # Local-only personal data (gitignored)
├── config.yaml            # Runtime configuration
├── requirements.txt
└── README.md
