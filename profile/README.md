# Raul Montoya Cardenas

San Marcos, Texas · montoyaraul34@gmail.com

---

> *Making large models run on hardware you can actually own.*

**AI engineering student** and independent researcher building systems where **coding agents can go further with less babysitting** — and where **model/hardware research stays measurable, reproducible, and safety-bounded**.

I coined **SAAQ** (*Spiking Adaptive Activity Quantization*) while starting early pipeline work ([corinth-canal](https://github.com/rmems/corinth-canal), [Surrogate_Viz.jl](https://github.com/rmems/Surrogate_Viz.jl)): study and compress large MoE models with spiking / neuromorphic ideas on hardware I own (e.g. RTX 5080). I am still learning Julia, Rust, Python, and CUDA. **Pursuing AI Engineering @ WGU.**

[rmems](https://github.com/rmems) · [Limen Neural](https://github.com/Limen-Neural) · [GitHub Projects](https://github.com/rmems?tab=projects)

---

## One system, many repos

This portfolio started as an **oversized research workspace**, then spilled into a noisy org catalog. The work was **modularized** so each repository has a clear job — but the pieces are meant to **compose into one system**, not sit as unrelated demos.

The public map is my [GitHub Projects](https://github.com/rmems?tab=projects) board. In short:

```text
Theseus physiology (telemetry + safety governor)
        ↓
SNN / temporal “nervous system” (Spikenaut + Julia SNN stack)
        ↓  works alongside / attaches to
Agents + LLMs (Autonomous SE + resource-aware control)
        ↑
Frontier compression (SAAQ, Grok MoE path) → smaller / spiking-friendly models
        ↑
Agoge forge (train/eval from engineering trajectories)
```

**Hard invariants I care about more than demo vibes:** no silent auto-merge · bounded repair · provenance · measurable gates (CI on pull requests and pushes).

---

## Research programs

Same five programs as LinkedIn and the Projects tab.

### 1. [Autonomous Software Engineering](https://github.com/users/rmems/projects/9)

Multi-agent Git worktree execution, engineering-trajectory collection, review/repair loops, and local agent evaluation — so agents ship further with less babysitting. **Humans merge.**

| | |
|---|---|
| [**worktrees-hives**](https://github.com/rmems/worktrees-hives) | Early/experimental multi-agent lab in isolated git worktrees; mandatory findings; **never auto-merges** |
| [**operation-prometheus**](https://github.com/rmems/operation-prometheus) | Engineering trajectories (issue→review→patch→validation) for local coding agents |
| [**NeuralForge-Memory**](https://github.com/rmems/NeuralForge-Memory) | Experimental RAG / vector DB with MCP |

---

### 2. [Frontier Model Systems & Compression](https://github.com/users/rmems/projects/6)

Open-weight MoE research on real Grok-1 checkpoints: structural dissection, **route-preserving** quantization / **SAAQ**, and compression that tracks **routing fidelity** — not just file size.

| | |
|---|---|
| [**magere-brug**](https://github.com/rmems/magere-brug) | SAAQ lab — recipes, manifests, hybrid MoE/SNN experiments |
| [**corinth-canal**](https://github.com/rmems/corinth-canal) | SAAQ reference pipeline (Rust) |
| [**xai-dissect**](https://github.com/rmems/xai-dissect) | Inspect raw open-weight Grok-1 shards (Rust CLI) |
| [**grok-ozempic**](https://github.com/rmems/grok-ozempic) | Grok-scale SNN-style quantization experiments |
| [**XAIDissect_Viz.jl**](https://github.com/rmems/XAIDissect_Viz.jl) | Viz of MoE routing / xai-dissect reports |
| [**hybrid-fusion**](https://github.com/rmems/hybrid-fusion) · [**engram-parser**](https://github.com/rmems/engram-parser) | MoE→SNN path: hybrid architecture + extract expert “memories” for transfer |
| [**combine-for-AI**](https://github.com/rmems/combine-for-AI) | Neutral quant benchmark harness (accuracy, latency, VRAM, routing, …) |
| [**Surrogate_Viz.jl**](https://github.com/rmems/Surrogate_Viz.jl) | Symbolic regression on telemetry (co-origin of the SAAQ term) |

---

### 3. [Artificial Neuromorphic Supervisor for LLMs](https://github.com/users/rmems/projects/10)

Event-driven / **SNN** layers that compress machine telemetry into a **small internal state** so agents can be **resource-aware**. The goal is an SNN (or event-driven model) that **runs alongside an LLM / agent stack** — a **nervous system**, not a full biological imitation. **Learned systems propose; deterministic systems protect** (hard thermal / resource safety is never overridden by a learned policy). FPGA / HDL work is a **deployment path** for that nervous system later, not the whole program.

| | |
|---|---|
| [**Spikenaut-SNN**](https://github.com/rmems/Spikenaut-SNN) | Own SNN from scratch — candidate “nervous system” / transfer target for MoE expert blocks |
| [**LiquidCortex.jl**](https://github.com/rmems/LiquidCortex.jl) · [**SpikeStream.jl**](https://github.com/rmems/SpikeStream.jl) · [**NeuroPulse.jl**](https://github.com/rmems/NeuroPulse.jl) · [**TemporalFocus.jl**](https://github.com/rmems/TemporalFocus.jl) · [**SynapticDistill.jl**](https://github.com/rmems/SynapticDistill.jl) | Julia SNN / temporal stack (LSM, streaming features, relevance, spike-coincidence attention, FPGA distillation) |
| [**silicon-hdl**](https://github.com/rmems/silicon-hdl) · [**silicon-bridge**](https://github.com/rmems/silicon-bridge) | Optional export path to small FPGA targets (learning field, not production HFT silicon) |
| [**blackwell-kernel-lab**](https://github.com/rmems/blackwell-kernel-lab) | Local GPU path on NVIDIA Blackwell / RTX 5080 for agentic + neuromorphic experiments |
| [**spike-viz**](https://github.com/rmems/spike-viz) | Visualize SNN encodings and activity |

Telemetry inputs come from **Theseus Machine Physiology** (below).

---

### 4. [Agoge Model Forge](https://github.com/users/rmems/projects/8)

Local-first post-training bridge: software-engineering trajectories → LoRA/QLoRA → eval → export/serve.

| | |
|---|---|
| [**agoge-forger**](https://github.com/rmems/agoge-forger) | Training forge (PyTorch-first; Rust/JAX options) |
| [**operation-prometheus**](https://github.com/rmems/operation-prometheus) | Upstream trajectory datasets that feed the forge |

---

### 5. [Theseus Machine Physiology](https://github.com/users/rmems/projects/7)

GPU/CPU/power/VRAM telemetry and machine-state datasets under a **Rust safety governor**. Mining is one sustained physiology source — not the whole program.

| | |
|---|---|
| [**gaming-telemetry**](https://github.com/rmems/gaming-telemetry) | High-load GPU telemetry for neuromorphic research |
| [**Theseus-Quarry**](https://github.com/rmems/Theseus-Quarry) | Mining / ops telemetry extraction |
| [**spikenaut-telemetry-etl**](https://github.com/rmems/spikenaut-telemetry-etl) | Fail-loud cleaning toward published datasets |
| [**thalamic-relay**](https://github.com/rmems/thalamic-relay) | Rust hardware orchestration relay (compute telemetry → SNN drive) |
| [**Ship-of-Theseus-HPC**](https://github.com/rmems/Ship-of-Theseus-HPC) | Workstation notes and hardware diagnostics |

---

## Why modular? ([Limen-Neural Consolidation](https://github.com/users/rmems/projects/5))

Selected repos moved from the [Limen-Neural](https://github.com/Limen-Neural) org back under [rmems](https://github.com/rmems) so this reads as a **personal research portfolio**, not a catch-all product org. The org keeps **shared libraries** maturing toward publish (**[neuromod](https://github.com/Limen-Neural/neuromod) v0.5.1 on crates.io** today; others such as [nir-rs](https://github.com/Limen-Neural/nir-rs), [brainstem-daemon](https://github.com/Limen-Neural/brainstem-daemon), [myelin-accelerator](https://github.com/Limen-Neural/myelin-accelerator), [axon-encoder](https://github.com/Limen-Neural/axon-encoder) still in progress).

Experimental SNN-HFT research hub: [**Limen-Capital**](https://github.com/rmems/Limen-Capital) (+ related signal/ledger crates). **Not live capital.**

Cloud training scaffold (future): [**Dioscuri-Cloud**](https://github.com/rmems/Dioscuri-Cloud).

---

## How I work

I normally go from **issue → pull request**, either from a **local CLI** or through **Linear** (cloud).

- **Agents** day to day: Grok Build, Codex, Claude, Cursor, Devin, Kilo, OpenCode, and others — plus shared memory (Ogham / Chroma). **Humans merge.**  
- **PR review** (rough order): Codex → CodeRabbit → Devin when I want a strong extra pass → Cursor Bugbot · Copilot · CodeAnt · Qodana (local + cloud). I still spot-check with textbooks / local judgment — bots are not ground truth.  
- **Before open/push:** local checks from each repo’s **`REVIEW.md`** and **Qodana CLI** when available.  
- **CI:** GitHub Actions on **pull requests and pushes** — early feedback and a rough benchmark of agent (and human) implementations.

---

## Currently

- **Autonomous SE:** worktrees-hives (early/experimental) + operation-prometheus  
- **Frontier compression / SAAQ:** magere-brug + corinth-canal; Grok path via xai-dissect / grok-ozempic  
- **SNN as nervous system for agents:** Spikenaut-SNN + Julia SNN stack; safety stays deterministic  
- **Physiology inputs:** Theseus telemetry path under a safety governor  
- **Agoge forge:** local post-training bridge from SE trajectories  
- **Education:** Pursuing AI Engineering @ WGU  

---

<sub>README updated by me (rmems) and with Grok Build: Grok 4.5 (high)</sub>
