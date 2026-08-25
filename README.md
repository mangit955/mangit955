# Manas Raghuwanshi

**AI Engineer.** I build the systems *around* the model — agent runtimes, tool execution, context engineering, sandboxed execution, evaluation, and the durability work that decides whether an AI product survives contact with real users.

[manasr.dev](https://manasr.dev) · [LinkedIn](https://www.linkedin.com/in/manas-raghuwanshi-526a55291) · [X](https://x.com/Ragu_dev23) · [Email](mailto:manasr955@gmail.com)

---

## What I'm building

### [Nap](https://github.com/mangit955/nap) — a durable runtime for long-running coding agents

Describe an app; an agent builds it in an isolated sandbox while you close the tab. The premise is that **a model saying it is finished is a claim, not a fact** — so every turn is committed, verified against the project's own checks, and repaired if it fails.

- **Verify, then repair.** Checks are discovered from the project's own `package.json`, run cheapest-first and short-circuit at the first failure. A failure opens a bounded repair turn (≤3) that carries the failure into the next attempt's context. A *checkpoint* is a **verified** commit, so "last known-good" is a fact a machine can evaluate rather than a judgement someone renders by reading the chat.
- **Execution left the request.** Turns are admitted, enqueued in Postgres, and claimed by a separate worker process. One in-flight turn per session is enforced by a partial unique index rather than by a `Map` some process has to remember — so a deploy drains instead of dropping work, and the tab is genuinely optional.
- **Durable append, then fanout — in that order.** Events land in Postgres before anyone sees them, which makes catching up a single question: everything after `seq`. Reconnecting an hour later is the same operation as reconnecting a second later.
- **Scale, measured rather than asserted.** A k6 ramp against a nine-pod Kubernetes cluster with KEDA on queue depth and an HPA on open sockets: **2,310 turns at 100 concurrent, 100% job/turn/verification completion, zero sequence gaps, zero duplicates**, including 219 mid-turn reconnects that each asked for the gap and got exactly it.
- **NapBench** — a benchmark harness that scores the agent against real sandboxes and a real browser, with two funded measurement write-ups committed in full.
- **3,894 tests across 289 files**, in four suites split by the environment each needs — node, `tsc`, jsdom, and a throwaway Postgres container.

`TypeScript` `Bun` `Hono` `Next.js` `Postgres + Drizzle` `E2B` `Kubernetes + KEDA` `k6`

### [Woopcode](https://github.com/mangit955/woop-code) — a terminal-native coding agent, built from scratch

- Multi-provider agent runtime across **Gemini, OpenAI, and Anthropic**
- Tool orchestration, repository-aware context, streaming, and session management
- Fail-closed shell risk classification and approval policies
- Sandbox-aware execution, tested against a real filesystem
- Benchmark-driven context engineering and agent evaluation

`TypeScript` `Multi-provider` `Terminal UI`

---

## What building these has actually taught me

- **Smaller context is not automatically cheaper context.**
  A compaction strategy in Woopcode cut peak prompt size by **36–43%** — and rewrote the cached prefix, destroying most of the provider's cache reuse. The bill went the wrong way for the right-looking reason.

- **The ceiling that fires is rarely the one you designed for.**
  A funded Nap session died on its fourth turn having assembled to a *fifth* of its context budget. A turn re-sends its whole transcript on every round trip, so its real cost is assembled size **×** step count. The truncation ladder was perfectly correct and had simply never run.

- **A grader that looks harder than the guard will embarrass you.**
  Nap's first funded measurement exposed a verifier blind spot no dry run could have: the sandbox template declared no `typecheck` script, so check discovery read three of five checks as `absent` and a job that never typechecked was reported **verified**. That drove a template fix, regression coverage, and an integration test that runs the real thing inside a real sandbox.

- **Unrecognized shell commands should fail closed.**
  For an agent holding write access to a repository, treating an unknown command as safe is a default that only looks convenient until it isn't.

- **Durability changes what an agent product can be.**
  Persisting before fanout and snapshotting idle sandboxes is what lets a user leave, come back, and neither lose the work nor pay for an idle machine in between.

---

## Currently

Building agent runtimes and developer infrastructure, and open to **AI Engineer / Applied AI / AI Infrastructure / Developer Tools** roles.

I care most about problems where **models meet real systems** — where the interesting failure isn't the model being wrong, but the harness believing it.

---

🌐 [manasr.dev](https://manasr.dev) · 💼 [LinkedIn](https://www.linkedin.com/in/manas-raghuwanshi-526a55291) · 𝕏 [@Ragu_dev23](https://x.com/Ragu_dev23) · ✉️ [manasr955@gmail.com](mailto:manasr955@gmail.com)
