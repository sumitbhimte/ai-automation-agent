# AI Assistant via Telegram with n8n Automation


[![n8n](https://img.shields.io/badge/built%20with-n8n-2087c3)](https://n8n.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)


**AI Assistant** is an intelligent virtual assistant powered by **n8n** and integrated with **Telegram**. It automates tasks such as answering queries, handling emails, scheduling meetings, and analyzing images—all from your Telegram chat.

---

## Key Features

- **Text & Voice Interaction:** Chat naturally using text or voice commands.
- **Email Automation:** Read, summarize, and send emails automatically.
- **Calendar Scheduling:** Manage Google Calendar events and check availability.
- **Voice Recognition & Response:** Understands voice commands and replies in text or audio.
- **Image Analysis:** Describes images using OpenAI GPT-4o.
- **Web Search:** Retrieves real-time information from the web.

---

## Tech Stack

| Component                | Technology/Service                |
|--------------------------|-----------------------------------|
| Workflow Automation      | n8n                               |
| Messaging Integration    | Telegram Bot API                  |
| AI Models & APIs         | Google Gemini, OpenAI GPT-4o      |
| Google Workspace         | Gmail API, Google Calendar API    |
| Web Data Retrieval       | SERP API                          |
| AI Agent Framework       | LangChain                         |

### Prerequisites

Before setting up, ensure you have:

- n8n installed ([installation guide](https://docs.n8n.io/hosting/))
- Telegram Bot Token (created via [BotFather](https://core.telegram.org/bots#creating-a-new-bot))
- OpenAI API Key ([generate here](https://platform.openai.com/api-keys))
- Google Cloud Credentials (for Gmail, Calendar, and Gemini APIs)
- SERP API Key ([obtain here](https://serpapi.com/))

---

## Setup Instructions for AI Assistant

Follow these steps to import and activate the workflow:

### Step 1: Import Workflow into n8n

- Open your n8n application.
- Click **"Import"** and select the provided `ai-agent.json`.
- Configure all nodes with your API credentials and correct paths.


---

### Step 2: Activate Workflow

- Click **"Execute Workflow"** to test or activate it to continuously listen for Telegram messages.

---
## Workflow Overview

The **AI Assistant** workflow operates as follows:

1. **Telegram Trigger:** Listens for incoming messages (text, voice, image).
2. **Message Routing:** Determines message type and routes accordingly.
3. **AI Processing:** Uses Google Gemini, OpenAI GPT-4o, and LangChain for intelligent responses.
4. **Voice & Image Handling:** Converts voice to text, analyzes images, and generates responses.
5. **Email & Calendar Automation:** Reads, summarizes, and sends emails; manages Google Calendar events.
6. **Web Search:** Retrieves real-time information using SERP API.
7. **Response Delivery:** Sends responses back via Telegram (text/audio).
