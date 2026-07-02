<div align="center">

# Hi, I'm Manas 👋

### Full-Stack Engineer building distributed systems, async pipelines & real-time products

[![Portfolio](https://img.shields.io/badge/Portfolio-manasr.dev-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://manasr.dev)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/manas-raghuwanshi-526a55291)
[![X](https://img.shields.io/badge/X-@Ragu__dev23-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/Ragu_dev23)
[![Email](https://img.shields.io/badge/Email-manasr955@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:manasr955@gmail.com)

</div>

<br>

I'm a final-year CS undergrad (graduating 2026) who learns by shipping. I've independently built and deployed **four production applications** — a matching-engine-powered exchange, a workflow automation platform, a form builder SaaS, and an AI agent — while going deep on system design, DBMS, and networking fundamentals. Currently looking for a full-time Software Engineer role.

<br>

## ⚡ What I'm working with

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Bun](https://img.shields.io/badge/Bun-000000?style=flat-square&logo=bun&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Tailwind](https://img.shields.io/badge/TailwindCSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

</div>

<br>

## 🚀 Featured builds

<table>
<tr>
<td width="50%" valign="top">

### [Flux — Perpetual Futures Exchange](https://github.com/mangit955/perpectual-futures)
Centralized perp exchange with a custom in-memory **Treap-based matching engine** (O(log n) insert/cancel), deterministic price-time priority, and self-trade prevention across a cross-margin 20x model.

Redis Streams consumer groups + a **transactional outbox pattern** (order and outbox row in one Postgres transaction) give exactly-once event persistence through crash recovery. Full trading lifecycle: 8-hour funding, automated liquidations, insurance fund, ADL engine — all driven by live Binance price feeds.

`TypeScript` `Bun` `PostgreSQL` `Redis Streams` `WebSockets` `Turborepo`

</td>
<td width="50%" valign="top">

### [Aurel — Visual Workflow Automation Engine](https://github.com/mangit955/aurel)
n8n-inspired automation engine used by **50+ users**. Drag-and-drop React Flow builder backed by a custom graph-traversal runtime with cycle detection and typed inter-node data propagation.

Durable job layer on **Redis + BullMQ**: per-worker concurrency limits, exponential-backoff retries with dead-letter queuing, and per-node execution logs streamed live over WebSockets for in-browser debugging.

`Next.js` `TypeScript` `React Flow` `BullMQ` `PostgreSQL` `Docker`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [Fill.in — Collaborative Form Builder SaaS](https://github.com/mangit955/fill.in)
Multi-tenant form builder with **20+ active users** — conditional branching, real-time autosave, and RBAC collaboration (owner/editor/viewer). Analytics dashboard hitting sub-200ms via indexed Postgres queries.

End-to-end **Zod validation** on every API route, with scoped Supabase Storage uploads governed by row-level security policies.

`Next.js` `TypeScript` `Supabase` `Zod`

</td>
<td width="50%" valign="top">

### [FitCoach Agent — AI Fitness Coaching Platform](https://github.com/mangit955/fitness-coach-agent)
Multi-tool LLM agent using discrete **LangChain tools** for workout planning, macro calculation, and progress retrieval — invoked autonomously by the model instead of one monolithic prompt.

FastAPI + SQLite backend with session-aware conversation memory, Dockerized and extended with a Telegram bot interface.

`Next.js` `FastAPI` `Python` `LangChain` `SQLite` `Docker`

</td>
</tr>
</table>

<br>

## 🧠 How I build

- Ship end-to-end: schema → API → real-time layer → deploy, with CI/CD for zero-downtime releases
- Bias toward durable systems — outbox patterns, idempotency keys, dead-letter queues over quick hacks
- Read AI-generated code and rewrite it by hand to actually internalize new patterns
- Currently sharpening distributed systems and DB internals alongside job hunting

<br>

## 📊 GitHub stats

<div align="center">

<!-- This SVG is generated and committed to this repo by .github/workflows/metrics.yml — no external server, never breaks -->
<img src="./github-metrics.svg" alt="GitHub Metrics" width="100%" />

</div>

<br>

<div align="center">

📫 Reach me at **manasr955@gmail.com** · 🌐 **[manasr.dev](https://manasr.dev)**

</div>
