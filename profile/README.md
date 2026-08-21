# Raul Montoya Cardenas

**ML Systems & Agent Evaluation Engineer**

San Marcos, Texas · montoyaraul34@gmail.com

[GitHub Projects](https://github.com/rmems?tab=projects) · [Hugging Face](https://huggingface.co/rmems) · [Limen Neural](https://github.com/Limen-Neural)

> *Building reproducible model systems and coding-agent evaluation infrastructure on hardware I can own.*

I build **Rust/Python/CUDA tooling for model systems, coding-agent evaluation, and reproducible ML experiments**: open-weight checkpoint analysis, MoE compression experiments, engineering-trajectory datasets, agent review/repair loops, and neuromorphic runtimes.

My current hiring focus is **ML systems, coding-agent / eval infrastructure, model tooling, and research engineering**. Neuromorphic computing is a specialist research track rather than a prerequisite for understanding the rest of the portfolio. **Pursuing AI Engineering @ WGU.**

---

## Recruiter snapshot

| Area | Evidence |
|---|---|
| **Agent systems & evals** | Coding-agent trajectories, synthetic-data validation, multi-agent worktree experiments, deterministic review/repair gates |
| **Model systems** | Raw checkpoint parsing, MoE routing analysis, GGUF/Safetensors tooling, route-preserving quantization experiments |
| **Systems engineering** | Rust-first CLIs/runtimes, Python data/eval tooling, CUDA/GPU validation, CI, reproducible artifacts |
| **External OSS** | Merged xAI/Grok provider work in `agent-afk`, including API-key + OAuth support and a later compatibility fix |
| **Public artifacts** | Hugging Face datasets, telemetry corpora, Grok-1 research packs, manifests, experiment reports |
| **Research specialty** | SNN / neuromorphic runtimes, telemetry-driven control, FPGA-oriented export and validation |

### What I optimize for

**Measurable results · reproducibility · provenance · fail-closed validation · explicit scope boundaries · humans merge**

---

## Selected engineering proof

### Upstream open-source contributions

- **[`agent-afk` PR #1019 — first-class xAI/Grok provider](https://github.com/griffinwork40/agent-afk/pull/1019)** — merged. Added API-key and SuperGrok OAuth paths, provider selection, credential handling, docs, and tests in an external codebase.
- **[`agent-afk` PR #1242 — xAI OAuth CLI-version compatibility](https://github.com/griffinwork40/agent-afk/pull/1242)** — merged. Fixed proxy-version negotiation with validated overrides/fallbacks and project-wide validation.

These matter to me because they test a different skill than owning my own repositories: **understanding another project's architecture, satisfying its contracts, and getting work accepted upstream.**

### Public ML / data artifacts

- **[Hugging Face portfolio](https://huggingface.co/rmems)** — public model, dataset, telemetry, and research artifacts.
- **[Grok-1 GOZ1 research packs](https://huggingface.co/datasets/rmems/grok-1-goz1-packs)** — packaged Grok-1 quantization research artifacts with manifests/provenance.
- **[Agentic Coding Trajectories](https://huggingface.co/datasets/rmems/agentic-coding-trajectories)** — observable coding-agent trajectories for evaluation/training research.
- **[Spikenaut SNN Telemetry](https://huggingface.co/datasets/rmems/Spikenaut-SNN-v2-Telemetry-Data-Weights-Parameters)** — machine telemetry and neuromorphic research data.

---

## Flagship projects

| Project | What it demonstrates |
|---|---|
| **[xai-dissect](https://github.com/rmems/xai-dissect)** | Rust CLI for read-only structural analysis of open Grok-1 checkpoints: raw shard parsing, tensor inventory, MoE expert/routing maps, statistics, and machine-readable manifests |
| **[synthetic-factory](https://github.com/rmems/synthetic-factory)** | Synthetic-data generation and curation with schemas, provenance, strict audit gates, failure-oriented fixtures, and public Hugging Face release plumbing |
| **[operation-prometheus](https://github.com/rmems/operation-prometheus)** | Software-engineering trajectory forge: `issue → implementation → review → fix → validation → merge` datasets for coding-agent research |
| **[grok-ozempic](https://github.com/rmems/grok-ozempic)** | Real Grok-1 compression experiments focused on expert precision, routing fidelity, residual drift, and reproducible comparison reports |
| **[corinth-canal](https://github.com/rmems/corinth-canal)** | End-to-end Rust reference pipeline spanning telemetry encoding, spiking hidden state, projection, GGUF/Safetensors model inspection, MoE routing, and SAAQ validation |
| **[Spikenaut-SNN](https://github.com/rmems/Spikenaut-SNN)** | From-scratch SNN research runtime and export target for telemetry / neuromorphic experiments |

### Shared libraries

I also maintain modular libraries under **[Limen Neural](https://github.com/Limen-Neural)**, including projects such as **[neuromod](https://github.com/Limen-Neural/neuromod)**, **[axon-encoder](https://github.com/Limen-Neural/axon-encoder)**, **[nir-rs](https://github.com/Limen-Neural/nir-rs)**, **[synaptic-mesh](https://github.com/Limen-Neural/synaptic-mesh)**, and **[brainstem-daemon](https://github.com/Limen-Neural/brainstem-daemon)**.

---

## Technical focus

**Languages**

`Rust` · `Python` · `Julia` · `CUDA C/C++` · `SystemVerilog`

**ML / model systems**

`PyTorch` · `Hugging Face` · `MoE` · `GGUF` · `Safetensors` · `LoRA/QLoRA` · quantization experiments · SNN / neuromorphic systems

**Engineering / infrastructure**

GitHub Actions · Docker · Linux · self-hosted GPU CI · structured JSON/JSONL/Parquet artifacts · reproducible experiment manifests · automated review gates

**Local research hardware**

NVIDIA RTX 5080 16 GiB · AMD Ryzen 9 9950X · Fedora Linux

---

## How I work with AI coding agents

I use coding agents heavily, but I do not treat generated output as ground truth.

Typical flow:

```text
issue / hypothesis
      ↓
isolated branch or worktree
      ↓
implementation
      ↓
local tests / lint / benchmark / experiment gate
      ↓
pull request
      ↓
independent review + repair
      ↓
human merge / release decision
```

Agent assistance is **explicitly attributed** in PRs, commit trailers, experiment notes, or release provenance where appropriate. I care about being able to explain and reproduce the result—not about pretending the tools were not used.

---

## Research programs

The repositories compose into five broader programs. Recruiters do **not** need to read all five to understand the flagship work above; these links are the deeper map.

1. **[Autonomous Software Engineering](https://github.com/users/rmems/projects/9)** — coding-agent worktrees, evaluation, engineering trajectories, review/repair loops.
2. **[Frontier Model Systems & Compression](https://github.com/users/rmems/projects/6)** — Grok-1 structural analysis, routing fidelity, quantization, SAAQ, GGUF/Safetensors tooling.
3. **[Artificial Neuromorphic Supervisor for LLMs](https://github.com/users/rmems/projects/10)** — event-driven/SNN state for resource-aware agents; deterministic systems retain safety authority.
4. **[Agoge Model Forge](https://github.com/users/rmems/projects/8)** — engineering trajectories → post-training → evaluation → export/serve.
5. **[Theseus Machine Physiology](https://github.com/users/rmems/projects/7)** — GPU/CPU/power/VRAM telemetry and machine-state datasets for model/control experiments.

### System map

```text
Machine telemetry / physiology
        ↓
Event-driven / SNN state
        ↓
Agents + LLM systems
        ↑
Agent evaluation + engineering trajectories
        ↑
Model analysis / compression / post-training
```

---

## Current priorities

- **Agent evaluation:** measurable coding-agent tasks, trajectories, graders, and failure analysis.
- **ML systems:** checkpoint tooling, model-format infrastructure, quantization experiments, routing fidelity.
- **Post-training:** connect curated engineering trajectories to reproducible training/evaluation loops.
- **Neuromorphic research:** keep SNN work grounded in measurable telemetry/runtime experiments rather than biological imitation claims.

---

## README attribution

Primary author and maintainer: **Raul Montoya Cardenas (`rmems`)**.

Recruiter-focused structure and editorial rewrite co-authored on **2026-08-21** with **OpenAI ChatGPT — GPT-5.6 Sol**. Project-specific AI contributions remain attributed in their respective commits, PRs, experiment records, and release provenance.
