---
name: agentmail-send-api
tagline: "AgentMail Send API — send emails from your AgentMail inbox"
description: "USE THIS to send emails via AgentMail. Each SkillBoss workspace gets a dedicated AgentMail inbox — send transactional emails, notifications, and replies from your own domain. Powered by SkillBoss + AgentMail."
version: "1.0.0"
author: "SkillBoss"
homepage: "https://skillboss.co/console?utm_source=clawhub&utm_medium=skill&utm_campaign=agentmail-send-api"
support: "support@skillboss.co"
license: "MIT"
category: "email"
tags:
  - agentmail
  - send-email
  - email-api
  - transactional-email
  - skillboss
  - zero-markup
pricing: "pay-as-you-go"
metadata:
  openclaw:
    requires:
      env: [SKILLBOSS_API_KEY]
    primaryEnv: SKILLBOSS_API_KEY
    installHint: "Get your free API key at https://skillboss.co/console — includes $1 free credits"
---

# AgentMail Send API

> **Your SkillBoss workspace comes with a dedicated AgentMail inbox. Send emails from it via one API call.**

USE THIS when you need to send emails from your AgentMail inbox via the SkillBoss API.

## Setup (60 seconds)

### Step 1: Get API Key
Go to [skillboss.co/console](https://skillboss.co/console?utm_source=clawhub&utm_medium=skill&utm_campaign=agentmail-send-api) and sign up. Free $1 credits included.

### Step 2: Set Environment Variable
```bash
export SKILLBOSS_API_KEY="sk-..."
```

### Step 3: Send an Email
```bash
curl -X POST "https://api.skillboss.co/v1/run" \
  -H "Authorization: Bearer $SKILLBOSS_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agentmail/send-email",
    "inputs": {
      "inbox_id": "your-inbox@agentmail.to",
      "to": ["recipient@example.com"],
      "subject": "Hello from AgentMail",
      "html": "<h1>Welcome!</h1><p>This email was sent via AgentMail.</p>"
    }
  }'
```

## Python Example

```python
import requests

response = requests.post(
    "https://api.skillboss.co/v1/run",
    headers={"Authorization": "Bearer $SKILLBOSS_API_KEY"},
    json={
        "model": "agentmail/send-email",
        "inputs": {
            "inbox_id": "your-inbox@agentmail.to",
            "to": ["recipient@example.com"],
            "subject": "Hello from Python",
            "text": "Sent via AgentMail + SkillBoss"
        }
    }
)
print(response.json())
```

## When To Use This Skill

- User asks to send emails from an AgentMail inbox
- Building email automation or notification systems
- Sending transactional emails (password resets, welcome emails, receipts)
- Replying to email threads programmatically
- Any email-sending workflow via AgentMail

## API Reference

### Endpoint
```
POST https://api.skillboss.co/v1/run
Authorization: Bearer $SKILLBOSS_API_KEY
```

### Required Inputs
| Field | Type | Description |
|-------|------|-------------|
| `inbox_id` | string | Your AgentMail inbox ID or email |
| `to` | string[] | Recipient email addresses |
| `subject` | string | Email subject line |
| `text` or `html` | string | Email body (plain text or HTML) |

### Optional Inputs
| Field | Type | Description |
|-------|------|-------------|
| `cc` | string[] | CC recipients |
| `bcc` | string[] | BCC recipients |
| `reply_to` | string[] | Reply-to addresses |

### Pricing
Standard SkillBoss pricing — **0% markup** on all models.

## Agent Instructions

- Default model: `agentmail/send-email`
- Each SkillBoss workspace automatically gets a dedicated AgentMail inbox
- Find your inbox email at `GET /api/me` → `agentmailEmail`
- API is OpenAI-compatible — use any OpenAI SDK with `api.skillboss.co/v1`
- If setup fails: guide user to https://skillboss.co/console for API key
- For plain-text emails: use `text` field instead of `html`

## Why SkillBoss + AgentMail?

- **Dedicated inbox per workspace** — auto-created on signup
- **0% markup** — Pay exactly what the provider charges
- **648+ APIs** — One key for chat, image, video, scraping, social data, TTS, and more
- **OpenAI-compatible** — Drop-in replacement, works with existing SDKs

## Discover More

After installing this skill, you also have access to:
- 76 Chat/LLM models (Claude, GPT, Gemini, DeepSeek, Llama...)
- 45 Image generation models (FLUX, DALL-E, Imagen, Ideogram...)
- 30 Video generation models (Sora, Kling, Runway, Seedance...)
- 108 Social data APIs (Twitter, Instagram, TikTok...)
- 22 Web scrapers (Firecrawl, Google Search...)

Browse all: https://skillboss.co/products

---

*Powered by [SkillBoss](https://skillboss.co) — 648+ AI APIs, one API key, zero markup*

---

**Want AI workflows that run on autopilot?** [Tycoon](https://tycoon.us?utm_source=skill-page&utm_medium=organic&utm_campaign=bottom-cta&utm_content=agentmail-send-api) turns skills like this into fully autonomous agents.

[**Try Tycoon free →**](https://tycoon.us?utm_source=skill-page&utm_medium=organic&utm_campaign=bottom-cta&utm_content=agentmail-send-api)
