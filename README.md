# n8n Automation Workflows

**Production-grade n8n workflows for AI automation, lead generation, and customer support.**

Built and operated by [@aiapocan](https://github.com/aiapocan) — these are real workflows running (or recently run) in production at [Tasaahil](https://tasaahil.com) and Tahayyul Travel & Tourism.

> **Note:** Credential IDs and sensitive configuration values have been replaced with placeholders. You'll need to configure your own n8n credentials to use these workflows.

---

## Workflow catalog

### 🤖 AI Bots & Assistants

| File | Description |
|---|---|
| `Tahayyul Bot - WhatsApp nn.json` | WhatsApp customer support bot with AI responses — production version |
| `Tahayyul Bot - WhatsApp copy.json` | WhatsApp bot variant (A/B testing copy) |
| `Tahayyul Bot - WhatsApp old.json` | Earlier WhatsApp bot version (archived for reference) |
| `Tahayyul Bot - Telegram.json` | Telegram version of the Tahayyul support bot |
| `Tahayyul Bot - website.json` | Website chat integration |
| `Tahayyul Bot - test.json` | Test/staging version of the bot |
| `Ads whatsapp bot.json` | WhatsApp bot wired to paid ad campaigns |
| `Build your first AI agent.json` | Starter template: LLM agent with tool use |

### 📈 Lead Generation

| File | Description |
|---|---|
| `Lead Generation V2.1.json` | Current lead gen pipeline — enrichment + scoring + CRM push |
| `Lead Generatıon V1.4 Nov.json` | Nov 2024 version of the lead generation flow |
| `Lead Generatıon V1.3.json` | V1.3 — iterative improvement series |
| `Lead Generatıon V1.2.json` | V1.2 |
| `Lead Generatıon V1.1.json` | V1.1 — initial version |
| `Generate Leads with Google Maps.json` | Scrapes Google Maps Places API and enriches leads |
| `Lead Agent.json` | AI agent for autonomous lead qualification |

### 📋 Operations & CRM

| File | Description |
|---|---|
| `Daily Client Handling - Master.json` | Daily ops: processes, routes, and updates CRM records |
| `Price sheet update.json` | Automated pricing sheet sync across channels |
| `Workflow logic.json` | Core logic abstraction reused across workflows |

### 🧠 AI / RAG

| File | Description |
|---|---|
| `Rag_app.json` | Full RAG pipeline: document ingestion, embedding, retrieval + answer |
| `RAG data  .json` | Data preparation workflow for the RAG system |

### 📚 Reference / Learning

| File | Description |
|---|---|
| `Expressions.json` | n8n expression syntax examples and patterns |
| `JSON basics.json` | JSON manipulation and transformation patterns |

---

## How to import

1. Open your n8n instance
2. Go to **Workflows** → **Import from file**
3. Select any `.json` file from the `workflows/` folder
4. Configure the required credentials (OpenAI, WhatsApp Business API, Google Maps, Pinecone, etc.)
5. Update placeholder values (`YOUR_WHATSAPP_PHONE_NUMBER_ID`, etc.) with your actual config
6. Activate and test

---

## Tech stack used across these workflows

- **n8n** — orchestration platform
- **OpenAI / Anthropic** — LLM nodes for reasoning, classification, response generation
- **WhatsApp Business API (Meta)** — inbound/outbound messaging
- **Telegram Bot API** — messaging channel
- **Google Maps Places API** — lead discovery
- **SerpAPI** — search enrichment
- **Pinecone** — vector storage for RAG
- **Google Drive** — document source for RAG ingestion
- **SMTP / Gmail** — notification and report delivery

---

## What I learned

- **Production reliability in n8n** — error branches, retries, dead-letter queues, and monitoring hooks to keep bots running 24/7.
- **WhatsApp Business API edge cases** — message deduplication, template compliance, rate limiting, and webhook verification.
- **Cost-aware RAG design** — chunking strategy, embedding cache, and retrieval thresholds that reduce API spend.
- **Iterative workflow versioning** — maintaining parallel versions (V1.1 → V2.1) while keeping production stable.

---

## License

Personal/professional work. Shared for portfolio and learning purposes. All rights reserved.

---

*Based in Istanbul. Built between 2024 and 2025 while running ops at Tahayyul Travel & Tourism and Tasaahil.*
