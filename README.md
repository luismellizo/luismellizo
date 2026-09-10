# Luis Mellizo

**I build AI-powered products end to end** — copilots, agents and automation that run in production, not in demos.

Founder @ [Prosite](https://prosite.com.co) · Colombia 🇨🇴 · open to remote roles (LATAM / US timezones) and to relocation.

---

## Systems running in production

Three of them ship with a **public code snapshot** — curated, documented, and honest about what was left out.

| | What it does | Live | Code |
|---|---|---|---|
| **Propaga** | One video in, five social networks out. AI writes the copy. | [propaga.lat](https://propaga.lat) | [propaga-showcase](https://github.com/luismellizo/propaga-showcase) |
| **Dilo** | Restaurants sell over WhatsApp; a bot takes the order, the kitchen sees it live. | [dilo.lat](https://dilo.lat) | [dilo-showcase](https://github.com/luismellizo/dilo-showcase) |


### Propaga — publish once, land everywhere
Upload a video (URL or file). Celery downloads it with yt-dlp, transcribes the audio with Whisper, and Gemini writes the title, description and hashtags in the personality you configured. You approve — then it publishes to **Facebook, Instagram, YouTube, X and TikTok**, each with its own upload protocol.

*The part nobody expects:* X's media endpoint still requires **OAuth 1.0a**, Instagram won't accept the file at all (it downloads the video from a public URL and makes you poll), and a `.mp4` from the internet may carry AV1 inside — which X rejects.

`Django` `Celery` `PostgreSQL` `Redis` `HTMX` `ffmpeg` `Gemini` `Groq`

### Dilo — conversational commerce on WhatsApp
Each merchant connects their own WhatsApp number through Meta Embedded Signup. An AI bot shows the menu, builds the order, takes payment, verifies the transfer receipt and drops it on a real-time Kanban board in the kitchen. Multi-tenant with per-store encrypted credentials and queryset-level isolation.

`Django` `DRF` `Channels` `Celery` `React 19` `WhatsApp Cloud API`


---

## Also building

**[Modela](https://github.com/luismellizo/modela)** — architectural 3D editor with an AI copilot that operates the CAD scene from text, images and your current selection. Built on [Pascal Editor](https://github.com/pascalorg/editor).

**Client work** — Kakay (Next.js 16 + Vite on Cloudflare Workers, Drizzle ORM) · B-ENG (landing for a civil engineering studio). Private repositories; happy to walk through either one.

---

## Stack

**AI** LLM agents & tool use · OpenRouter · Anthropic / OpenAI / Gemini APIs · RAG · STT/TTS
**Backend** Python · Django · DRF · Celery · Django Channels · PostgreSQL · Redis
**Frontend** TypeScript · React · Next.js · HTMX · Tailwind · Three.js
**Infra** Docker · Nginx · Coolify · Cloudflare Workers · Supabase · Linux (Arch)
**Integrations** WhatsApp Cloud API · Meta Graph · YouTube Data API · Wompi · Nequi · AWS SES

---

## How I work

I care about the failure paths. A third-party API will go down mid-pipeline, a token will expire between the UI saying "connected" and the worker trying to use it, and a user will close the tab halfway through. The interesting part of a system is what it does then — degrade, report honestly, and keep the work that already succeeded.

The public snapshots above document that reasoning: not just what the code does, but what broke first and why it's written this way.

---

## Reach me

🌐 [prosite.com.co](https://prosite.com.co) · 📧 luismellizoo@gmail.com
📍 Bogotá, Colombia · GMT-5 · open to relocation
