# Agent References

A local reference collection of open-source AI agent projects, agent-powered applications, and supporting libraries, cloned for study and experimentation.

## Repository layout

| Path | Contents |
|---|---|
| `reference/agent` | Agent frameworks and harnesses (see below) |
| `reference/apps` | Agent-powered applications (see below) |
| `reference/support` | Supporting libraries (see below) |
| `reference/agent/README.md` | Per-repo details and update commands |

All reference folders are gitignored (see `.gitignore`) so the clones stay local and don't pollute this repo's history.

## Agent repos (`reference/agent`)

| Directory | Repo | Notes |
|---|---|---|
| `codex` | [openai/codex](https://github.com/openai/codex) | OpenAI's local coding agent CLI |
| `pi` | [earendil-works/pi](https://github.com/earendil-works/pi) | Pi agent harness: coding agent, runtime, multi-provider LLM API |
| `SoL-Pi` | [NVlabs/SoL-Pi](https://github.com/NVlabs/SoL-Pi) | Standalone extension for Pi packaging four efficiency mechanisms from auto-research: action fusion, observation packing, evidence-preserving reduction, and online context compaction; opt-in, no Pi patches (MIT) |
| `hermes-agent` | [nousresearch/hermes-agent](https://github.com/nousresearch/hermes-agent) | Self-improving agent by Nous Research with a learning loop |
| `jcode` | [1jehuang/jcode](https://github.com/1jehuang/jcode) | RAM-efficient coding agent harness |
| `prime-agent` | [PrimeIntellect-ai/prime-agent](https://github.com/PrimeIntellect-ai/prime-agent) | Self-improving RLM coding and research agent |
| `deepseek-harness` | [deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness) | Plugin-based agent harness ("everything is a plugin") |
| `meta-harness` | [stanford-iris-lab/meta-harness](https://github.com/stanford-iris-lab/meta-harness) | Stanford IRIS Lab framework for automated search over task-specific model harnesses (paper: arXiv 2603.28052) |
| `jit-agent` | [bingreeky/JIT](https://github.com/bingreeky/JIT) | JIT-Agent — meta-agent that writes a task-specific harness on the fly ("Model-as-a-Harness"); ships 11 seed harnesses and a JIT-27B checkpoint (arXiv 2608.25593) |
| `headlong` | [laude-institute/headlong](https://github.com/laude-institute/headlong) | Laude Institute's <10K-line Bash agent microharness with persistent agency — the agent keeps thinking between external interactions and decides when to respond |
| `maka` | [apache/maka](https://github.com/apache/maka) | Apache Software Foundation (incubating) local-first agent workspace — desktop + CLI + eval, all sharing one Runtime Host that records model messages and tool calls as recoverable execution facts |
| `loop-engineering` | [cobusgreyling/loop-engineering](https://github.com/cobusgreyling/loop-engineering) | Patterns and tooling for designing agent loops |
| `loopx` | [huangruiteng/loopx](https://github.com/huangruiteng/loopx) | Open, provider-neutral, local-first control plane for long-horizon agents (sits on top of Codex, Claude Code, Cursor, dsh) |
| `herdr` | [herdrdev/herdr](https://github.com/herdrdev/herdr) | Herdr — Rust terminal multiplexer built as a runtime for coding agents; hosts Claude Code / Codex / Cursor / OpenCode in persistent panes with state detection (working / blocked / idle) and session resume across disconnects; Apache-2.0, Homebrew formula |
| `ai-agents-the-definitive-guide` | [Nicolepcx/ai-agents-the-definitive-guide](https://github.com/Nicolepcx/ai-agents-the-definitive-guide) | Companion notebooks for the O'Reilly book *AI Agents: The Definitive Guide*; 12 chapters of Colab-ready Jupyter notebooks spanning agent foundations, architectures and patterns, planning, model choice, production contracts and tool governance, deployment, evaluation, memory, cost, and threat modeling; no license declared |
| `MathModelAgent` | [jihe520/MathModelAgent](https://github.com/jihe520/MathModelAgent) | Agent for mathematical modeling competitions: a staged skill pipeline (analysis/modeling, coding and visualization, drawio diagrams, paper writing, verification) drives a problem from statement to a submission-ready paper; Python backend, web frontend, Docker deploy, prebuilt macOS/Windows desktop app; free for personal use, commercial use by arrangement |
| `pub-dsh-privacy-router` | [LYiHub/pub-dsh-privacy-router](https://github.com/LYiHub/pub-dsh-privacy-router) | Host-side plugin for DeepSeek Harness (dsh) that privacy-gates local vs cloud routing — deterministic rules plus a local classifier label each turn `public` / `sensitive` / `unknown`, keeping sensitive and unknown turns on the local model and sending only rebuilt, whitelisted plain-text public turns to the cloud; pairs with `LYiHub/pub-local-ai-discovery-server` for local provider discovery; MIT |
| `Recuris` | [Gen-Verse/Recuris](https://github.com/Gen-Verse/Recuris) | Recursive self-improvement framework (NUS/Stanford/Oxford/Princeton, arXiv 2608.24876) that improves a long-horizon agent by evolving its memory instead of its weights or prompt — a frozen agent paired with a Skill Memory, a meta-agent that patches only the failing component from structured traces, and a deterministic validation gate over paired held-out evidence; training-free and model-agnostic, SOTA on τ²-Bench Retail and Airline; Apache-2.0 |
| `ai-agent-book` | [bojieli/ai-agent-book](https://github.com/bojieli/ai-agent-book) | 《深入理解 AI Agent：设计原理与工程实践》(AI Agents in Depth) — open-source home of the book: full text of 10 chapters built around "Agent = LLM + context + tools", 109 companion experiments under `chapter1`–`chapter10`, community translations into 15 languages, PDF/EPUB builds and an Astro web reader; Apache-2.0 |
| `open-code-review` | [alibaba/open-code-review](https://github.com/alibaba/open-code-review) | OpenCodeReview (`ocr`) — Alibaba's battle-tested AI code review CLI: deterministic engineering (file selection, smart bundling into isolated sub-agent contexts, template-based rule matching, comment positioning/reflection modules) wrapped around an LLM agent with a review-tuned prompt and toolset, producing line-level comments; `ocr review` for diffs (workspace, branch range, single commit, resumable sessions) and `ocr scan` for whole-file audits, plus delegation mode where a host coding agent runs the review with no OCR API key; built-in multi-language ruleset (NPE, thread-safety, XSS, SQL injection), OpenAI/Anthropic-compatible endpoints, MCP server, CI integrations and plugins for Claude Code / Codex / Cursor / Kimi Code / OpenCode; Go, Apache-2.0 |
| `Qwen-Live-Harness` | [QwenLM/Qwen-Live-Harness](https://github.com/QwenLM/Qwen-Live-Harness) | Qwen-Live-Harness — open-source harness built around the Qwen Omni Realtime API (Qwen3.8 Omni Flash Realtime): a local daemon plus an Electron "Host" desktop UI add realtime audio/video interaction with screen or camera context, background task delegation to Qwen Code / Qoder CLI / Codex / Claude Code / Gemini CLI (with approval handling and progress tracking), proactive audio/visual/time-condition monitors, and local long-term memory libraries with cloud consolidation; macOS-first (Windows/Linux in progress), Apache-2.0 |
| `rrsi` | [google-research/rrsi](https://github.com/google-research/rrsi) | RRSI (Regularized Recursive Self-Improvement of Agent Harnesses, Google Research, arXiv 2609.24972) — evolves a frozen LLM agent's harness (prompts, control flow, tools, memory, context management, sub-agents) against a fixed evolve set while regularizing the search instead of the harness: annealed edit budget, history-conditioned proposal, stall-driven redirection to untried components, leakage-screening critic, noise-adjusted gain floor, token-cost rule and pruning of non-contributing components; one loop instantiated on three domains (terminal agent / Terminal-Bench 2.1, document work / Harvey LAB, engineering design / EngDesign), candidates drafted and evaluated in isolated git worktrees with an auditable edit history; Python, Apache-2.0 |

## App repos (`reference/apps`)

| Directory | Repo | Notes |
|---|---|---|
| `PI-Desktop` | [vastsa/PI-Desktop](https://github.com/vastsa/PI-Desktop) | PI-Desktop — modular, local-first, model-agnostic desktop workspace for AI agents: brings projects, sessions, review, preview, agents, models and workflows into one persistent environment, with a plugin SDK/devkit, i18n and an agent host/runtime (`apps/desktop`, `apps/pi-host`, `packages/agent-runtime`, `packages/agent-host`, `crates/host-core`); macOS / Windows / Linux, LGPL-3.0 |
| `orca` | [stablyai/orca](https://github.com/stablyai/orca) | Orca — "next-gen IDE for parallel agentic development": runs Codex, Claude Code, OpenCode or Pi side-by-side, each in its own git worktree, fanning one prompt across agents to compare and merge the winner; Ghostty-class terminal splits, Design Mode (click a UI element to send its HTML/CSS/screenshot into an agent prompt), SSH worktrees, native GitHub/Linear task browsing, and an iOS/Android mobile companion for monitoring and steering agents; Electron + React, MIT |

## Support repos (`reference/support`)

| Directory | Repo | Notes |
|---|---|---|
| `turbovec` | [ryancodrai/turbovec](https://github.com/ryancodrai/turbovec) | Memory-efficient Rust vector search (TurboQuant) with Python bindings |
| `PageIndex` | [VectifyAI/PageIndex](https://github.com/VectifyAI/PageIndex) | Reasoning-based, vectorless RAG with an agentic tree index |
| `OpenViking` | [volcengine/OpenViking](https://github.com/volcengine/OpenViking) | Context/memory database for AI agents |
| `graphiti` | [getzep/graphiti](https://github.com/getzep/graphiti) | Temporal knowledge graphs built from conversations |
| `zvec-grep` | [zvec-ai/zvec-grep](https://github.com/zvec-ai/zvec-grep) | zg — local-first search layer for humans and agents; unifies ripgrep, BM25, and vector search behind one interface (powered by zvec), usable from the CLI or by agents, with ranked source-linked results; Apache-2.0 |
| `deepwiki-rs` | [sopaco/deepwiki-rs](https://github.com/sopaco/deepwiki-rs) | Litho — Rust AI-driven documentation generator that analyzes a codebase and emits C4-model architecture docs (context, container, component, code level) and AI-ready context; CLI published on crates.io, successor project is `sopaco/terrain`; MIT |
| `scira` | [zaidmukaddam/scira](https://github.com/zaidmukaddam/scira) | Scira (formerly MiniPerplx) — minimalistic agentic search engine that plans, retrieves, and cites; Next.js app on the Vercel AI SDK with multi-provider model routing, web search/content retrieval, and streaming answers; AGPL-3.0, so changes must stay open source |
| `baalda` | [naveedharri/baalda](https://github.com/naveedharri/baalda) | Baalda — local-first collaborative Markdown "second brain" (Tauri v2, Rust core, TypeScript UI); plain .md files on disk are AI-editable and shared in real time, with a built-in MCP endpoint for agents; Apache-2.0 |
| `ai-knowledge-graph` | [robert-mcdermott/ai-knowledge-graph](https://github.com/robert-mcdermott/ai-knowledge-graph) | Turns unstructured documents (`.txt`, `.md`, `.rst`, `.pdf`, `.docx`) into typed Subject-Predicate-Object knowledge graphs via any OpenAI-compatible endpoint; entity standardization, traceable inference, JSON/CSV/GraphML/Neo4j Cypher exports, plus `graph-chat` and `graph-serve` commands; Apache-2.0 |
| `Self-Index` | [augustinLib/Self-Index](https://github.com/augustinLib/Self-Index) | Self-Index (Yonsei University / Samsung Research / UC Irvine / Korea University, arXiv 2609.19656) — a search index that self-evolves without human intervention: Self-Diagnosis finds index shortfalls from retrieval outcomes and co-retrieval patterns (no relevance annotations), Self-Revision refines only the affected key sets while documents stay unchanged, Self-Validation accepts revisions only when faithful, specific, and separated, and a Query Simulator explores demands not yet covered; reported +57.0% (BGE) / +40.4% (BM25) average nDCG@10 on BRIGHT, +41.1% accuracy and −24.0% online cost on BrowseComp-Plus, +13.9% on LongMemEval-V2; repository is currently a placeholder ("code will be released soon"), no license declared |

## License

Apache License 2.0 — see [LICENSE](LICENSE).
