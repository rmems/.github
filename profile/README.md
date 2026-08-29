# Raul Montoya Cardenas

**Early-Career AI / Research Engineer | Agentic Systems, Synthetic Data & Model Evaluation**

**B.S. AI Engineering, Western Governors University — Expected Sept. 2027**

San Marcos, Texas · montoyaraul34@gmail.com

[GitHub Projects](https://github.com/rmems?tab=projects) · [Hugging Face](https://huggingface.co/rmems) · [Limen Neural](https://github.com/Limen-Neural)

> *Building reproducible post-training experiments, synthetic-data research, and agentic evaluation systems on hardware I can own.*

I am an **early-career AI / research engineer** focused on **agentic systems, synthetic-data research, post-training evaluation, and reproducible ML experiments**. I build the surrounding infrastructure in Python, Rust, CUDA, and related systems languages: synthetic-data generation and curation, real software-engineering trajectory extraction, rights/provenance gates, held-out model evaluation, open-weight checkpoint analysis, model-format tooling, and neuromorphic runtimes.

My current research question is straightforward to state and difficult to answer well:

> **How do rights-cleared synthetic supervision, real engineering trajectories, provenance-aware curation, executable validation, and data mixing change downstream model behavior — while frontier hosted models remain research-only comparators rather than training sources?**

My current hiring focus is **early-career AI / research engineering roles in agentic systems, model evaluation, ML systems, post-training infrastructure, and model tooling**. Neuromorphic computing remains a specialist research track rather than a prerequisite for understanding the rest of the portfolio.

---

## Current research program

The current work is intentionally split into separate systems so that frontier-model research, training-candidate data, real-world evidence, training, and evaluation do not collapse into one opaque pipeline.

```text
Frontier hosted models
OpenAI · Anthropic · xAI · Meta
        ↓
matched research campaigns
quality / failure / validator / cost comparisons
        ↓
research artifacts only
(no SFT / DPO / RL / distillation / weight updates)

Rights-cleared training candidates ───────┐
DeepSeek channels with pinned terms       │
local/open-weight generators              ├─→ Synthetic Factory
                                          │   provenance → validation → curation
Operation Prometheus ─────────────────────┘
real engineering trajectories
                  ↓
          Agoge Model Forge
      frozen splits → SFT → held-out eval
                  ↓
          measured model behavior
```

This separation is now an explicit project-policy boundary in **[Synthetic Factory #161](https://github.com/rmems/synthetic-factory/issues/161)**: hosted outputs from OpenAI, Anthropic, SpaceXAI/xAI, and Meta are **research-only** in this program. Their exact retention, evaluation, attribution, and redistribution rights remain evidence-gated by provider/channel/date, but they do not enter any model-weight update path.

The production training corpus instead moves toward sources whose intended use can be defended directly: **rights-cleared DeepSeek/API channels after first-party terms snapshots are pinned, local/open-weight generators under compatible licenses, and Operation Prometheus trajectories extracted from owned or permissively licensed engineering history**. Unknown provenance fails closed.

### Planned first controlled study

The first study is designed to compare the same open-weight starting checkpoint under matched, reproducible conditions using **training-candidate sources that independently pass the rights/project-policy gate**:

| Arm | Training condition |
|---|---|
| **A** | Untouched starting checkpoint |
| **B** | Minimally curated rights-cleared synthetic supervision |
| **C** | Synthetic-Factory-curated rights-cleared synthetic supervision |
| **D** | Owned or permissively licensed real-world software-engineering trajectories |
| **E** | Curated synthetic + real-world mixture |

The primary question is **not which frontier generator “wins.”** Claude Fable 5, Grok 4.6, GPT-5.6-Sol, Muse Spark 1.2, and future hosted frontier systems are used as **matched research comparators** for measurements such as schema-valid yield, executable/oracle pass rate, repair behavior, trajectory diversity, failure modes, and cost/latency efficiency. Outputs from the explicitly policy-blocked OpenAI, Anthropic, xAI, and Meta provider families are deliberately excluded from training exports; other hosted-provider outputs, including DeepSeek, are eligible only after the exact channel independently passes the rights/project-policy gate.

The first bounded training run is local-first on an **RTX 5080 16 GiB**. Larger cloud runs, repeated seeds, ablations, and bigger checkpoints come only after the rights-cleared dataset → training → held-out-evaluation path is reproducible.

**No result is claimed in advance.** Improvement, degradation, mixed behavior, null results, and inconclusive runs are all valid experiment outcomes if the contract is frozen before results are inspected.

---

## Recruiter snapshot

| Area | Evidence |
|---|---|
| **Agentic systems & evals** | Coding-agent trajectories, multi-agent worktree experiments, deterministic review/repair gates, executable task verification |
| **Synthetic data & post-training** | Synthetic Factory provenance/rights gates + Agoge frozen splits, SFT manifests, base-vs-SFT held-out evaluation, and reproducible experiment artifacts |
| **Real-world training evidence** | Operation Prometheus event-sourced software-engineering trajectories from public issues, patches, review, fixes, CI, and merge history |
| **Model systems** | Raw checkpoint parsing, MoE routing analysis, GGUF/Safetensors tooling, route-preserving quantization experiments |
| **Systems engineering** | Rust-first CLIs/runtimes, Python data/eval tooling, CUDA/GPU validation, CI, reproducible artifacts |
| **External OSS** | Shipped upstream xAI/Grok provider work in `agent-afk` plus Devin/Linux usage telemetry in UsagePal v0.7.70 |
| **Research specialty** | SNN / neuromorphic runtimes, telemetry-driven control, oracle-grounded simulation, FPGA-oriented export and validation |

### What I optimize for

**Measurable results · reproducibility · provenance · rights-aware data lineage · fail-closed validation · leakage-resistant evaluation · explicit scope boundaries · humans merge**

---

## Selected engineering proof

### Upstream open-source contributions

- **[`UsagePal` PR #48 — Devin Linux support + richer usage telemetry](https://github.com/Halloweedev/usagepal/pull/48)** — merged upstream and shipped into the project's v0.7.70 release line. Added Linux credential discovery, Devin/Devin-Next SQLite auth paths, `DEVIN_API_KEY` fallback, ACU/quota/credit tracking, pace indicators, non-macOS panel groundwork, docs, and tests. The upstream changelog explicitly attributes the shipped Devin/Linux work to `@rmems`.
- **[`agent-afk` PR #1019 — first-class xAI/Grok provider](https://github.com/griffinwork40/agent-afk/pull/1019)** — merged. Added API-key and SuperGrok OAuth paths, provider selection, credential handling, docs, and tests in an external codebase.
- **[`agent-afk` PR #1242 — xAI OAuth CLI-version compatibility](https://github.com/griffinwork40/agent-afk/pull/1242)** — merged. Fixed proxy-version negotiation with validated overrides/fallbacks and project-wide validation.

These matter to me because they test a different skill than owning my own repositories: **understanding another project's architecture, satisfying its contracts, and getting work accepted and shipped upstream.**

### Public ML / data artifacts

- **[Hugging Face portfolio](https://huggingface.co/rmems)** — public model, dataset, telemetry, and research artifacts.
- **[Grok-1 GOZ1 research packs](https://huggingface.co/datasets/rmems/grok-1-goz1-packs)** — packaged Grok-1 quantization research artifacts with manifests/provenance.
- **[Agentic Coding Trajectories](https://huggingface.co/datasets/rmems/agentic-coding-trajectories)** — public raw coding-agent trajectories for evaluation/research; raw visibility is not a training-eligibility claim.
- **[Thalamic Relay Trajectories](https://huggingface.co/datasets/rmems/thalamic-relay-trajectories)** — early neuromorphic/safety-gating synthetic trajectories with explicit raw-vs-curated separation.
- **[Neuromorphic Event-Language Bridge](https://huggingface.co/datasets/rmems/neuromorphic-event-language-bridge)** — event-stream ↔ structured-language grounding artifacts for future oracle-grounded neuromorphic experiments.
- **[Spikenaut SNN Telemetry](https://huggingface.co/datasets/rmems/Spikenaut-SNN-Telemetry)** — machine telemetry and neuromorphic research data.

---

## Flagship projects

| Project | What it demonstrates |
|---|---|
| **[synthetic-factory](https://github.com/rmems/synthetic-factory)** | Synthetic-data research and curation with append-only raw evidence, provider/channel/date provenance, rights + project-policy gates, research-only frontier lanes, training-candidate routing, strict audit gates, failure-oriented fixtures, and Hugging Face release plumbing |
| **[operation-prometheus](https://github.com/rmems/operation-prometheus)** | Real software-engineering trajectory forge: `issue → implementation → review → fix → validation → merge`, with lineage-safe data/eval design and a primary path toward rights-defensible training evidence |
| **[agoge-forger](https://github.com/rmems/agoge-forger)** | Reproducible post-training/evaluation forge: local LoRA/QLoRA, immutable split contracts, checkpoints/manifests, base-vs-SFT held-out evaluation, and later cloud/distributed lanes; consumes only training-candidate data that passes upstream gates |
| **[xai-dissect](https://github.com/rmems/xai-dissect)** | Rust CLI for read-only structural analysis of open Grok-1 checkpoints: raw shard parsing, tensor inventory, MoE expert/routing maps, statistics, and machine-readable manifests |
| **[grok-ozempic](https://github.com/rmems/grok-ozempic)** | Grok-1 compression experiments focused on expert precision, routing fidelity, residual drift, and reproducible comparison reports |
| **[corinth-canal](https://github.com/rmems/corinth-canal)** | End-to-end Rust reference pipeline spanning telemetry encoding, spiking hidden state, projection, GGUF/Safetensors model inspection, MoE routing, and SAAQ validation |
| **[Spikenaut-SNN](https://github.com/rmems/Spikenaut-SNN)** | From-scratch SNN research runtime and export target for telemetry / neuromorphic experiments |

### Shared libraries

I also maintain modular libraries under **[Limen Neural](https://github.com/Limen-Neural)**, including projects such as **[neuromod](https://github.com/Limen-Neural/neuromod)**, **[axon-encoder](https://github.com/Limen-Neural/axon-encoder)**, **[nir-rs](https://github.com/Limen-Neural/nir-rs)**, **[synaptic-mesh](https://github.com/Limen-Neural/synaptic-mesh)**, and **[brainstem-daemon](https://github.com/Limen-Neural/brainstem-daemon)**.

---

## Technical focus

**Languages**

`Rust` · `Python` · `Julia` · `CUDA C/C++` · `SystemVerilog`

**ML / model systems**

`PyTorch` · `Hugging Face` · `LoRA/QLoRA` · `MoE` · `GGUF` · `Safetensors` · quantization experiments · SNN / neuromorphic systems

**Experiment / data systems**

Immutable dataset manifests · provider/channel/date provenance · rights/project-policy gates · train/validation/held-out splits · leakage guards · deterministic/executable scoring · raw-vs-curated separation · JSON/JSONL/Parquet artifacts

**Engineering / infrastructure**

GitHub Actions · Docker · Linux · self-hosted GPU CI · Terraform experiments · cloud-training scaffolding · automated review gates

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

The same principle drives the research data work:

> **Frontier models may provide research comparisons; executable evidence, validated oracles, provenance/rights gates, and held-out evaluation determine what can become training evidence and what the evidence actually supports.**

---

## Research programs

The repositories compose into five broader programs. Recruiters do **not** need to read all five to understand the flagship work above; these links are the deeper map.

1. **[Autonomous Software Engineering](https://github.com/users/rmems/projects/9)** — coding-agent worktrees, evaluation, engineering trajectories, review/repair loops.
2. **[Frontier Model Systems & Compression](https://github.com/users/rmems/projects/6)** — Grok-1 structural analysis, routing fidelity, quantization, SAAQ, GGUF/Safetensors tooling.
3. **[Artificial Neuromorphic Supervisor for LLMs](https://github.com/users/rmems/projects/10)** — event-driven/SNN state for resource-aware agents; deterministic systems retain safety authority.
4. **[Agoge Model Forge](https://github.com/users/rmems/projects/8)** — rights-cleared engineering/synthetic trajectories → post-training → evaluation → export/serve.
5. **[Theseus Machine Physiology](https://github.com/users/rmems/projects/7)** — GPU/CPU/power/VRAM telemetry and machine-state datasets for model/control experiments.

### System map

```text
Frontier hosted models → matched research/eval campaigns → comparative reports
                         (research-only; no weight-update path)

Rights-cleared synthetic candidates ──────┐
                                          ├─→ curation / provenance gates ──┐
Real engineering history ─────────────────┘                                │
                                                                           ↓
                                                                   post-training + eval
                                                                           ↓
                                                                  measured model behavior

Machine telemetry → event-driven / SNN state → neuromorphic transfer experiments
```

---

## Current priorities

1. **Enforce the research-only frontier boundary** — implement Synthetic Factory #161 so OpenAI/Anthropic/xAI/Meta hosted outputs cannot enter SFT, DPO, RL, distillation, continued-pretraining, or other weight-update/export paths; keep research/redistribution status evidence-gated and fail closed.
2. **Build a defensible training-candidate slice** — prioritize Operation Prometheus plus local/open-weight sources and only add hosted production teachers such as DeepSeek after the exact channel's first-party terms and intended downstream use are pinned.
3. **Freeze the first experiment contract** — immutable train/validation/held-out splits, leakage guards, exact model/tokenizer revisions, metrics, seeds, and success/null criteria.
4. **Run the first local base → SFT → held-out comparison** — preserve training telemetry, checkpoints, generations, regressions, and reproducibility artifacts.
5. **Scale only after the baseline is reproducible** — repeated seeds, ablations, synthetic/real mixture studies, then bounded cloud and larger-model experiments; keep neuromorphic work as a transfer domain with authoritative simulator/hardware labels.

---

## README attribution

Primary author and maintainer: **Raul Montoya Cardenas (`rmems`)**.

Recruiter-focused structure and editorial rewrite co-authored on **2026-08-21** with **OpenAI ChatGPT — GPT-5.6 Sol**. Research-program refresh co-authored on **2026-08-28** with **OpenAI ChatGPT — GPT-5.6 Sol**. Rights/provenance policy + shipped-OSS refresh co-authored on **2026-08-29** with **OpenAI ChatGPT — GPT-5.6 Sol**. Project-specific AI contributions remain attributed in their respective commits, PRs, experiment records, and release provenance.
