🎙️ Privacy-First Voice AI Assistant

A local, privacy-first voice assistant designed for daily personal use — not for surveillance, automation hype, or cloud dependency.

This project emphasizes engineering discipline: safety, intent control, explicit memory, and reliability — instead of flashy demos.

🧠 Why This Project Exists

Most modern voice assistants are:

Always listening

Cloud-dependent

Opaque about data usage

Difficult to reason about safely

This assistant was built with the opposite philosophy:

Push-to-talk only (no background listening)

Local execution wherever possible

Explicit intent and safety gates

User-controlled memory

No silent automation

The goal is not to replace tools, but to support focused thinking and daily planning.

✨ Core Capabilities
🎙 Voice Interaction

Push-to-talk activation via keyboard hotkey

No always-on microphone

Low-latency speech-to-text (Whisper)

🧠 Reasoning Layer

Natural language understanding via LLM (Groq)

Deterministic intent classification

Calm, concise responses by default

🛡 Safety & Intent Control

Every request is classified before action:

QUERY — informational requests

TASK — limited, sandboxed actions

SYSTEM_ACTION — blocked

REJECT — blocked

The LLM never executes actions directly.

🛠 Safe Tool Execution

Explicitly registered tools only

Sandboxed file access

No shell commands

No OS-level actions

Current tools:

Save personal notes

Read saved notes

🧠 Memory (Explicit & Ethical)

No silent data collection

Memory written only on explicit user request

Local persistence (JSON)

Fully user-auditable and removable

Memory types:

Long-term factual memory (explicit)

Session context (temporary)

No background profiling. Ever.

📅 Daily Briefing / Focus Mode

A calm, proactive mode that:

Summarizes saved context

Suggests one focus for the next hour

Asks one clarifying question

No notifications.
No nagging.
Triggered only when requested.

🏗️ Architecture Overview

The assistant follows a deterministic, layered processing pipeline:

🏗️ Architecture Overview

The assistant follows a deterministic, layered processing pipeline:

Voice Input
→ Speech-to-Text (Whisper)
→ Mode & Intent Detection
→ Safety Gate
→ LLM Reasoning or Tool Execution
→ Text-to-Speech Response


Each layer has a single responsibility, making the system predictable, safe, and easy to extend.

🧩 Design Principles

Single, explicit entry point

Clear separation of concerns

Deterministic control flow

No hidden or implicit state

User control over memory and actions

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


This structure is:

scalable

readable

recruiter-friendly

immediately understandable

🔐 Privacy & Ethics

This assistant:

Does not listen unless explicitly activated

Does not transmit audio recordings

Does not store data without consent

Runs entirely on the user’s machine

Keeps API keys local and uncommitted

Privacy is a default, not an option.

🚀 Getting Started
1. Clone the repository
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


API keys and personal data are never committed to the repository.

5. Run the assistant
python src/main.py


Press Ctrl + Alt + Space to speak

Press ESC to exit

📌 Project Status

Personal, private assistant

Actively used and iterated

Not published as a product

Not intended for mass deployment

This is a deliberately scoped personal system, not a startup demo.

🔮 Future Work (Optional)

Performance tuning

Config-driven behavior

Optional open-source framework version (without personal data)

⚠️ Disclaimer

This project is provided for personal and educational use.
No guarantees are made regarding fitness for production or commercial deployment.
