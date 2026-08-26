# Agent References

A local reference collection of open-source AI agent projects and supporting libraries, cloned for study and experimentation.

## Repository layout

| Path | Contents |
|---|---|
| `reference/agent` | Agent frameworks and harnesses (see below) |
| `reference/support` | Supporting libraries (see below) |
| `reference/agent/README.md` | Per-repo details and update commands |

Both reference folders are gitignored (see `.gitignore`) so the clones stay local and don't pollute this repo's history.

## Agent repos (`reference/agent`)

| Directory | Repo | Notes |
|---|---|---|
| `codex` | [openai/codex](https://github.com/openai/codex) | OpenAI's local coding agent CLI |
| `pi` | [earendil-works/pi](https://github.com/earendil-works/pi) | Pi agent harness: coding agent, runtime, multi-provider LLM API |
| `hermes-agent` | [nousresearch/hermes-agent](https://github.com/nousresearch/hermes-agent) | Self-improving agent by Nous Research with a learning loop |
| `jcode` | [1jehuang/jcode](https://github.com/1jehuang/jcode) | RAM-efficient coding agent harness |
| `prime-agent` | [PrimeIntellect-ai/prime-agent](https://github.com/PrimeIntellect-ai/prime-agent) | Self-improving RLM coding and research agent |
| `deepseek-harness` | [deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness) | Plugin-based agent harness ("everything is a plugin") |
| `meta-harness` | [stanford-iris-lab/meta-harness](https://github.com/stanford-iris-lab/meta-harness) | Stanford IRIS Lab framework for automated search over task-specific model harnesses (paper: arXiv 2603.28052) |
| `headlong` | [laude-institute/headlong](https://github.com/laude-institute/headlong) | Laude Institute's <10K-line Bash agent microharness with persistent agency — the agent keeps thinking between external interactions and decides when to respond |
| `maka` | [apache/maka](https://github.com/apache/maka) | Apache Software Foundation (incubating) local-first agent workspace — desktop + CLI + eval, all sharing one Runtime Host that records model messages and tool calls as recoverable execution facts |
| `loop-engineering` | [cobusgreyling/loop-engineering](https://github.com/cobusgreyling/loop-engineering) | Patterns and tooling for designing agent loops |
| `loopx` | [huangruiteng/loopx](https://github.com/huangruiteng/loopx) | Open, provider-neutral, local-first control plane for long-horizon agents (sits on top of Codex, Claude Code, Cursor, dsh) |

## Support repos (`reference/support`)

| Directory | Repo | Notes |
|---|---|---|
| `turbovec` | [ryancodrai/turbovec](https://github.com/ryancodrai/turbovec) | Memory-efficient Rust vector search (TurboQuant) with Python bindings |
| `PageIndex` | [VectifyAI/PageIndex](https://github.com/VectifyAI/PageIndex) | Reasoning-based, vectorless RAG with an agentic tree index |
| `OpenViking` | [volcengine/OpenViking](https://github.com/volcengine/OpenViking) | Context/memory database for AI agents |
| `graphiti` | [getzep/graphiti](https://github.com/getzep/graphiti) | Temporal knowledge graphs built from conversations |

## License

Apache License 2.0 — see [LICENSE](LICENSE).
