# Manas Raghuwanshi

**AI Engineer building agents, LLM systems, and developer tools.**

I like working on the systems around the model: agent runtimes, tool execution, context engineering, sandboxes, evaluation, persistence, and the infrastructure that makes AI products reliable.

[Portfolio](https://manasr.dev) · [LinkedIn](https://www.linkedin.com/in/manas-raghuwanshi-526a55291) · [X](https://x.com/Ragu_dev23) · [Email](mailto:manasr955@gmail.com)

---

### What I'm building

**[Woopcode](https://github.com/mangit955/woop-code)** — a terminal-native coding agent built from scratch.

- Multi-provider agent runtime for **Gemini, OpenAI, and Anthropic**
- Tool orchestration, repository-aware context, streaming, and session management
- Fail-closed shell risk classification and approval policies
- Sandbox-aware execution and real-filesystem testing
- Benchmark-driven context engineering and agent evaluation

**[Nap](https://github.com/mangit955/nap)** — an AI app-building platform where you describe an application and the agent builds it while you walk away.

- Agent runtime + tool execution inside isolated **E2B sandboxes**
- Durable event log with Postgres + WebSocket streaming
- Snapshot/restore for idle projects
- Token, step, sandbox, and per-user quotas
- Authentication, encrypted API-key storage, cancellation, and recovery
- **2,243 tests across 173 files**

---

### Engineering interests

`AI Agents` `LLM Systems` `Agent Infrastructure` `Context Engineering` `Developer Tools` `AI Evaluation` `TypeScript` `Python`

---

### A few things I've learned building AI systems

- **Smaller context doesn't necessarily mean cheaper context.**  
  In Woopcode, a compaction strategy reduced peak prompt size by **36–43%**, but rewriting the cached prefix destroyed much of the provider's cache reuse.

- **Unrecognized shell commands should fail closed.**  
  For an agent with write access to a repository, treating unknown commands as safe is a dangerous default.

- **Durability changes what an agent product can be.**  
  Nap persists events before fanout and snapshots idle sandboxes so a user can leave and return without losing the work or paying for an idle machine.

---

### Currently

Building AI agents and developer infrastructure, and looking for **AI Engineer / Applied AI / AI Infrastructure / Developer Tools** opportunities.

I care most about problems where **models meet real systems**.

---

### Links

🌐 [manasr.dev](https://manasr.dev)  
💼 [LinkedIn](https://www.linkedin.com/in/manas-raghuwanshi-526a55291)  
𝕏 [@Ragu_dev23](https://x.com/Ragu_dev23)  
✉️ [manasr955@gmail.com](mailto:manasr955@gmail.com)
