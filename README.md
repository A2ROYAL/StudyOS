# 🎓 StudyOS — Your AI-Powered Study Workspace

> **The study workspace that actually thinks with you.**
> Plan your day, track every subject, focus deeply, and learn faster — all in one place. No sign-up. No backend. Your data stays on your device.

![StudyOS](https://img.shields.io/badge/StudyOS-v3.0.0-8052ff?style=for-the-badge&logo=bookstack&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-00d4aa?style=for-the-badge)
![No Backend](https://img.shields.io/badge/No%20Backend-Runs%20Locally-ff6b6b?style=for-the-badge)
![Built for Students](https://img.shields.io/badge/Built%20for-Students%20Worldwide-f5c518?style=for-the-badge)

---

## ✨ What is StudyOS?

StudyOS is a **free, open-source study command center** that runs entirely in your browser — pure HTML/CSS/JS, zero dependencies, no cloud. Open `index.html` and go.

It adapts to **any student, anywhere**: pick your country and education level during onboarding and it suggests the right subjects (school, university, or competitive-exam prep).

---

## 🚀 Features

- 🌍 **Global onboarding** — name + target date → country → education level → auto-suggested subjects (fully editable).
- ✨ **AI Day Planner** — describe what you need to study + hours available, and get a time-blocked schedule (Pomodoro / Deep Work / Balanced / Exam styles).
- 📝 **Smart Notes** — write notes, get AI auto-summaries, and turn any note into flashcards in one click.
- 🃏 **Flashcards** — spaced-repetition decks with a flip-to-study mode, grouped by subject.
- 🔗 **Resources** — one-click quick-launch to NotebookLM, Khan Academy, Wolfram Alpha, Desmos, Anki, Quizlet, and more, plus your own saved link library with search.
- ⏱️ **Focus Timer** — Pomodoro, Short/Long Break, and Deep Work (90 min). Completed sessions feed your real stats.
- 🎯 **Goals & Mastery** — track per-subject mastery with sliders and set milestones.
- 📊 **Real dashboard** — today's study time, streak, mastery, and a 12-week activity heatmap, all derived from actual sessions (no fake numbers).
- 🌌 **Study Galaxy** — a 3D knowledge map (`galaxy.html`) that visualizes your real subjects and progress as orbiting planets.
- 🤖 **AI Tutor** — ask questions and get step-by-step help, with offline arithmetic and study tips built in.

---

## 🤖 Connecting the AI Tutor

StudyOS works fully offline (arithmetic, study tips, all non-AI features). For full AI answers, connect a provider in **Settings → Connect AI**:

| Provider | Works in browser? | Notes |
|----------|-------------------|-------|
| **Ollama** (local) | ✅ Recommended | Free, private, no key. Start it with `OLLAMA_ORIGINS=* ollama serve` so the browser is allowed to connect, then `ollama pull llama3.1`. |
| **OpenAI-compatible** | ✅ Yes | OpenAI, OpenRouter, Groq, etc. Enter key + base URL + model. |
| **NVIDIA NIM** | ⚠️ Needs a proxy | NVIDIA's cloud endpoint sends no CORS headers, so browsers block direct calls. Use it only via your own proxy (set the proxy URL as the OpenAI-compatible base URL). |

> **Why can't NIM be called directly?** Browser security (CORS) blocks cross-site API calls unless the provider explicitly allows them. OpenAI and Anthropic do; NVIDIA's `integrate.api.nvidia.com` currently does not. This is a provider limitation, not a StudyOS bug.

All keys and data are stored only in your browser's `localStorage` — nothing leaves your device.

---

## 🚀 Get Started

```bash
# 1. Clone
git clone https://github.com/A2ROYAL/StudyOS.git

# 2. Open index.html in any modern browser. That's it.
```

> **Tip:** For the most reliable AI experience, serve it over http (`python -m http.server`) and use Ollama or an OpenAI-compatible provider.

---

## 🛠️ Tech Stack

| Layer | Tech |
|-------|------|
| Frontend | Vanilla HTML + CSS + JS (zero dependencies) |
| 3D Galaxy | Three.js (r128) |
| AI | Ollama / OpenAI-compatible / NVIDIA NIM (via proxy) |
| Storage | Browser `localStorage` — all data stays on your device |
| Backend | None |

---

## 📄 License

MIT — free for personal and commercial use. ⭐ the repo if it helps you study!

*Built with 💜 for students everywhere.*
