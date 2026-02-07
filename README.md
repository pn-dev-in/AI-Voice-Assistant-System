# Voice-First AI Assistant (Local, Privacy-Preserving)

An applied AI system demonstrating **speech recognition, LLM-based reasoning, safety guardrails, and modular AI architecture**.


## 🔍 What This Project Demonstrates
- End-to-end AI system design
- Voice-based human–AI interaction
- LLM integration (Groq)
- Safety-aware intent classification
- Local-first, privacy-preserving architecture
- Modular, extensible Python codebase


## 📌 Overview
A local, privacy-first, voice-driven AI assistant designed for daily personal use.

Unlike cloud-based assistants, this system runs locally, activates only on explicit user input, and enforces strict safety and memory controls.

---

## ✨ Key Features
- LLM-based reasoning using Groq
- Push-to-talk voice interaction (no always-on listening)
- Explicit, user-controlled long-term memory
- Intent classification with safety guardrails
- Sandboxed task execution
- Modular and extensible architecture

---


## 🏗️ System Architecture
Voice Input  
→ Speech-to-Text (Whisper)  
→ Mode & Intent Detection  
→ Safety Gate  
→ LLM Reasoning (Groq) or Tool Execution  
→ Text-to-Speech Response

---

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

## 🎯 Intended Role Fit
This project is aligned with:
- AI/ML Engineer (Applied Systems)
- AI Engineer – Voice / Conversational AI
- Software Engineer (AI-integrated systems)

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

⚠️ Disclaimer

This project is provided for personal and educational use.
No guarantees are made regarding fitness for production or commercial deployment.
