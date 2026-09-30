# AI Lead Capture Chatbot

An AI-powered chatbot that captures and qualifies leads from website visitors and automatically syncs them to Pipedrive CRM.

🔴 **Live on:** [debestesalespodcast.nl](https://debestesalespodcast.nl)

## What it does

- Chats with website visitors in Dutch 24/7
- Qualifies leads through natural conversation
- Collects name, phone, email and company
- Validates email format before accepting
- Automatically creates Organization + Person + Lead in Pipedrive
- Sends email notification with conversation summary
- Escalates to human support when needed

## Stack

- **n8n** — workflow orchestration
- **OpenAI GPT-4o-mini** — conversational AI
- **Pipedrive API** — CRM integration
- **Gmail API** — email notifications
- **Google Sheets** — conversation logging
- **Custom chat widget** — embedded on client website

## Architecture

Website visitor
→ Chat Widget (embedded)
→ n8n Chat Trigger
→ AI Agent (GPT-4o-mini)
→ Code node (extract JSON + clean output)
→ IF complete?
→ Create Organization + Person + Lead (Pipedrive)
→ Send email notification (Gmail)

## Infrastructure

- Hosted on Hetzner VPS (Ubuntu)
- nginx reverse proxy
- SSL via Let's Encrypt
- Google Cloud OAuth for API access
