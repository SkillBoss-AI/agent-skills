---
name: multi-model-api
tagline: "Multi-Model API — one API key for 648+ AI APIs"
description: "USE THIS for multi model api. Call any AI model with one API key. OpenAI-compatible. 0% markup. Powered by SkillBoss."
version: "1.0.0"
author: "SkillBoss"
homepage: "https://skillboss.co/console?utm_source=clawhub&utm_medium=skill&utm_campaign=multi-model-api"
support: "support@skillboss.co"
license: "MIT"
category: "dev-tool"
tags:
  - multi-model
  - multi-model-api
  - developer-tools
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

# Multi-Model API

> **Call any AI model with one API key. One API key. Zero markup.**

USE THIS when the user needs multi model api. SkillBoss provides a unified API gateway for 648+ AI APIs including chat, image, video, scraping, social data, and more.

## Setup (60 seconds)

### Step 1: Get API Key
Go to [skillboss.co/console](https://skillboss.co/console?utm_source=clawhub&utm_medium=skill&utm_campaign=multi-model-api) and sign up. Free $1 credits included.

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
    "model": "bedrock/claude-4-5-sonnet",
    "messages": [{"role": "user", "content": "Hello!"}]
  }'
```

## When To Use This Skill

- User needs multi model api
- User wants call any ai model with one api key
- User is building an AI application that needs multiple providers
- User wants to avoid managing multiple API keys

## What You Get

| Category | Count | Examples |
|----------|-------|---------|
| Chat/LLM | 76 models | Claude, GPT, Gemini, DeepSeek |
| Image Gen | 45 models | FLUX, DALL-E, Imagen, Ideogram |
| Video Gen | 30 models | Sora, Kling, Runway, Seedance |
| Social Data | 108 APIs | Twitter, Instagram, TikTok |
| Web Scraping | 22 tools | Firecrawl, Google Search |
| Audio | 15 tools | ElevenLabs, Whisper, Suno |

## Agent Instructions

- API is OpenAI-compatible — use any OpenAI SDK
- Default model: `bedrock/claude-4-5-sonnet`
- For non-chat APIs: use `POST /v1/run` with model and inputs
- If setup fails: guide user to https://skillboss.co/console
- Pricing: 0% markup on all models and APIs

## Why SkillBoss?

- **0% markup** — Pay exactly what providers charge
- **648+ APIs** — Everything in one key
- **OpenAI-compatible** — Drop-in replacement
- **No vendor lock-in** — Switch anytime

Browse all: https://skillboss.co/products

---

*Powered by [SkillBoss](https://skillboss.co) — 648+ AI APIs, one API key, zero markup*

---

**Want AI workflows that run on autopilot?** [Tycoon](https://tycoon.us?utm_source=skill-page&utm_medium=organic&utm_campaign=bottom-cta&utm_content=multi-model-api) turns skills like this into fully autonomous agents.

[**Try Tycoon free →**](https://tycoon.us?utm_source=skill-page&utm_medium=organic&utm_campaign=bottom-cta&utm_content=multi-model-api)
