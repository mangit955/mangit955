# Manas Raghuwanshi

Full-stack engineer. Distributed systems, async pipelines, real-time products. Final-year CS, graduating 2026 — currently looking for a full-time Software Engineer role.

**[manasr.dev](https://manasr.dev)** · [LinkedIn](https://www.linkedin.com/in/manas-raghuwanshi-526a55291) · [X](https://x.com/Ragu_dev23) · [manasr955@gmail.com](mailto:manasr955@gmail.com)

---

### Currently

- Shipping and interviewing — four production apps live, actively talking to teams
- Going deep on distributed systems and database internals between interviews
- Rewriting AI-generated code by hand to actually internalize new patterns, not just ship them

### Stack

`TypeScript` `Next.js` `Node.js` `Bun` `PostgreSQL` `Redis` `Docker` `Prisma` `Python`

---

### Featured builds

**[Flux — Perpetual Futures Exchange](https://github.com/mangit955/perpectual-futures)** · `TypeScript` `Bun` `PostgreSQL` `Redis Streams`
Custom in-memory matching engine on a Treap-based price-level tree (O(log n) insert/cancel), deterministic price-time priority, self-trade prevention. Redis Streams + a transactional outbox pattern give exactly-once event persistence through crash recovery. Full trading lifecycle — funding, liquidations, ADL — driven by live Binance price feeds.

**[Aurel — Visual Workflow Automation Engine](https://github.com/mangit955/aurel)** · `Next.js` `React Flow` `BullMQ` `PostgreSQL`
n8n-inspired automation engine, 50+ users. Drag-and-drop React Flow builder on a custom graph-traversal runtime with cycle detection. Redis + BullMQ job layer: per-worker concurrency limits, exponential-backoff retries, dead-letter queuing, live per-node execution logs over WebSockets.

**[Fill.in — Collaborative Form Builder SaaS](https://github.com/mangit955/fill.in)** · `Next.js` `Supabase` `Zod`
Multi-tenant form builder, 20+ active users. Conditional branching, real-time autosave, RBAC collaboration. Analytics dashboard at sub-200ms via indexed Postgres queries; end-to-end Zod validation on every route.

**[FitCoach Agent — AI Fitness Coaching Platform](https://github.com/mangit955/fitness-coach-agent)** · `FastAPI` `LangChain` `Python`
Multi-tool LLM agent — discrete LangChain tools for workout planning, macro calculation, progress retrieval, invoked autonomously instead of one monolithic prompt. FastAPI + SQLite backend, Dockerized, extended with a Telegram bot interface.

---

📫 **manasr955@gmail.com** · 🌐 **[manasr.dev](https://manasr.dev)**
