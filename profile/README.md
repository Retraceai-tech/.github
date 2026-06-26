<div align="center">

<img src="https://raw.githubusercontent.com/Retraceai-tech/.github/main/profile/assets/banner.gif" alt="Retrace" width="560" />

# Retrace

### The execution replay engine for AI agents.

Record every LLM call, tool invocation, and error your agents make — replay it step-by-step like a video, fork from any decision point, and prove the fix.

[![Platform](https://img.shields.io/badge/Platform-retraceai.tech-FF6B00?style=for-the-badge)](https://retraceai.tech)
[![Docs](https://img.shields.io/badge/Docs-docs.retraceai.tech-0A66C2?style=for-the-badge)](https://docs.retraceai.tech)
[![CLI](https://img.shields.io/badge/CLI-cli.retraceai.tech-111111?style=for-the-badge)](https://cli.retraceai.tech)

</div>

---

## What is Retrace?

Retrace turns every AI-agent run into a **recorded, replayable, forkable artifact** — so engineering teams can see exactly what happened in production, reproduce it on demand, and branch from any step to test a fix.

Add one wrapper to your agent. From then on every model call, tool call, retrieval, and error is captured as a **span** inside a **trace**. Open the dashboard and that run becomes an interactive timeline you can scrub through, fork, and re-execute.

> **Record → Replay → Fork → Prove** — the loop AI engineers actually live in: *something broke → find the exact step → change one thing → prove the fix → ship it.*

## Capabilities

- **Record** — one wrapper captures the full execution tree; no manual logging.
- **Replay** — step through a past run, or re-run it live to see what changed.
- **Fork & cascade-replay** — branch at any span, change the input, and the whole agent re-executes down the new path.
- **Prove the fix** — re-run a failed trace and get a verdict: improved, regressed, or unchanged.
- **Detect failures** — hallucinations, loops, goal drift, context loss, and schema violations, flagged automatically.
- **Control spend** — circuit breakers and budget ceilings stop a runaway agent *before* the next expensive call.
- **Govern** — PII redaction, prompt-injection scanning, and audit logs.
- **Share** — publish any run as an interactive, public "tape."

## Products

| Product | Where |
|---------|-------|
| 🌐 **Platform** — record, replay, fork, detections & analytics | **[retraceai.tech](https://retraceai.tech)** |
| 📚 **Documentation** — guides, SDK & API reference | **[docs.retraceai.tech](https://docs.retraceai.tech)** |
| ⌨️ **CLI** — drive Retrace from your terminal | **[cli.retraceai.tech](https://cli.retraceai.tech)** · [`homebrew-tap`](https://github.com/Retraceai-tech/homebrew-tap) |
| 🧩 **SDKs** — Python & TypeScript | [`retrace-sdk`](https://github.com/Retraceai-tech/retrace-sdk) |

## Get started

```bash
# Python
pip install retrace

# TypeScript
npm install retrace-sdk

# CLI (macOS, Linux, WSL)
brew tap retraceai-tech/homebrew-tap
brew trust retraceai-tech/tap
brew install retrace-cli
```

```python
import retrace

retrace.configure(api_key="rt_...")

@retrace.record(name="research-agent", resumable=True)
def run_agent(prompt: str):
    plan = call_planner(prompt)      # captured automatically
    results = call_tools(plan)       # captured automatically
    return summarize(results)
```

<div align="center">

---

**[Get started →](https://retraceai.tech)** · **[Read the docs →](https://docs.retraceai.tech)** · **[Try the CLI →](https://cli.retraceai.tech)**

Built for the AI engineering loop: **find the step, change one thing, prove the fix.**

<br/>

<picture><img src="https://raw.githubusercontent.com/Retraceai-tech/.github/main/profile/assets/banner.png" alt="Retrace" height="28" /></picture>

<sub>
  <a href="https://retraceai.tech"><b>Website</b></a> &nbsp;•&nbsp;
  <a href="https://docs.retraceai.tech"><b>Documentation</b></a> &nbsp;•&nbsp;
  <a href="https://cli.retraceai.tech"><b>CLI</b></a> &nbsp;•&nbsp;
  <a href="https://github.com/Retraceai-tech"><b>GitHub</b></a>
</sub>

<sub>© 2026 Retrace · The execution replay engine for AI agents · Made for AI engineers.</sub>

</div>
