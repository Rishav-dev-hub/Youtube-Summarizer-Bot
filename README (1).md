# 🤖 YouTube Summarizer Telegram Bot

An AI-powered Telegram bot that automatically summarizes any YouTube video in 5 bullet points — built with n8n, Groq AI, and Supadata.

> Send any YouTube link → Get a clean English summary in under 15 seconds.

---

## 🎬 Demo

![Bot Demo](https://img.shields.io/badge/Status-Live-brightgreen)
![Built With](https://img.shields.io/badge/Built%20With-n8n-orange)
![AI](https://img.shields.io/badge/AI-Groq%20LLaMA%203-blue)
![Platform](https://img.shields.io/badge/Platform-Telegram-2CA5E0)

**How it works:**

```
You (Telegram) → Send YouTube link
      ↓
Bot extracts Video ID
      ↓
Fetches transcript via Supadata API
      ↓
Summarizes with Groq AI (LLaMA 3.1)
      ↓
Sends 5-point English summary back to you
```

---

## ✨ Features

- Send any YouTube URL to the bot and get an instant AI summary
- Works for any language video — always responds in English
- 5 clean bullet points + 1-line description of the video
- Fully automated — runs 24/7 with no manual intervention
- Built entirely without writing a backend server

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| [n8n](https://n8n.io) | Workflow automation (no-code) |
| [Telegram Bot API](https://core.telegram.org/bots) | User interface |
| [Supadata API](https://supadata.ai) | YouTube transcript fetching |
| [Groq API](https://groq.com) | AI summarization (LLaMA 3.1 8B) |
| JavaScript | Video ID extraction logic |

---

## 🔧 How to Set Up Yourself

### Prerequisites
- n8n account (free at [n8n.io](https://n8n.io))
- Telegram account
- Supadata API key (free at [supadata.ai](https://supadata.ai))
- Groq API key (free at [console.groq.com](https://console.groq.com))

### Step 1 — Create your Telegram bot
1. Open Telegram → search `@BotFather`
2. Send `/newbot` and follow the steps
3. Copy your bot token

### Step 2 — Import the workflow
1. Download `workflow.json` from this repo
2. Open n8n → click **"Import workflow"**
3. Upload the file

### Step 3 — Add your credentials
| Node | Credential Needed |
|------|------------------|
| Telegram Trigger | Bot Token from BotFather |
| Supadata HTTP Request | `x-api-key` header |
| Groq HTTP Request | `Authorization: Bearer <key>` header |

### Step 4 — Publish and test
1. Click **Publish** in n8n
2. Send a YouTube link to your bot
3. Get your summary in ~15 seconds!

---

## 📁 Project Structure

```
youtube-summarizer-bot/
│
├── workflow.json        # n8n workflow export (import this)
├── README.md            # This file
└── screenshots/         # Demo screenshots
    ├── telegram-demo.png
    └── n8n-workflow.png
```

---

## 📸 Workflow Screenshot

> Add a screenshot of your n8n canvas here (Export → take a screenshot → upload to screenshots/ folder)

---

## 🚀 Future Improvements

- [ ] Save all summaries to Google Sheets
- [ ] Add `/history` command to view past summaries
- [ ] Handle videos with no transcript gracefully
- [ ] Support summarizing YouTube playlists
- [ ] Add language selection option

---

## 💡 What I Learned

- How to build automation workflows using n8n
- Integrating multiple APIs (Telegram, Supadata, Groq) in a single pipeline
- Handling API errors and edge cases in no-code tools
- Deploying and publishing live automation workflows

---

## 👨‍💻 Author

**Rishav** — BTech Student  
Built as a personal automation project to learn n8n and AI APIs.

[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com/Rishav504)

---

## 📄 License

MIT License — feel free to use and modify this project.
