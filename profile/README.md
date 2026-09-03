# Raul Montoya Cardenas

**Early-Career AI / Research Engineer | Agentic Systems, Model Evaluation & ML Infrastructure**

**B.S. AI Engineering student, Western Governors University — Expected September 2027**

San Marcos, Texas · montoyaraul34@gmail.com

[GitHub Projects](https://github.com/rmems?tab=projects) · [Hugging Face](https://huggingface.co/rmems) · [Limen Neural](https://github.com/Limen-Neural)

> Building reproducible post-training, synthetic-data, model-evaluation, and agentic engineering systems on hardware I can own.

I am an early-career AI / research engineer focused on **agentic systems, synthetic-data research, model evaluation, post-training infrastructure, and model tooling**. I build in Python, Rust, CUDA, and related systems languages, with an emphasis on executable validation, reproducibility, provenance, and honest separation between shipped evidence and active research.

My current program connects three systems:

- **Synthetic Factory** evaluates and curates synthetic-data campaigns behind provenance, rights, and project-policy gates.
- **Operation Prometheus** reconstructs real software-engineering trajectories from issues, patches, reviews, fixes, CI, and merges.
- **Agoge Model Forge** turns eligible data into frozen training/evaluation contracts, local post-training runs, and held-out comparisons.

Frontier hosted-model outputs remain research comparators in this program rather than weight-update data. Training candidates must independently pass the applicable provenance, license, and project-policy gates.

---

## Selected engineering proof

### Shipped upstream contributions

- **[UsagePal PR #56 — Antigravity metrics and Linux support](https://github.com/Halloweedev/usagepal/pull/56)** — merged upstream. Added Linux Antigravity discovery and authentication paths, host-aware language-server metadata, deterministic process/socket discovery, quota-pool reporting, burn-rate status, and macOS-target dependency isolation.
- **[UsagePal PR #48 — Devin Linux support and richer telemetry](https://github.com/Halloweedev/usagepal/pull/48)** — merged and shipped in the v0.7.70 release line. Added Linux credential discovery, Devin/Devin-Next authentication paths, ACU/quota/credit tracking, pace indicators, documentation, and tests.
- **[agent-afk PR #1019 — first-class xAI/Grok provider](https://github.com/griffinwork40/agent-afk/pull/1019)** — merged. Added API-key and SuperGrok OAuth paths, provider selection, credential handling, documentation, and tests.
- **[agent-afk PR #1242 — xAI OAuth CLI compatibility](https://github.com/griffinwork40/agent-afk/pull/1242)** — merged. Fixed proxy-version negotiation with validated overrides and fallbacks.

These contributions demonstrate work inside other maintainers' architectures: understanding existing contracts, passing review, and shipping changes upstream.

### Public ML and data artifacts

- **[Hugging Face portfolio](https://huggingface.co/rmems)** — public model, dataset, telemetry, and research artifacts.
- **[Grok-1 GOZ1 research packs](https://huggingface.co/datasets/rmems/grok-1-goz1-packs)** — packaged Grok-1 quantization research artifacts with manifests and provenance.
- **[Agentic Coding Trajectories](https://huggingface.co/datasets/rmems/agentic-coding-trajectories)** — raw coding-agent trajectories for evaluation and research; public visibility is not a training-eligibility claim.
- **[Neuromorphic Event-Language Bridge](https://huggingface.co/datasets/rmems/neuromorphic-event-language-bridge)** — event-stream to structured-language grounding artifacts.
- **[Spikenaut SNN Telemetry](https://huggingface.co/datasets/rmems/Spikenaut-SNN-Telemetry)** — machine telemetry and neuromorphic research data.

---

## Current model-training program

The first controlled study will compare one open-weight starting checkpoint under matched conditions:

| Arm | Condition |
|---|---|
| **A** | Untouched starting checkpoint |
| **B** | Minimally curated, rights-cleared synthetic supervision |
| **C** | Synthetic-Factory-curated, rights-cleared synthetic supervision |
| **D** | Owned or permissively licensed real engineering trajectories |
| **E** | Curated synthetic and real-trajectory mixture |

The first run is local-first on an **RTX 5080 16 GiB**. The experiment contract will freeze model and tokenizer revisions, splits, seeds, metrics, leakage checks, and success/null criteria before results are inspected.

**Current status:** infrastructure and data contracts are being hardened; no training improvement is claimed in advance. Active work includes the [Synthetic Factory rights-policy foundation](https://github.com/rmems/synthetic-factory/pull/168), [Agoge immutable readiness contracts](https://github.com/rmems/agoge-forger/pull/114), and the [Operation Prometheus eligibility and quality ledger](https://github.com/rmems/operation-prometheus/pull/64).

---

## Flagship projects

| Project | Evidence and purpose |
|---|---|
| **[synthetic-factory](https://github.com/rmems/synthetic-factory)** | Synthetic-data research with append-only evidence, provider/channel provenance, strict validation, failure-oriented fixtures, research-only frontier lanes, and active rights/project-policy enforcement |
| **[operation-prometheus](https://github.com/rmems/operation-prometheus)** | Event-sourced software-engineering trajectory forge spanning issue, implementation, review, repair, CI, and merge history |
| **[agoge-forger](https://github.com/rmems/agoge-forger)** | Local-first PyTorch post-training and evaluation tooling with configuration, artifact, checkpoint, split, and readiness contracts |
| **[xai-dissect](https://github.com/rmems/xai-dissect)** | Rust CLI for read-only structural analysis of open Grok-1 checkpoints, including tensor inventory and MoE routing maps |
| **[grok-ozempic](https://github.com/rmems/grok-ozempic)** | Grok-1 compression experiments centered on expert precision, routing fidelity, and residual drift |
| **[corinth-canal](https://github.com/rmems/corinth-canal)** | Rust research pipeline connecting telemetry encoding, spiking state, projection, model inspection, MoE routing, and SAAQ validation |
| **[Spikenaut-SNN](https://github.com/rmems/Spikenaut-SNN)** | From-scratch SNN runtime and export target for telemetry-driven neuromorphic experiments |

I also maintain modular Rust and neuromorphic libraries under **[Limen Neural](https://github.com/Limen-Neural)**, including [neuromod](https://github.com/Limen-Neural/neuromod), [axon-encoder](https://github.com/Limen-Neural/axon-encoder), [nir-rs](https://github.com/Limen-Neural/nir-rs), [synaptic-mesh](https://github.com/Limen-Neural/synaptic-mesh), and [brainstem-daemon](https://github.com/Limen-Neural/brainstem-daemon).

---

## Technical focus

| Area | Tools and methods |
|---|---|
| **Languages** | Rust, Python, Julia, CUDA C/C++, SystemVerilog |
| **ML systems** | PyTorch, Hugging Face, LoRA/QLoRA, MoE, GGUF, Safetensors, quantization, SNNs |
| **Data and evaluation** | Immutable manifests, provenance and rights gates, held-out splits, leakage guards, deterministic and executable scoring, JSONL/Parquet artifacts |
| **Infrastructure** | GitHub Actions, Docker, Linux, self-hosted GPU CI, cloud-training scaffolding, automated review gates |
| **Hardware** | NVIDIA RTX 5080 16 GiB, AMD Ryzen 9 9950X, Fedora Linux |

My neuromorphic work is a specialist research track: event-driven state, telemetry-aware control, SNN runtimes, and FPGA-oriented export and validation. It complements the central agentic/model-evaluation portfolio without being required to understand it.

---

## Engineering practice

I use coding agents heavily, with isolated branches or worktrees, local tests, linting, benchmarks or experiment gates, pull-request review, repair, and human merge decisions. Agent assistance is attributed in commits, PRs, experiment notes, or release provenance where appropriate.

What I optimize for:

**Measurable results · reproducibility · provenance · rights-aware lineage · fail-closed validation · leakage-resistant evaluation · explicit scope boundaries**

### Current priorities

1. Land the end-to-end rights/project-policy boundary for Synthetic Factory and keep research-only outputs outside all weight-update paths.
2. Freeze and execute the first local base-to-SFT held-out comparison using independently eligible data.
3. Publish the resulting checkpoints, telemetry, evaluations, regressions, and null results with reproducible artifacts.

---

## Attribution

Primary author and maintainer: **Raul Montoya Cardenas (rmems)**.

Recruiter-focused structure and research-program edits were developed with OpenAI ChatGPT / Codex. Project-specific AI contributions remain attributed in their respective commits, pull requests, experiment records, and release provenance.
