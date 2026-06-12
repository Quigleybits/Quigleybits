# Aidan Quigley

**Agentic infrastructure engineer & toolsmith · London**

I build the systems, standards, and tooling that make AI agents reliable in real engineering work — role-chained pipelines, a CLI conformance standard for MCP (mclip.dev), and a production RAG brain I run daily. The method is the moat: spec-first, with decision logs, adversarial review gates, and documented dead-ends in the open. Not chat demos — a dozen live apps across web, mobile, and games, with the reasoning shown.

> In the AI age the artifact proves less than it used to — generation is cheap. What stays scarce is judgment: the problem you chose, the options you rejected, the risk you removed, and what changed because you were involved. So this profile leads with *how* the work was done, and links to the record.
>
> — Framing after **Nate B. Jones**, *AI News & Strategy Daily*.

<br>

## Currently
<!-- NOW:START -->
Building an **agentic employment hub** — local pipelines that keep my public surfaces aligned to one idea: in the AI age, the human value is the judgment behind the work, not the artifact. The same engine, generalised into a `show-your-work` tool that walks a repo's full git history and argues what its author actually decided.

Working through:

- **The harness is the moat, not the model** — the same model can swing from ~78% to ~42% task success across harnesses, so agent risk and quality live in the environment around it: permission gates, tool scoping, run-level observability — not the weights.
- **A scaffold that rewrites itself** — the step past *"the harness matters"* is a harness that evolves on every model change, feeding its own run history back in, with human-owned kill conditions on any loop allowed to edit its own structure.
- **Verification is the bottleneck** — generation has outrun the ability to check it, so the leverage now is evals and scored review gates for open-ended work, not faster generation.
- **MCP as the standard layer** — the platform contest is being fought over the standard and memory layer (MCP / A2A stitching), not raw model quality — which is why I'm authoring a CLI conformance profile for it.
<!-- NOW:END -->

<br>

## Selected work — judgment, not just artifacts
<!-- WORK:START -->
*Chosen for how the work was done. Each entry names the non-obvious call and links to the record.*

- **[MCLIP](https://mclip.dev) — a CLI conformance standard for MCP.** The MCP→CLI space was already crowded with non-portable wrappers, so rather than ship a ninth I standardised the *translation*: a normative spec with tagged rules, backed by 9 executable fixture servers and a Go verify harness that asserts response shape and exit codes — scoped honestly to mechanics, not the cross-vendor verbs MCP can't yet guarantee. A spec without conformance is just prose.
- **[2nd_brain](https://2ndbrain.website) — a production personal RAG.** Wrote an explicit trade-off hierarchy (capture-durability › always-on › simplicity …) as the tie-breaker for every design call — *"no graph DB; relational tables on the free tier are enough."* Shipped self-monitoring as discrete probes, each behind an adversarial-review pass, and captured failure modes as reusable rules instead of silently patching them.
- **[Hymn_core](https://hymncore.net) — line-by-line hymn → scripture retrieval.** Treated retrieval quality as an experiment, not a vibe: a frozen eval set, standard-candle baselines, and binomial/McNemar significance gates decide what ships — a local Qwen3 embedding swap only went live behind a `--retriever` flag after clearing the gate. A 27-entry decision log records the deltas that overturned intuition: an LLM reads the full ~300-candidate pool on theological merit, and the weak retrievers were kept for coverage once the data showed they supply 81% of candidates yet 0.8% of final picks.
- **[scosig](https://scosig.com) — a research-intelligence dashboard with an unattended daily arXiv pipeline.** Ran a six-model summariser bake-off scored by a five-judge blind panel, then overrode the prose winner for Haiku — SLA, cost, and provenance beat a marginal edge from no-SLA free endpoints. When a blind re-pilot showed abstract-only summaries left datasets *"not stated"* half the time, pulled full-text extraction forward rather than ship the degraded version. Twenty dated decision records, one per call.
- **[claude-skills](https://www.npmjs.com/package/@quigleybits/claude-skills) — a published agent-skill suite.** Skill routing is *measured, not asserted*: an LLM trigger-eval harness scores each skill against TRIGGER/IGNORE cases. Built spec-first, with review gates that caught 10 design issues before any code was written.
- **autoresearch-vision — porting an autonomous research loop to a new domain (private).** Adapted Karpathy's [`autoresearch`](https://github.com/karpathy/autoresearch) — an autonomous, single-GPU experiment loop built for *LLM* pretraining — to a different class of models and a different need: self-driving *computer-vision* research for clinical organoid / microscopy imaging. The signal is in the translation, not the fork — bits-per-byte → MAE / Dice, BPE tokeniser → image preprocessing, GPT blocks → EfficientNet + task heads — plus one deeper rethink: Karpathy treats the agent as a flat optimiser, so I made the loop *stratified*, steering it to invent architectures and mine domain literature (the part hyperparameter sweeps can't automate) over grid-searching, with a learnings ledger so dead ends aren't re-tried. The extra structure is logged in-repo as an unproven, empirically-testable bet. *Private; walkthrough on request.*
<!-- WORK:END -->

<br>

## How I work

- **Spec → plan → build.** Specs and plans are first-class artefacts; no ad-hoc implementation.
- **Adversarial review before "done."** Plans and diffs go through an independent reviewer; corrections are folded back in verbatim, not waved away.
- **Verification before completion.** Pre-commit hooks gate on tests, lint, and types; UI changes are checked in a real browser, not asserted.
- **Cheapest model that does the job.** Haiku for enrichment, Sonnet for synthesis, Opus for deep reasoning.
- **Complexity only where it earns its keep.** Serverless-first, free-tier-first, boring tech first.
- **Pilot, then batch.** Risky changes are proven on one item before they touch the set.

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
**Live:** [mclip.dev](https://mclip.dev) · [2ndbrain.website](https://2ndbrain.website) · [hymncore.net](https://hymncore.net)
