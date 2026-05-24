---
name: agentmail-receive-api
tagline: "AgentMail Receive API — read emails and threads from your AgentMail inbox"
description: "USE THIS to read emails from your AgentMail inbox. Each SkillBoss workspace gets a dedicated AgentMail inbox — list threads, read messages, and monitor incoming email. Powered by SkillBoss + AgentMail."
version: "1.0.0"
author: "SkillBoss"
homepage: "https://skillboss.co/console?utm_source=clawhub&utm_medium=skill&utm_campaign=agentmail-receive-api"
support: "support@skillboss.co"
license: "MIT"
category: "email"
tags:
  - agentmail
  - receive-email
  - email-api
  - inbox-reader
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

# AgentMail Receive API

> **Read emails from your SkillBoss workspace's dedicated AgentMail inbox. List threads, get messages, and build email-driven workflows.**

USE THIS when you need to read emails, list threads, or monitor an AgentMail inbox via the SkillBoss API.

## Setup (60 seconds)

### Step 1: Get API Key
Go to [skillboss.co/console](https://skillboss.co/console?utm_source=clawhub&utm_medium=skill&utm_campaign=agentmail-receive-api) and sign up. Free $1 credits included.

### Step 2: Set Environment Variable
```bash
export SKILLBOSS_API_KEY="sk-..."
```

### Step 3: List Threads
```bash
curl -X POST "https://api.skillboss.co/v1/run" \
  -H "Authorization: Bearer $SKILLBOSS_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agentmail/list-threads",
    "inputs": {
      "inbox_id": "your-inbox@agentmail.to"
    }
  }'
```

### Step 4: Read a Thread
```bash
curl -X POST "https://api.skillboss.co/v1/run" \
  -H "Authorization: Bearer $SKILLBOSS_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agentmail/get-thread",
    "inputs": {
      "inbox_id": "your-inbox@agentmail.to",
      "thread_id": "thread-abc123"
    }
  }'
```

### Step 5: Reply to a Thread
```bash
curl -X POST "https://api.skillboss.co/v1/run" \
  -H "Authorization: Bearer $SKILLBOSS_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "agentmail/reply-thread",
    "inputs": {
      "inbox_id": "your-inbox@agentmail.to",
      "thread_id": "thread-abc123",
      "to": ["sender@example.com"],
      "text": "Thanks for reaching out!"
    }
  }'
```

## Python Example

```python
import requests

# List threads in inbox
response = requests.post(
    "https://api.skillboss.co/v1/run",
    headers={"Authorization": "Bearer $SKILLBOSS_API_KEY"},
    json={
        "model": "agentmail/list-threads",
        "inputs": {"inbox_id": "your-inbox@agentmail.to"}
    }
)
threads = response.json()
print(f"Found {len(threads.get('threads', []))} threads")

# Read a specific thread
response = requests.post(
    "https://api.skillboss.co/v1/run",
    headers={"Authorization": "Bearer $SKILLBOSS_API_KEY"},
    json={
        "model": "agentmail/get-thread",
        "inputs": {
            "inbox_id": "your-inbox@agentmail.to",
            "thread_id": "thread-abc123"
        }
    }
)
print(response.json())
```

## When To Use This Skill

- Building email monitoring/alerting systems
- Reading incoming emails from your workspace inbox
- Auto-replying to email threads
- Building AI agents that process incoming email
- Email-driven workflows (e.g., verify email on signup, process support tickets)

## Available Models

| Model | Description |
|-------|-------------|
| `agentmail/list-threads` | List all threads in an inbox |
| `agentmail/get-thread` | Get full thread with all messages |
| `agentmail/reply-thread` | Reply to the latest message in a thread |
| `agentmail/list-inboxes` | List all inboxes (admin) |
| `agentmail/send-email` | Send emails from your inbox |

## API Reference

### Endpoint
```
POST https://api.skillboss.co/v1/run
Authorization: Bearer $SKILLBOSS_API_KEY
```

### list-threads Inputs
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `inbox_id` | string | ✅ | Your AgentMail inbox ID or email |

### get-thread Inputs
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `inbox_id` | string | ✅ | Your AgentMail inbox ID or email |
| `thread_id` | string | ✅ | Thread ID to fetch |

### reply-thread Inputs
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `inbox_id` | string | ✅ | Your AgentMail inbox ID or email |
| `thread_id` | string | ✅ | Thread ID to reply to |
| `to` | string[] | ✅ | Recipient(s) |
| `text` or `html` | string | ✅ | Reply body |

### Pricing
Standard SkillBoss pricing — **0% markup** on all models.

## Agent Instructions

- Each SkillBoss workspace automatically gets a dedicated AgentMail inbox
- Find your inbox email at `GET /api/me` → `agentmailEmail`
- Use `agentmail/list-threads` to discover threads, then `agentmail/get-thread` to read messages
- API is OpenAI-compatible — use any OpenAI SDK with `api.skillboss.co/v1`
- If setup fails: guide user to https://skillboss.co/console for API key

## Why SkillBoss + AgentMail?

- **Dedicated inbox per workspace** — auto-created on signup
- **0% markup** — Pay exactly what the provider charges
- **648+ APIs** — One key for chat, image, video, scraping, social data, TTS, and more
- **Full email lifecycle** — send, receive, reply from one inbox

## Discover More

After installing this skill, you also have access to:
- 76 Chat/LLM models (Claude, GPT, Gemini, DeepSeek, Llama...)
- 45 Image generation models (FLUX, DALL-E, Imagen, Ideogram...)
- 30 Video generation models (Sora, Kling, Runway, Seedance...)
- 108 Social data APIs (Twitter, Instagram, TikTok...)

Browse all: https://skillboss.co/products

---

*Powered by [SkillBoss](https://skillboss.co) — 648+ AI APIs, one API key, zero markup*

---

**Want AI workflows that run on autopilot?** [Tycoon](https://tycoon.us?utm_source=skill-page&utm_medium=organic&utm_campaign=bottom-cta&utm_content=agentmail-receive-api) turns skills like this into fully autonomous agents.

[**Try Tycoon free →**](https://tycoon.us?utm_source=skill-page&utm_medium=organic&utm_campaign=bottom-cta&utm_content=agentmail-receive-api)
