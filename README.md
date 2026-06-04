# Aidan Quigley

**Agentic infrastructure engineer & toolsmith · London**

I build the systems, standards, and tooling that make AI agents reliable in real engineering work — role-chained pipelines, a CLI conformance standard for MCP (mclip.dev), and a production RAG brain I run daily. The method is the moat: spec-first, with decision logs, adversarial review gates, and documented dead-ends in the open. Not chat demos — a dozen live apps across web, mobile, and games, with the reasoning shown.

> In the AI age the artifact proves less than it used to — generation is cheap. What stays scarce is judgment: the problem you chose, the options you rejected, the risk you removed, and what changed because you were involved. So this profile leads with *how* the work was done, and links to the record.

<br>

## Currently
<!-- NOW:START -->
Building an **agentic employment hub** — local pipelines that keep my public surfaces aligned to one idea: in the AI age, the human value is the judgment behind the work, not the artifact. The same engine, generalised into a `show-your-work` tool that walks a repo's full git history and argues what its author actually decided.

Working through:

- **The harness, not the model** — permission gates, tool scoping, and run-level observability are where agent risk and quality actually live.
- **Workflow architecture over prompting** — multi-pass pipelines (spec → build → adversarial review), with skill and `CLAUDE.md` files treated as versioned, measured artifacts.
- **Autonomous research loops** — an agent that runs its own train → measure → keep/discard cycles on a single GPU, steered toward *inventing* model architectures rather than grid-searching hyperparameters, with a learnings ledger so it never re-tries a ruled-out idea.
- **Agentic pipelines, not faster typing** — agents owning end-to-end handoffs (review → merge → release).
<!-- NOW:END -->

<br>

## Selected work — judgment, not just artifacts
<!-- WORK:START -->
*Chosen for how the work was done. Each entry names the non-obvious call and links to the record.*

- **[MCLIP](https://mclip.dev) — a CLI conformance standard for MCP.** The MCP→CLI space was already crowded with non-portable wrappers, so rather than ship a ninth I standardised the *translation*: a normative spec with tagged rules, backed by 9 executable fixture servers and a Go verify harness that asserts response shape and exit codes. A spec without conformance is just prose.
- **[2nd_brain](https://2ndbrain.website) — a production personal RAG.** Wrote an explicit trade-off hierarchy (capture-durability › always-on › simplicity …) as the tie-breaker for every design call — *"no graph DB; relational tables on the free tier are enough."* Shipped self-monitoring as discrete probes, each behind an adversarial-review pass, and captured failure modes as reusable rules instead of silently patching them.
- **[Hymn_core](https://hymncore.net) — line-by-line hymn → scripture retrieval.** Refused to let ranking scores pick the answer: five overlapping sources feed ~300 candidates, but an LLM selects on theological merit — and I kept the weak retrievers for coverage after the data showed they supply 81% of candidates yet 0.8% of final picks. A 27-entry decision log records the measured deltas that overturned intuition (a work-stealing queue cut one job from ~8h to ~5min).
- **[cctts](https://github.com/Quigleybits/cctts) — a Claude Code TTS plugin.** Deleted an entire storage layer once it proved unused (three rejected alternatives logged), and self-audited the shipped README against reality — logging the drift rather than hiding it.
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

## Activity

<div align="center">
  <img src="https://ghchart.rshah.org/Quigleybits" alt="Aidan Quigley's GitHub contribution graph" />
</div>

<br>

---

**Open to** AI / applied-AI, agent & developer-tooling, and AI-infrastructure roles.
**Live:** [mclip.dev](https://mclip.dev) · [2ndbrain.website](https://2ndbrain.website) · [hymncore.net](https://hymncore.net)
