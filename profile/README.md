<div align="center">

<img src="https://kendr.org/kendr-icon-192.png" alt="Kendr" width="88" height="88" />

# Kendr

**A personal AI workspace that automates work, connects apps, remembers context, runs local models, and helps you build software.**

[Website](https://kendr.org) · [Download](https://kendr.org/download.html) · [Docs](https://kendr.org/docs/) · [Developer API](https://kendr.org/docs/developer-api.html) · [Skills](https://kendr.org/skills.html) · [Blog](https://kendr.org/blog/)

</div>

---

## What Kendr is

Most AI tools stop at the chat box. Kendr is one workspace that can **think, act, remember, and build** — on the web when you want zero setup, and on the desktop when you need local files, connected apps, schedules, and local models.

Start in the browser. Install the desktop app when the work gets real.

## The products

| | | |
|---|---|---|
| 🖥️ **Kendr Colleague** | Desktop automation | Connected services, scheduled tasks, local files, local models, approval checkpoints before anything sensitive happens. |
| 🧑‍💻 **Kendr Code** | Software development | Plans, writes, tests, and improves code with full project context. |
| ☁️ **Kendr Cloud** | Web + platform | Browser chat, accounts, hosted frontier models, intelligent routing, credits, sync, and one API key. |

## What makes it different

- **Intelligent routing** — `kendr-intelligent` picks one model per task on cost/capability grounds and stays sticky for that task. Exact models stay addressable through canonical `kc-*` aliases.
- **Deep research with a source trail** — citations, reusable context, and deliverables you can hand off to execution, not a wall of prose.
- **Persistent memory** — project and user memory that survives the session.
- **Local-first when it matters** — local models and local files, so private work never has to leave the machine.
- **Skills & MCP** — installable capability packs and hosted MCP servers, publishable through a versioned contract.
- **Cloud knowledge bases** — hosted KB indexing, retrieval, evaluation, and a managed vector store.
- **One key, one wallet** — provider credentials stay server-side; usage settles against a single credit ledger with exact per-call accounting.

## Build on Kendr

OpenAI-compatible, so most SDKs work with a base-URL change:

```bash
curl https://api.kendr.org/v1/chat/completions \
  -H "Authorization: Bearer kndr_live_..." \
  -H "Content-Type: application/json" \
  -d '{
    "model": "kendr-intelligent",
    "messages": [{"role": "user", "content": "Summarize this quarter'\''s filings."}]
  }'
```

Also available: `/v1/responses`, `/v1/messages` (Anthropic Messages), `/v1/models`, video analysis, and the Kendr search surfaces (Search, Images, Maps, Flights, Hotels, Shopping, Scholar).

- 📘 [Developer API](https://kendr.org/docs/developer-api.html) — formats, verified streaming, exact usage, errors
- 🔐 [Auth & SDKs](https://kendr.org/docs/auth-and-sdks.html) — OTP, sessions, scoped API keys, OAuth (PKCE + device code), JS/Python SDKs
- 🔌 [Models & connectors](https://kendr.org/docs/connectors-and-models.html)
- 🧩 [Skills & hosted MCP](https://kendr.org/docs/skills-and-mcp.html)
- 📄 [OpenAPI spec](https://api.kendr.org/api/v1/openapi.json)

## Under the hood

A deliberately hybrid stack, each part where it earns its keep:

- **Rust** — model contracts, routing, provider invocation, immutable credit settlement, catalog discovery, reconciliation
- **Python** — identity, accounts, marketplace, knowledge bases, updates, administration
- **React + Vite** — public site, browser chat, wallet and usage views, admin console
- **Postgres + Redis** — service-owned schemas; rate, health, affinity, and circuit-breaker state
- **Kubernetes on EKS**, GitOps-delivered, with commit-SHA-pinned images and a manually dispatched production promotion

## Comparisons

- [Kendr Intelligent vs. leading models](https://kendr.org/comparison/models.html) — cost, context, output limits, workload fit
- [Kendr vs. Gemini / ChatGPT Deep Research](https://kendr.org/comparison/deep-research.html)

## Get in touch

- 🌐 [kendr.org](https://kendr.org)
- 📥 [Download the desktop app](https://kendr.org/download.html)
- 🏢 [Enterprise](https://kendr.org/enterprise)
- ✉️ Questions, partnerships, and enterprise inquiries — via the site

<div align="center">
<sub>Built for people who want AI that finishes the work, not just describes it.</sub>
</div>
