# Raul Montoya Cardenas

**Early-Career AI / Research Engineer | Agentic Systems, Synthetic Data & Model Evaluation**

**B.S. AI Engineering, Western Governors University — Expected Sept. 2027**

San Marcos, Texas · montoyaraul34@gmail.com

[GitHub Projects](https://github.com/rmems?tab=projects) · [Hugging Face](https://huggingface.co/rmems) · [Limen Neural](https://github.com/Limen-Neural)

> *Building reproducible post-training experiments, synthetic-data curation, and agentic evaluation systems on hardware I can own.*

I am an **early-career AI / research engineer** focused on **agentic systems, synthetic training data, post-training evaluation, and reproducible ML experiments**. I build the surrounding infrastructure in Python, Rust, CUDA, and related systems languages: synthetic-data generation and curation, real software-engineering trajectory extraction, held-out model evaluation, open-weight checkpoint analysis, model-format tooling, and neuromorphic runtimes.

My current research question is straightforward to state and difficult to answer well:

> **When does model-generated supervision improve a model, when does it degrade behavior, and can provenance-aware curation, executable validation, and human/synthetic data mixing change that outcome?**

My current hiring focus is **early-career AI / research engineering roles in agentic systems, model evaluation, ML systems, post-training infrastructure, and model tooling**. Neuromorphic computing remains a specialist research track rather than a prerequisite for understanding the rest of the portfolio.

---

## Current research program

The current work is intentionally split into separate systems so that generation, real-world evidence, training, and evaluation do not collapse into one opaque pipeline.

```text
Synthetic Factory
synthetic generation → provenance → validation → curation
                         ↓
Operation Prometheus     ↓
real engineering history ↓
        \                /
         \              /
          Agoge Model Forge
      frozen splits → SFT → held-out eval
                  ↓
          measured model behavior
```

### Planned first controlled study

The first study is designed to compare the same open-weight starting checkpoint under matched, reproducible conditions:

| Arm | Training condition |
|---|---|
| **A** | Untouched starting checkpoint |
| **B** | Minimally curated synthetic supervision |
| **C** | Synthetic-Factory-curated synthetic supervision |
| **D** | Public real-world software-engineering trajectories |
| **E** | Curated synthetic + real-world mixture |

The primary question is **not which frontier generator “wins.”** Claude Fable 5, Grok 4.6, GPT-5.6-Sol, Muse Spark 1.2, and future generators are potential sources of raw synthetic supervision. The experiment is about whether the **pipeline, curation strategy, and data mixture** produce different downstream outcomes.

The first bounded run is local-first on an **RTX 5080 16 GiB**. Larger cloud runs, repeated seeds, ablations, and bigger checkpoints come only after the local dataset → training → held-out-evaluation path is reproducible.

**No result is claimed in advance.** Improvement, degradation, mixed behavior, null results, and inconclusive runs are all valid experiment outcomes if the contract is frozen before results are inspected.

---

## Recruiter snapshot

| Area | Evidence |
|---|---|
| **Agentic systems & evals** | Coding-agent trajectories, multi-agent worktree experiments, deterministic review/repair gates, executable task verification |
| **Synthetic data & post-training** | Synthetic Factory curation gates + Agoge frozen splits, SFT manifests, base-vs-SFT held-out evaluation, and reproducible experiment artifacts |
| **Real-world training evidence** | Operation Prometheus event-sourced software-engineering trajectories from public issues, patches, review, fixes, CI, and merge history |
| **Model systems** | Raw checkpoint parsing, MoE routing analysis, GGUF/Safetensors tooling, route-preserving quantization experiments |
| **Systems engineering** | Rust-first CLIs/runtimes, Python data/eval tooling, CUDA/GPU validation, CI, reproducible artifacts |
| **External OSS** | Merged xAI/Grok provider work in `agent-afk`, including API-key + OAuth support and a later compatibility fix |
| **Research specialty** | SNN / neuromorphic runtimes, telemetry-driven control, oracle-grounded simulation, FPGA-oriented export and validation |

### What I optimize for

**Measurable results · reproducibility · provenance · fail-closed validation · leakage-resistant evaluation · explicit scope boundaries · humans merge**

---

## Selected engineering proof

### Upstream open-source contributions

- **[`agent-afk` PR #1019 — first-class xAI/Grok provider](https://github.com/griffinwork40/agent-afk/pull/1019)** — merged. Added API-key and SuperGrok OAuth paths, provider selection, credential handling, docs, and tests in an external codebase.
- **[`agent-afk` PR #1242 — xAI OAuth CLI-version compatibility](https://github.com/griffinwork40/agent-afk/pull/1242)** — merged. Fixed proxy-version negotiation with validated overrides/fallbacks and project-wide validation.

These matter to me because they test a different skill than owning my own repositories: **understanding another project's architecture, satisfying its contracts, and getting work accepted upstream.**

### Public ML / data artifacts

- **[Hugging Face portfolio](https://huggingface.co/rmems)** — public model, dataset, telemetry, and research artifacts.
- **[Grok-1 GOZ1 research packs](https://huggingface.co/datasets/rmems/grok-1-goz1-packs)** — packaged Grok-1 quantization research artifacts with manifests/provenance.
- **[Agentic Coding Trajectories](https://huggingface.co/datasets/rmems/agentic-coding-trajectories)** — public raw coding-agent trajectories for evaluation/training research; raw visibility is not a training-readiness claim.
- **[Thalamic Relay Trajectories](https://huggingface.co/datasets/rmems/thalamic-relay-trajectories)** — early neuromorphic/safety-gating synthetic trajectories with explicit raw-vs-curated separation.
- **[Neuromorphic Event-Language Bridge](https://huggingface.co/datasets/rmems/neuromorphic-event-language-bridge)** — event-stream ↔ structured-language grounding artifacts for future oracle-grounded neuromorphic experiments.
- **[Spikenaut SNN Telemetry](https://huggingface.co/datasets/rmems/Spikenaut-SNN-Telemetry)** — machine telemetry and neuromorphic research data.

---

## Flagship projects

| Project | What it demonstrates |
|---|---|
| **[synthetic-factory](https://github.com/rmems/synthetic-factory)** | Synthetic-data generation and curation with append-only raw evidence, provenance, payload-kind routing, strict audit gates, failure-oriented fixtures, and Hugging Face release plumbing |
| **[operation-prometheus](https://github.com/rmems/operation-prometheus)** | Real software-engineering trajectory forge: `issue → implementation → review → fix → validation → merge`, with lineage-safe data/eval design |
| **[agoge-forger](https://github.com/rmems/agoge-forger)** | Reproducible post-training/evaluation forge: local LoRA/QLoRA, immutable split contracts, checkpoints/manifests, base-vs-SFT held-out evaluation, and later cloud/distributed lanes |
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

Immutable dataset manifests · train/validation/held-out splits · leakage guards · deterministic/executable scoring · raw-vs-curated provenance · JSON/JSONL/Parquet artifacts

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

> **Models may propose examples; executable evidence, validated oracles, curation gates, and held-out evaluation decide what the evidence actually supports.**

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
Synthetic generation ──────┐
                           ├─→ curated supervision ──┐
Real engineering history ──┘                        │
                                                    ↓
                                            post-training + eval
                                                    ↓
                                           measured model behavior

Machine telemetry → event-driven / SNN state → neuromorphic transfer experiments
```

---

## Current priorities

1. **Finish a defensible curated training slice** — strict curation, provenance, payload-kind correctness, deduplication, and sampled review before promotion.
2. **Freeze the first experiment contract** — immutable train/validation/held-out splits, leakage guards, exact model/tokenizer revisions, metrics, seeds, and success/null criteria.
3. **Run the first local base → SFT → held-out comparison** — preserve training telemetry, checkpoints, generations, regressions, and reproducibility artifacts.
4. **Scale only after the baseline is reproducible** — repeated seeds, ablations, synthetic/human mixture studies, then bounded cloud and larger-model experiments.
5. **Use neuromorphic work as a transfer domain** — simulator- and hardware-grounded data where authoritative labels come from validated execution rather than model invention.

---

## README attribution

Primary author and maintainer: **Raul Montoya Cardenas (`rmems`)**.

Recruiter-focused structure and editorial rewrite co-authored on **2026-08-21** with **OpenAI ChatGPT — GPT-5.6 Sol**. Research-program refresh co-authored on **2026-08-28** with **OpenAI ChatGPT — GPT-5.6 Sol**. Project-specific AI contributions remain attributed in their respective commits, PRs, experiment records, and release provenance.
