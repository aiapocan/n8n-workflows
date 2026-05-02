# n8n Automation Workflows

**22 production-grade automation workflows for AI agents, lead generation, customer support, and business operations.**

These are real workflows built and operated in production — not templates or tutorials. Each one solves a specific business problem.

> Credentials and environment-specific values have been replaced with placeholders. Configure your own n8n credentials to run these workflows.

---

## Why these workflows exist

Manual business operations don't scale. These workflows automate the work that used to require humans sitting at a screen — qualifying leads, responding to customers, syncing data, generating reports — and run them 24/7 without intervention.

---

## Workflow catalog

### 🤖 Agentic AI & Bots

| Workflow | What it does |
|----------|-------------|
| `Tahayyul Bot - WhatsApp nn.json` | Production WhatsApp AI support bot — receives messages, classifies intent, generates responses with LLM, sends reply |
| `Tahayyul Bot - Telegram.json` | Same bot architecture deployed on Telegram |
| `Tahayyul Bot - website.json` | Website chat integration version |
| `Tahayyul Bot - WhatsApp copy.json` | A/B variant of the WhatsApp bot |
| `Tahayyul Bot - test.json` | Staging/test environment version |
| `Tahayyul Bot - WhatsApp old.json` | Previous version — archived for reference |
| `Ads whatsapp bot.json` | WhatsApp bot wired to paid ad campaign leads |
| `Build your first AI agent.json` | Clean starter: LLM agent with tool use (weather API example) |
| `Lead Agent.json` | Autonomous agent for lead qualification and routing |

### 📈 Lead Generation

| Workflow | What it does |
|----------|-------------|
| `Lead Generation V2.1.json` | Current pipeline — scrape, enrich, score, push to CRM |
| `Lead Generatıon V1.4 Nov.json` | Nov 2024 iteration |
| `Lead Generatıon V1.3.json` | V1.3 |
| `Lead Generatıon V1.2.json` | V1.2 |
| `Lead Generatıon V1.1.json` | V1.1 — initial version |
| `Generate Leads with Google Maps.json` | Google Maps Places API → extract businesses → enrich → output |

### 🗂️ Operations & CRM

| Workflow | What it does |
|----------|-------------|
| `Daily Client Handling - Master.json` | Daily ops: processes incoming records, routes by status, updates CRM |
| `Price sheet update.json` | Syncs pricing data across channels automatically |
| `Workflow logic.json` | Shared logic layer reused across multiple workflows |

### 🧠 RAG & Knowledge Systems

| Workflow | What it does |
|----------|-------------|
| `Rag_app.json` | Full RAG pipeline: ingest → embed → store → retrieve → answer |
| `RAG data  .json` | Data preparation and chunking workflow for the RAG system |

### 📚 Reference

| Workflow | What it does |
|----------|-------------|
| `Expressions.json` | n8n expression syntax patterns and examples |
| `JSON basics.json` | JSON transformation and manipulation patterns |

---

## How to import

1. Open your n8n instance
2. **Workflows → Import from file**
3. Select any `.json` from the `workflows/` folder
4. Set up required credentials (OpenAI, WhatsApp Business API, Google Maps, Pinecone, etc.)
5. Replace placeholders (`YOUR_WHATSAPP_PHONE_NUMBER_ID`, etc.) with your config
6. Activate and test

---

## Stack used across these workflows

```
Orchestration    n8n
AI / LLMs        OpenAI GPT-4 · Anthropic Claude · LangChain nodes
Messaging        WhatsApp Business API (Meta) · Telegram Bot API
Lead data        Google Maps Places API · SerpAPI
Vector store     Pinecone
Documents        Google Drive
Notifications    SMTP / Gmail
```

---

## Design principles

- **Error branches on every critical node** — failures route to notification, not silent drops
- **Idempotent design** — re-running a workflow doesn't create duplicate records
- **Versioned iteration** — V1.1 → V2.1 shows how workflows evolve with production feedback
- **Separation of concerns** — shared logic extracted into reusable sub-workflows

---

## License

Professional work shared for portfolio purposes. All rights reserved.
