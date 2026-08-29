# Manas Raghuwanshi

**AI engineer building agent runtimes and developer infrastructure.** I work on the layer where model output meets system guarantees: tool execution, sandboxing, persistence, verification, evaluation, and context cost.

[manasr.dev](https://manasr.dev) · [LinkedIn](https://www.linkedin.com/in/manas-raghuwanshi-526a55291) · [X](https://x.com/Ragu_dev23) · [Email](mailto:manasr955@gmail.com)

## Selected work

### [Nap](https://github.com/mangit955/nap) · durable runtime for long-running coding agents

Nap runs coding work outside the request that started it.

- A Postgres-backed queue and event log let workers execute turns while the browser reconnects from durable `seq` values.
- An E2B sandbox owns all six agent tools: read, write, edit, list, search, and command execution.
- Each turn commits its workspace, discovers checks from the project's `package.json`, and creates a checkpoint only after verification. Failures open a bounded repair turn.
- A documented nine-pod load run completed 2,310 turns at 100 concurrent with zero sequence gaps and zero duplicates. [Read the scale report.](https://github.com/mangit955/nap/blob/main/docs/scaling-cluster.md)

### [Woopcode](https://github.com/mangit955/woop-code) · terminal coding agent

Woopcode is a Bun/TypeScript CLI with provider adapters for Gemini, OpenAI, and Anthropic.

- Plan mode withholds write tools and rejects writes at runtime.
- Approval classification parses shell structure and defaults unknown commands to risky.
- Optional E2B execution, content-hash workspace sync, project-scoped sessions, replayable JSONL telemetry, and a Harbor adapter.
- [Read the runtime loop](https://github.com/mangit955/woop-code/blob/main/runtime/loop.ts) · [read the approval boundary](https://github.com/mangit955/woop-code/blob/main/runtime/approval/classifier.ts) · [read sandbox sync](https://github.com/mangit955/woop-code/blob/main/runtime/sandbox/sync.ts)

## Engineering notes

- In Woopcode, a context compaction change cut peak prompt size by 36–43% but reduced cache reuse. Fewer tokens did not mean lower cost.
- In Nap, funded runs exposed a verifier blind spot: a missing sandbox `typecheck` script made absent checks look verified. The fix added template coverage, regression tests, and a real-sandbox integration case. [Read the measurement notes.](https://github.com/mangit955/nap/blob/main/docs/napbench-verification-measurement.md)

## Currently

I’m building agent runtimes and AI infrastructure. I’m open to AI Engineer, Applied AI, AI Infrastructure, and Developer Tools roles.

I’m interested in systems that make model behavior inspectable, recoverable, and safe to act on.

[Website](https://manasr.dev) · [LinkedIn](https://www.linkedin.com/in/manas-raghuwanshi-526a55291) · [X](https://x.com/Ragu_dev23) · [Email](mailto:manasr955@gmail.com)
