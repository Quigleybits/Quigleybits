<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=28&duration=4000&pause=1000&color=00FF00&center=true&vCenter=true&width=720&lines=Hi+there!+I'm+Quigleybits+%F0%9F%91%8B;Agentic+Infrastructure+%7C+Full-Stack+%7C+Toolsmith" alt="Typing SVG" />
</div>

<br>

## About me

UK-based agentic infrastructure engineer. I build the systems and tooling that make AI agents useful in real engineering work — MCP servers, role-chained pipelines, knowledge infrastructure, and a CLI standard for MCP.

<br>

## What I'm into

### AI as a workflow engine, not a chatbot

Orchestrating role-chained agent pipelines (planner → implementer → verifier → reviewer → critic) instead of single-prompt requests. Running parallel agent sessions with explicit file ownership and worktree isolation. Treating AI as a multi-stage workflow with scored peer review at plan and code checkpoints — not as autocomplete with vibes.

Public artefacts: a published npm package of Claude Code slash commands, a handful of Claude Code plugins (text-to-speech, local Claude↔Codex bridge), and a research lab for agent-team assemblies.

### Personal knowledge infrastructure

A production RAG of my own design — Postgres + pgvector + Voyage-4-large (1024d) + HNSW, fronted by Supabase Edge Functions and a TypeScript MCP server, with Telegram capture, daily ingest crons, and weekly synthesis. Cloud-first by choice: no VPS and no GPU dependency in the production loop. Embed the source, not the summary.

### Standards & infra contributions

Currently authoring **MCLIP** — a CLI conformance profile for the Model Context Protocol — with a normative spec, a security model, 30+ conformance fixtures, and a Go reference implementation. The goal: when any MCP server is exposed through any MCLIP-conformant client, the command shape, flag conventions, JSON envelope, and exit codes are identical. Live at <https://mclip.dev>.

### Pipelines & automation

YouTube transcript scrapers (yt-dlp + faster-whisper + residential proxies for cron runs), X / Twitter API bookmark pipelines via OAuth2 PKCE, Firecrawl + Tavily for structured web research, and GitHub Actions for embed-pending workers, weekly synthesis, and health checks. The bias is toward small, durable, scheduled jobs over big synchronous services.

### Full-stack pragmatism

Comfortable shipping in Next.js 16, SvelteKit, React Native + Expo, and Phaser 3, with backends rotating between Supabase (Postgres + RLS + Realtime + Edge Functions) and Firebase (Firestore + Auth + Cloud Functions + App Check). Python for data, scraping, and tooling; Go where the standard demands it. Multiple live deployments behind custom domains.

<br>

## How I work

- **Spec → plan → build.** Specs and plans are first-class artefacts; no ad-hoc implementation.
- **Verification before completion.** Pre-commit hooks gate on tests / lint / types; Playwright (Node-script-first) for UI verification.
- **Cheapest model per task.** Haiku for enrichment, Sonnet for synthesis, Opus reserved for deep reasoning.
- **Complexity only where it earns its keep.** Free-tier-first, serverless-first, boring tech first.
- **Pilot then batch.** Risky changes proven on one item before applied across a set.

<br>

## Tech I reach for

<div align="center">
  <img src="https://skillicons.dev/icons?i=ts,js,python,go,nextjs,svelte,react,nodejs,tailwind,supabase,firebase,postgres,docker,vercel,git&perline=8" />
</div>

<table>
  <tr>
    <td><b>AI / LLM</b></td>
    <td>Claude (Opus / Sonnet / Haiku), Codex CLI, MCP servers (TS + Go), Voyage embeddings, FAISS, Whisper / Voxtral</td>
  </tr>
  <tr>
    <td><b>Frontend</b></td>
    <td>Next.js 16 (App Router, Turbopack), SvelteKit, React Native + Expo, Phaser 3, Tailwind, vanilla TS + Vite</td>
  </tr>
  <tr>
    <td><b>Backend</b></td>
    <td>Supabase (Postgres, RLS, Realtime, Edge Functions), Firebase (Firestore, Auth, Cloud Functions Gen 2, App Check), Flask, Bun</td>
  </tr>
  <tr>
    <td><b>Pipelines</b></td>
    <td>yt-dlp, faster-whisper, Tavily, Firecrawl, GitHub Actions cron, residential-proxy networks</td>
  </tr>
  <tr>
    <td><b>Infra</b></td>
    <td>Vercel, Firebase Hosting, Docker, Resend (email), Playwright</td>
  </tr>
</table>

<br>

## GitHub Stats

<div align="center">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=Quigleybits&show_icons=true&theme=dark&hide_border=true&include_all_commits=true&title_color=00FF00&icon_color=00FF00&text_color=FFFFFF&bg_color=0D1117" />
  <img height="180em" src="https://github-readme-streak-stats.herokuapp.com/?user=Quigleybits&theme=dark&hide_border=true&ring=00FF00&fire=00FF00&currStreakLabel=00FF00&sideLabels=00FF00&background=0D1117" />
</div>

<br>

## Contribution Graph

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Quigleybits/Quigleybits/output/github-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Quigleybits/Quigleybits/output/github-snake.svg" />
    <img alt="Snake animation" src="https://raw.githubusercontent.com/Quigleybits/Quigleybits/output/github-snake-dark.svg" />
  </picture>
</div>

<br>

<div align="center">
  <img src="https://komarev.com/ghpvc/?username=Quigleybits&label=Profile+views&color=00FF00&style=flat" />
</div>
