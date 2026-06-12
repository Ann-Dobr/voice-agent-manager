# 🤖 Voice Agent Manager

Telegram bot for managing ElevenLabs voice agents — create agents, update prompts, greetings and knowledge base via text or voice messages.

## 📋 What it does

User manages voice agents through a Telegram bot interface:
- Creates new agents with custom names
- Updates agent prompts, greetings and knowledge base
- All changes are saved to MySQL database and synced with ElevenLabs API
- Supports both text input and **voice messages** (transcribed via Whisper API)

## 🛠 Tech Stack

- **n8n** — workflow automation
- **Telegram Bot API** — user interface with inline keyboards
- **OpenAI GPT-4o** — AI dispatcher, interprets user commands
- **OpenAI Whisper** — voice message transcription
- **MySQL** — agent data storage
- **ElevenLabs API** — voice agent configuration
- **JavaScript** — data processing logic

## 📊 Architecture

<img width="1546" height="646" alt="image" src="https://github.com/user-attachments/assets/0a0b04e3-5d71-4a61-9f19-950fcb7bcfeb" />

## ⚙️ Key Features

- AI agent interprets free-form user input and maps it to structured commands
- Voice messages automatically transcribed and processed as text
- Memory context window maintains conversation state across multiple steps
- Inline keyboard navigation for agent selection and settings
- Graceful handling of empty agent list with user-friendly prompts

## 📁 Files

- [`workflow.json`](workflow.json) — n8n workflow export (import directly into your n8n instance)

## ⚙️ Setup Requirements

- n8n instance (self-hosted)
- Telegram Bot token
- OpenAI API key
- MySQL database
- ElevenLabs API key
