<div align="center">

<img src="https://img.shields.io/badge/Gmail%20AI%20Agent-Auto%20Reply%20with%20Gemini-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail AI Agent Banner" />

# Gmail Auto-Reply AI Agent

**Reads your inbox. Understands context. Drafts the perfect reply — powered by Gemini 1.5 Flash.**

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org/)
[![Gemini](https://img.shields.io/badge/Gemini%201.5%20Flash-4285F4?style=flat-square&logo=google&logoColor=white)](https://deepmind.google/technologies/gemini/)
[![Gmail API](https://img.shields.io/badge/Gmail%20API-EA4335?style=flat-square&logo=gmail&logoColor=white)](https://developers.google.com/gmail/api)
[![OAuth 2.0](https://img.shields.io/badge/OAuth%202.0-Secured-34A853?style=flat-square&logo=google&logoColor=white)](https://oauth.net/2/)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

</div>

---

## Overview

This Python-based AI agent connects to your Gmail inbox via OAuth 2.0, reads incoming emails, and uses **Google Gemini 1.5 Flash** to generate polite, professional, context-aware replies — automatically. Clean, modular, and built to be extended.

> **GitHub Description:** Python AI agent that reads Gmail inbox and uses Gemini 1.5 Flash to generate intelligent, context-aware email replies via Gmail API and OAuth 2.0.

---

## Demo

![Agent in Action](https://github.com/user-attachments/assets/699200a0-503f-4c9d-96da-42146b181e60)

---

## Features

| Feature | Description |
|---------|-------------|
| **Secure Auth** | Gmail access via OAuth 2.0 — no passwords stored |
| **Email Reading** | Automatically fetches and parses the latest inbox message |
| **AI Reply Generation** | Gemini 1.5 Flash drafts intelligent, context-aware responses |
| **Modular Codebase** | Clean structure — easy to customize and extend |
| **Extendable** | Ready for auto-send, batch replies, and workflow integrations |

---

## How It Works

```
Gmail Inbox
     │
     ▼  OAuth 2.0
Fetch Latest Email
(Gmail API)
     │
     ▼
Parse Email Content
(subject + body)
     │
     ▼
Send to Gemini 1.5 Flash
(google-generativeai SDK)
     │
     ▼
AI-Generated Reply
(printed to terminal / sendable)
```

---

## Tech Stack

| Component | Technology |
|-----------|-----------|
| **Language** | Python 3.x |
| **AI Model** | Gemini 1.5 Flash |
| **Email Access** | Gmail API (Google Cloud) |
| **Auth** | OAuth 2.0 (`google-auth-oauthlib`) |
| **AI SDK** | `google-generativeai` |

---

## Project Structure

```
EmailAnsweringAiAgent/
│
├── auth_gmail.py         # OAuth 2.0 authentication flow
├── read_email.py         # Fetch email + generate AI reply
├── credentials.json      # OAuth client credentials (not committed)
├── token.json            # Generated auth token (not committed)
├── requirements.txt      # Python dependencies
└── README.md
```

>  Never commit `credentials.json` or `token.json` to version control. Add them to `.gitignore`.

---

## Setup & Installation

### 1. Clone the Repository

```bash
git clone https://github.com/JustCodeIT199/EmailAnsweringAiAgent.git
cd EmailAnsweringAiAgent
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install google-auth google-auth-oauthlib google-api-python-client google-generativeai
```

### 3. Enable Gmail API on Google Cloud

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project
3. Enable the **Gmail API**
4. Configure the **OAuth Consent Screen**
5. Add your email under **Test Users**
6. Create an **OAuth Client ID** (Desktop type)
7. Download and save as `credentials.json` in the project root

### 4. Set Your Gemini API Key

```bash
# macOS / Linux
export GEMINI_API_KEY=your_api_key_here

# Windows (Command Prompt)
set GEMINI_API_KEY=your_api_key_here
```

> Get your Gemini API key from [Google AI Studio](https://aistudio.google.com/app/apikey).

### 5. Authenticate Gmail Access

```bash
python auth_gmail.py
```

A browser window will open for Gmail authorization. On success, a `token.json` file is generated for future sessions.

---

## Usage

### Read Latest Email & Generate AI Reply

```bash
python read_email.py
```

**What happens:**
1. Fetches your latest Gmail message
2. Passes the content to Gemini 1.5 Flash
3. Prints the AI-generated reply in the terminal

---

## Environment Variables

| Variable | Description |
|----------|-------------|
| `GEMINI_API_KEY` | Your Google Gemini API key |

---

## Roadmap

- [ ] Auto-send replies directly via Gmail API
- [ ] Batch processing — handle multiple unread emails
- [ ] LangChain integration for multi-step reasoning
- [ ] n8n / Zapier workflow automation support
- [ ] Filter emails by sender, subject, or label before replying
- [ ] Web UI for monitoring and managing AI replies

---

## Credits

Built with:
- [Google Gmail API](https://developers.google.com/gmail/api)
- [Google Gemini API](https://deepmind.google/technologies/gemini/)

---

## License

This project is open-source and available under the [MIT License](LICENSE).

---
