# IdeaForge  
**AI-Powered Software Idea Evaluator & Validation Platform**

An intelligent web application that helps students, developers, and innovators instantly evaluate the potential of their software ideas using cutting-edge AI analysis. Submit an idea → get deep validation, multi-factor scoring → receive a full development roadmap via POML  all in seconds.

[![GitHub Repo](https://img.shields.io/badge/GitHub-CyberForgeEx/IdeaForgeAI-181717?logo=github)](https://github.com/CyberForgeEx/IdeaForgeAI)
[![Stars](https://img.shields.io/github/stars/CyberForgeEx/IdeaForgeAI?style=social)](https://github.com/CyberForgeEx/IdeaForgeAI)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-3.0%2B-black?logo=flask)](https://flask.palletsprojects.com)
[![Groq AI](https://img.shields.io/badge/Powered%20by-Groq%20AI-ff3434?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mN8/+F9PwAI8wNPvd7POQAAAABJRU5ErkJggg==)](https://groq.com)

---

## Project Goal

Turn vague startup ideas into rigorously evaluated, actionable software projects by combining:

- Smart pre-filtering (keyword + regex + repetition detection)
- Real AI validation & scoring via Groq’s ultra-fast LLMs.
- Professional-grade metrics across 8 critical business/tech dimensions.
- Automatic generation of a structured POML (Prompt Orchestration Markup Language) roadmap.

Perfect for solo founders, indie hackers, product managers, accelerators, and university entrepreneurship programs.

---

#### 1. Core Features
Everything you need to validate ideas at lightspeed

- `Authentication`           – Secure register/login with hashed passwords & session management.
- `Idea Validation Engine`    – Multi-layer checks: length, keywords, AI relevance scoring.
- `AI Evaluation Dashboard`   – 8-factor scoring (0–10) with detailed explanations.
- `POML Generator`            – Auto-creates full development roadmap + prompt chains.
- `Advanced Analytics`        – Stats, rankings, best/worst ideas, factor averages.

#### 2. User Experience & Collaboration
Built for real-world usage

- `Favorites System`          – Star ideas with one-click AJAX toggles
- `Idea Comparison Tool`      – Side-by-side comparison of 4 ideas
- `Mobile-Responsive UI`      – Claymorphic design, dark mode ready, enterprise feel
- `Timezone-Aware`            – Full UTC+4 support with custom Jinja filters

#### 3. Technical Excellence
Production-ready from day one

- `Secure & Scalable`         – Flask + SQLite 
- `Groq-Powered AI`             – Blazing-fast inference (llama-3.3-70b-versatile default)
- `Smart Error Handling`        – Graceful fallbacks, user-friendly messages.

---

## Quick Start

```bash
# Clone the repository
git clone https://github.com/CyberForgeEx/IdeaForgeAI.git
cd IdeaForgeAI

# Set up virtual environment
python3 -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Create .env file (get your free key at console.groq.com)
echo "GROQ_API_KEY=your_groq_api_key_here" > .env
echo "SECRET_KEY=$(openssl rand -hex 32)" >> .env

# Run the app
python app.py
```

Open → http://127.0.0.1:5000

---

### Prerequisites

- Python 3.10+
- Git
- Free Groq API key → [console.groq.com](https://console.groq.com)

Install everything on Ubuntu/Debian:
```bash
sudo apt update && sudo apt install python3 python3-venv python3-pip git
```

---

## Recommended Workflow

1. Register → `/register`
2. Submit your first idea → `/evaluate`
3. View AI evaluation + scores → redirects to `/idea/<id>`
4. Generate POML roadmap → button on idea page
5. Check your dashboard → `/dashboard` for stats & rankings
6. Compare your top ideas → comparison tool
7. Star favorites & add comments for future reference.

---

## Useful Tools While Building Ideas

| Tool              | Purpose                                    |
|-------------------|--------------------------------------------|
| Groq Console      | Monitor usage & test prompts               |
| Cursor / Windsurf | AI-assisted coding with POML import        |
| Notion / Obsidian | Store and organize your evaluated ideas    |
| Figma             | Rapid UI mockups from POML suggestions     |

---

**Turn inspiration into validated, build-ready software projects instantly.**

If IdeaForge helps you kill bad ideas fast and double down on winners, please give it a star it truly makes a huge motivation!

[github.com/CyberForgeEx/IdeaForgeAI](https://github.com/CyberForgeEx/IdeaForgeAI)
