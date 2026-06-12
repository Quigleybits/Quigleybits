# Aidan Quigley

**Agentic infrastructure engineer & toolsmith · London**

I build the systems, standards, and tooling that make AI agents reliable in real engineering work — role-chained pipelines, a CLI conformance standard for MCP (mclip.dev), and a production RAG brain I run daily. The method is the moat: spec-first, with decision logs, adversarial review gates, and documented dead-ends in the open. Not chat demos — a dozen live apps across web, mobile, and games, with the reasoning shown.

> Generation is cheap now; judgment isn't. This profile leads with the problems I chose, the options I rejected, and the risk I removed — *how* the work was done — and links to the record.

<br>

## Currently
<!-- NOW:START -->
Building **agent_os** — a personal agentic operating system, run as a private research workshop: an 8-role agent team (planner, paired researchers, coder, tester, always-on critic, doc-maintainer) deployed in my daily harness; a loop runtime with ~20 specialist roles on file but only 2 resident; and a 6-level taxonomy for memory that outlives sessions. The bet underneath: **the harness is the moat, not the model** — the same model's task success can double across harnesses, so the scaffold is where the engineering lives.

Working through:

- **Self-evolving scaffold** — the harness should rewrite itself: run history and knowledge captures feed back into skills, agent definitions, and rules as versioned, measured artifacts.
- **Verification is the bottleneck** — generation has outrun checking; autonomous loops compound only through a three-part ratchet (safety veto, minimum-improvement delta, re-baselining on the same evals).
- **Agentic pipelines, not faster typing** — agents owning end-to-end handoffs (spec → build → adversarial review → merge), with human review throughput as the binding constraint.
<!-- NOW:END -->

<br>

## Selected work — judgment, not just artifacts
<!-- WORK:START -->
*Chosen for how the work was done. Each entry names the non-obvious call and links to the record.*

- **[MCLIP](https://mclip.dev) — a CLI conformance standard for MCP.** The MCP→CLI space was already crowded with non-portable wrappers, so rather than ship a ninth I standardised the *translation*: a normative spec with tagged rules, backed by 9 executable fixture servers and a Go verify harness that asserts response shape and exit codes. Deliberately scoped to mechanics-not-semantics — MCP doesn't standardise tool names, so the spec refuses to promise what it can't hold — and fronted by an agent-readable door (`llms.txt` + a machine-readable profile manifest), so the standard is consumable by the agents it governs.
- **[2nd_brain](https://2ndbrain.website) — a production personal RAG.** Wrote an explicit trade-off hierarchy (capture-durability › always-on › simplicity …) as the tie-breaker for every design call — *"no graph DB; relational tables on the free tier are enough."* Shipped self-monitoring as discrete probes, each behind an adversarial-review pass, and captured failure modes as reusable rules instead of silently patching them.
- **[Hymn_core](https://hymncore.net) — line-by-line hymn → scripture retrieval.** Refused to let ranking scores pick the answer: five overlapping sources feed ~300 candidates, but an LLM selects on theological merit — and I kept the weak retrievers for coverage after the data showed they supply 81% of candidates yet 0.8% of final picks. A 27-entry decision log records the measured deltas that overturned intuition, and a local-embedding bake-off shipped only after passing a statistical significance gate — behind a `--retriever` flag, not a blind swap.
- **[cctts](https://github.com/Quigleybits/cctts) — a Claude Code TTS plugin.** Deleted an entire storage layer once it proved unused (three rejected alternatives logged), and self-audited the shipped README against reality — logging the drift rather than hiding it.
- **[claude-skills](https://www.npmjs.com/package/@quigleybits/claude-skills) — a published agent-skill suite.** Skill routing is *measured, not asserted*: an LLM trigger-eval harness scores each skill against TRIGGER/IGNORE cases, and nothing publishes until it survives a test on a real codebase that isn't its own. Built spec-first, with review gates that caught 10 design issues before any code was written.
- **autoresearch-vision — porting an autonomous research loop to a new domain (private).** Adapted Karpathy's [`autoresearch`](https://github.com/karpathy/autoresearch) — an autonomous, single-GPU experiment loop built for *LLM* pretraining — to a different class of models and a different need: self-driving *computer-vision* research for clinical organoid / microscopy imaging. The signal is in the translation, not the fork — bits-per-byte → MAE / Dice, BPE tokeniser → image preprocessing, GPT blocks → EfficientNet + task heads — plus one deeper rethink: Karpathy treats the agent as a flat optimiser, so I made the loop *stratified*, steering it to invent architectures and mine domain literature (the part hyperparameter sweeps can't automate) over grid-searching, with a learnings ledger so dead ends aren't re-tried. The extra structure is logged in-repo as an unproven, empirically-testable bet. *Private; walkthrough on request.*
<!-- WORK:END -->

<br>

## How I work
<!-- HOW:START -->
*Distilled from `agent_os` — my private research workshop on agent teams, loops, and memory — and refreshed as the system evolves. Walkthrough on request.*

- **An agent team, not a chat window.** Eight roles — orchestrator, planner, paired researchers, coder, tester, always-on critic, doc-maintainer — run in my daily harness. "Done" is gated by the tester and challenged by the critic, never declared by the maker.
- **Catalog ≠ payroll.** ~20 specialist roles on file, 2 resident; specialists spawn fresh per job on the cheapest model that clears the bar, write their output to disk, and die. Cost scales with work, not headcount.
- **Maker / verifier split.** The agent that builds never judges its own work — verification runs in a separate context, often on a different model.
- **Ratchets before autonomy.** Self-improving loops pass a three-part gate — safety veto, minimum-improvement delta, re-baselining on the same eval subset — so compounding only points upward.
- **Artifacts, not prose.** Handoffs are file paths and traces, never summaries; a summary without its source is context pollution.
- **Evals before automation.** Skill routing is measured against trigger/ignore cases before anything runs unattended; skill files are trainable parameters, versioned and scored.
- **A constitution agents can't edit.** Principles, kill conditions, and decision logs are human-owned; loops read them, propose changes, and never write them.
<!-- HOW:END -->

<br>

## Tech I reach for

| | |
|---|---|
| **AI / LLM** | Claude (Opus / Sonnet / Haiku), Codex CLI, MCP servers (TypeScript + Go), Voyage embeddings, FAISS, Whisper / Voxtral |
| **Frontend** | Next.js (App Router), SvelteKit, React Native + Expo, Phaser 3, Tailwind |
| **Backend** | Supabase (Postgres, RLS, Realtime, Edge Functions), Firebase (Firestore, Auth, Cloud Functions, App Check), Flask |
| **Data & pipelines** | Python, pgvector, yt-dlp, faster-whisper, Tavily, Firecrawl, GitHub Actions cron |
| **Infra** | Vercel, Firebase Hosting, Docker, Playwright |

<br>

---

**Open to** AI / applied-AI, agent & developer-tooling, and AI-infrastructure roles.
**Live:** [mclip.dev](https://mclip.dev) · [2ndbrain.website](https://2ndbrain.website) · [hymncore.net](https://hymncore.net) · [kanban.website](https://kanban.website) · [scosig.com](https://scosig.com) · [portfolio](https://quigleybits.work)
