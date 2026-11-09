# Aidan Quigley

**Agentic infrastructure engineer & toolsmith · London**

I build the systems, standards and tooling that make AI agents dependable in real engineering work: a coordination protocol for agents from different providers, a CLI conformance profile for MCP, and small extensions for terminal coding agents.

> Generation is cheap now; judgment isn't. Everything below links to something you can open and check.

<br>

## Currently
<!-- NOW:START -->
Shipping small tools for terminal coding agents, in public, with their limits stated.

- **[Agent Co-op](https://github.com/Quigleybits/agent-coop)** has been in public beta since 7 September, as [`agent-coop-cli` 0.1.0](https://pypi.org/project/agent-coop-cli/) on PyPI.
- **[pi-usage-meters](https://github.com/Quigleybits/pi-usage-meters) 0.6.3** and **[pi-ram-meters](https://github.com/Quigleybits/pi-ram-meters-extension) 0.2.0** shipped on 8 November.
- **[MCLIP](https://github.com/Quigleybits/mclip)** is pre-SEP. The core specification, 9 fixture servers and the verify harness are built. The `mclio` binary and the full conformance harness are next.
<!-- NOW:END -->

<br>

## Selected work — judgment, not just artifacts
<!-- WORK:START -->
*Public work, chosen for the call behind it. Each entry links to the record.*

- **[Agent Co-op](https://github.com/Quigleybits/agent-coop) — local-first coordination for terminal coding agents from different providers.** One agent implements and a different provider reviews. Done work is evidenced by hashed receipts, and an item closes only after independent review and the completion gate. The public docs deliberately quote no reliability rate, because *"a rate without its denominator is marketing, not evidence."* They tell you to run the suite and a real item on your own repo. MIT, no runtime dependencies.
- **[MCLIP](https://mclip.dev) — a CLI conformance profile for MCP.** The MCP-to-CLI space already had many wrappers, each with its own flags and output, so I standardised the translation instead of adding another: any MCP server gets the same command shape, JSON envelope and exit codes. [The repo](https://github.com/Quigleybits/mclip) holds the specification, 9 synthetic fixture servers and a Go verify harness.
- **[pi-usage-meters](https://github.com/Quigleybits/pi-usage-meters) — one `/usage` view of subscription quota.** It covers Claude, Codex, Copilot, Kimi, Grok, GLM and MiniMax plans. The entry renders in the transcript and never enters the model's context. Install it from [npm](https://www.npmjs.com/package/pi-usage-meters).
- **[pi-ram-meters](https://github.com/Quigleybits/pi-ram-meters-extension) — a Windows RAM dashboard and process picker for pi.** `/ram` shows what is using memory and lets you choose what to close. Names and descriptions are guidance only: labels do not authorize closure, and unknown work stays marked as caution.
- **[cctts](https://github.com/Quigleybits/cctts) — a Claude Code plugin that speaks assistant output aloud.** Voice, rate and volume can be set per terminal, per project or globally. The README says up front that spoken text goes to Microsoft's Edge TTS endpoint, and that macOS and Linux are unvalidated.
- **[claude-skills](https://www.npmjs.com/package/@quigleybits/claude-skills) — published Claude Code skills.** `/recon` surveys a project and `/debrief` closes a session. Each ships with an eval set of queries that should and should not trigger it. The installer never deletes or overwrites an existing skill directory.
- **[Scosig](https://scosig.com) — a customisable research-intelligence dashboard, scoped to each researcher's signal.** *Live product; code private.*
<!-- WORK:END -->

<br>

## How I work
<!-- HOW:START -->
- **The maker never judges its own work.** Review runs in a separate context, often with a different provider.
- **Evidence, not assertion.** "Done" needs something you can re-check: a hash, a test run or a live link.
- **Evals before automation.** Skill routing is tested against should-trigger and should-ignore queries before it runs unattended.
- **State the limits.** The READMEs say what is unsupported or not yet built.
<!-- HOW:END -->

<br>

## Tech I reach for
<!-- TECH:START -->
| | |
|---|---|
| **AI / LLM** | Claude (Fable / Opus / Sonnet / Haiku), Codex CLI, MCP servers (TypeScript + Go), Voyage + Qwen3 (local) embeddings, FAISS + BM25 hybrid retrieval, PyTorch, Whisper / Voxtral |
| **Frontend** | Next.js (App Router), SvelteKit, Astro, React Native + Expo, Phaser 3, Tailwind + shadcn |
| **Backend** | Supabase (Postgres, RLS, Realtime, Edge Functions), Firebase (Firestore, Auth, Cloud Functions, App Check), Neon + Drizzle, FastAPI / Flask |
| **Data & pipelines** | Python, pgvector, D3, yt-dlp, faster-whisper, Tavily, Firecrawl, GitHub Actions cron |
| **Infra** | Vercel, Firebase Hosting, Cloud Run, Docker, Playwright |
<!-- TECH:END -->

<br>

---

**Live:** [mclip.dev](https://mclip.dev) · [kanban.website](https://kanban.website) · [scosig.com](https://scosig.com)
