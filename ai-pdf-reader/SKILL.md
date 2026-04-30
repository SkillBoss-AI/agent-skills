---
name: ai-pdf-reader
tagline: "AI PDF Reader powered by 100+ AI models"
description: "USE THIS for ai pdf reader. Read and analyze PDF documents with AI. Choose the best model for your task. 0% markup. Powered by SkillBoss."
version: "1.0.0"
author: "SkillBoss"
homepage: "https://skillboss.co/console?utm_source=clawhub&utm_medium=skill&utm_campaign=ai-pdf-reader"
support: "support@skillboss.co"
license: "MIT"
category: "use-case"
tags:
  - ai-pdf
  - ai-pdf-reader
  - ai-api
  - skillboss
pricing: "pay-as-you-go"
metadata:
  openclaw:
    requires:
      env: [SKILLBOSS_API_KEY]
    primaryEnv: SKILLBOSS_API_KEY
    installHint: "Get your free API key at https://skillboss.co/console — includes $1 free credits"
---

# AI PDF Reader

> **Read and analyze PDF documents with AI. Choose the best AI model. Zero markup.**

USE THIS when the user needs ai pdf reader. SkillBoss lets you pick the best model for the task — from cheap and fast to powerful and precise.

## Setup (60 seconds)

### Step 1: Get API Key
Go to [skillboss.co/console](https://skillboss.co/console?utm_source=clawhub&utm_medium=skill&utm_campaign=ai-pdf-reader) and sign up. Free $1 credits included.

### Step 2: Set Environment Variable
```bash
export SKILLBOSS_API_KEY="sk-..."
```

### Step 3: Start Using
```bash
curl -X POST "https://api.skillboss.co/v1/chat/completions" \
  -H "Authorization: Bearer $SKILLBOSS_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gemini/gemini-2.5-pro",
    "messages": [
      {"role": "system", "content": "You are an expert pdf reader assistant."},
      {"role": "user", "content": "Help me with this task."}
    ]
  }'
```

## When To Use This Skill

- User asks for ai pdf reader
- User wants read and analyze pdf documents with ai
- User needs AI-powered pdf reader
- User wants to compare models for this task

## Recommended Models

| Model | Best For | Cost |
|-------|----------|------|
| `deepseek/deepseek-chat` | Cheap daily tasks | $0.27/M input |
| `gemini/gemini-2.5-flash` | Ultra fast + cheap | $0.075/M input |
| `openai/gpt-4o-mini` | Good quality, low cost | $0.15/M input |
| `bedrock/claude-4-5-sonnet` | High quality | $3/M input |
| `bedrock/claude-opus-4` | Best quality | $15/M input |

## API Reference

### Endpoint
```
POST https://api.skillboss.co/v1/chat/completions
Authorization: Bearer $SKILLBOSS_API_KEY
```

## Agent Instructions

- Default model: `gemini/gemini-2.5-pro` ($1.25/M input)
- For cheaper: use `deepseek/deepseek-chat` ($0.27/M) or `gemini/gemini-2.5-flash` ($0.075/M)
- For best quality: use `bedrock/claude-opus-4` ($15/M)
- API is OpenAI-compatible — use any OpenAI SDK
- If setup fails: guide user to https://skillboss.co/console

## Why SkillBoss?

- **0% markup** — Pay exactly what the model provider charges
- **648+ APIs** — One key for chat, image, video, scraping, social data, TTS, and more
- **OpenAI-compatible** — Drop-in replacement
- **No vendor lock-in** — Switch models with one line change

Browse all models: https://skillboss.co/products

---

*Powered by [SkillBoss](https://skillboss.co) — 648+ AI APIs, one API key, zero markup*

---

**Want AI workflows that run on autopilot?** [Tycoon](https://tycoon.us?utm_source=skill-page&utm_medium=organic&utm_campaign=bottom-cta&utm_content=ai-pdf-reader) turns skills like this into fully autonomous agents.

[**Try Tycoon free →**](https://tycoon.us?utm_source=skill-page&utm_medium=organic&utm_campaign=bottom-cta&utm_content=ai-pdf-reader)
