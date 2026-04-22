# n8n Automation Portfolio

A collection of self-hosted n8n workflows demonstrating real-world automation patterns: multi-system integration, LLM orchestration, webhook-driven pipelines, and stateful conversational agents.

All workflows are deployed on a self-hosted n8n instance (Docker on a Hostinger VPS). Production code and credentials are not included. This repository contains architecture diagrams, redacted node-list screenshots, and pattern documentation.

---

## Projects

| # | Project | Domain | Key Patterns |
|---|---------|--------|--------------|
| 01 | [Conversational Lead-Capture & Booking](./01-conversational-lead-capture) | SMB / Lead Gen | RAG, chat memory, LLM-driven calendar booking, two-way SMS |
| 02 | [NFL Matchup Prediction Pipeline](./02-nfl-matchup-prediction) | Data Aggregation | Multi-source webhooks, LLM sentiment analysis, JSON normalization |
| 03 | [NFL Fantasy Lineup Optimizer](./03-nfl-fantasy-optimizer) | Decision Support | API orchestration, scheduled execution, LLM-driven recommendations |

---

## Technology Stack Across Projects

**Orchestration:** n8n (self-hosted, Docker)
**LLMs:** OpenAI (GPT models), Anthropic Claude, Google Gemini
**Databases:** PostgreSQL (chat memory, structured state)
**Messaging:** Twilio (SMS), Gmail (email delivery)
**Data Sources:** REST APIs, webhooks, HTTP nodes, web scraping (Apify)
**Scheduling:** Google Calendar, n8n cron triggers
**Infrastructure:** Docker on Hostinger VPS

---

## Engineering Practices Demonstrated

- **Structured LLM outputs.** All LLM calls use explicit JSON schemas so downstream nodes can reliably parse responses.
- **Error handling.** Failed branches, retry logic on API timeouts, and separate error outputs for upstream service hiccups.
- **State persistence.** PostgreSQL-backed chat memory with custom session keys, not in-memory or ephemeral storage.
- **Separation of concerns.** Workflows broken into discrete, testable flows connected by webhooks rather than monolithic single-canvas designs.
- **Rate-limit awareness.** Batched requests, throttling nodes, and backoff on third-party APIs.

---

## Repository Structure

```
n8n-automation-portfolio/
├── README.md                           (this file)
├── LICENSE
├── 01-conversational-lead-capture/
│   ├── README.md                       (project detail + architecture)
│   ├── diagrams/                       (Mermaid source + rendered diagrams)
│   └── screenshots/                    (redacted n8n canvas captures)
├── 02-nfl-matchup-prediction/
│   ├── README.md
│   ├── diagrams/
│   └── screenshots/
└── 03-nfl-fantasy-optimizer/
    ├── README.md
    ├── diagrams/
    └── screenshots/
```

---

## A Note on Redaction

Screenshots show workflow structure, node sequencing, and expression logic. All of the following have been redacted or replaced with placeholders:

- API keys, webhook URLs, and credential names
- Client names, phone numbers, and email addresses
- Database connection strings
- Any data specific to live or past clients

The purpose of this repo is to demonstrate *how* these workflows are built, not to share working production code.
