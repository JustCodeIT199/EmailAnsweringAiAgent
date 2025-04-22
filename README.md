# EmailAnsweringAiAgent
# Gmail Auto-Reply Agent using Gemini 1.5 Flash

This project is a Python-based AI agent that reads your Gmail inbox, uses Google's Gemini 1.5 Flash model to understand the email content, and generates a polite, professional reply. It leverages the Gmail API for reading emails and the Gemini API for generating smart responses.

---

## ✨ Features

- Connects securely to your Gmail inbox using OAuth 2.0
- Automatically reads the latest email
- Uses Gemini 1.5 Flash to generate intelligent, context-aware replies
- (Optional) Extendable to send replies via Gmail
- Clean, modular Python code — easy to customize

---

## 🚀 Setup Instructions

### 1. Clone the Repo

```bash
git clone https://github.com/your-username/gmail-gemini-agent.git
cd gmail-gemini-agent
```
### 2. Install Dependencies
```
pip install -r requirements.txt
```
Or install manually:
```
pip install google-auth google-auth-oauthlib google-api-python-client google-generativeai
```
### 3. Enable Gmail API
Go to Google Cloud Console

Create a new project

Enable Gmail API

Go to OAuth Consent Screen and configure it

Add your email under Test Users

Create OAuth Client ID (Desktop) and download credentials.json

### 4. Authenticate Gmail Access
```
python auth_gmail.py
```
This will open a browser window for you to log in and authorize access. It will generate a token.json file for future use.

## 🔁 Usage
### 1. Read Latest Email and Generate AI Reply
```
python read_email.py
```
This script will:

Fetch your latest Gmail message

Pass the content to Gemini 1.5 Flash

Print the AI-generated response in your terminal

## 🔐 Environment Variables
Set your Gemini API key before running the script (or hardcode it safely in your code):
```
export GEMINI_API_KEY=your_api_key_here
```
## 🧠 Model Used
Model: gemini-1.5-flash

API: google-generativeai SDK

Supports real-time AI-generated responses

## ✅ Coming Soon
Auto-send replies via Gmail

Batch reply support

Langchain or n8n integration

## 📄 License
This project is licensed under the MIT License. See LICENSE for more details.

## 🙌 Credits
Built with:

Google Gmail API

Google Gemini API
