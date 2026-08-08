# Raul Montoya Cardenas

San Marcos, Texas · montoyaraul34@gmail.com

---

> *Making large models run on hardware you can actually own.*

**AI Systems Engineering** and **Research Engineering** — I research **SAAQ** (**Spiking Adaptive Activity Quantization**), a term I coined while starting [corinth-canal](https://github.com/rmems/corinth-canal) and [Surrogate_Viz.jl](https://github.com/rmems/Surrogate_Viz.jl): ways to study and compress large MoE models with spiking / neuromorphic ideas, mostly on hardware I can run myself (e.g. an RTX 5080). I am still learning to master Julia, Rust, Python, and CUDA. Very interested in agentic infrastructure.

repos: [rmems](https://github.com/rmems) · libraries: [Limen Neural](https://github.com/Limen-Neural)

---

## Why this work

- I built my first workstation for **local AI inference and training**, then hit a hard wall: I still could not run the massive smart models I cared about on hardware I own. That **memory bottleneck** is what pushed me into **spiking neural networks** and neuromorphic ideas as a path to conserve memory and make large models more runnable on personal silicon.
- My passion for neuromorphic computing also comes from a **7th-grade football concussion** — the idea that this line of research might one day help others discover new ways to understand the brain more deeply through neuromorphic computing is what keeps me excited (research motivation, not a medical claim).
- **True north: agentic engineering** — systems so small teams and solo researchers can ship serious work without a giant org. That passion shows up most clearly in [worktrees-hives](https://github.com/rmems/worktrees-hives) and [operation-prometheus](https://github.com/rmems/operation-prometheus). Neuromorphic + SAAQ work sits under that larger systems-engineering identity.

These repos are modular today on purpose, but they are meant to **interact as one system over time**: telemetry → features → Spikenaut / Julia SNN stack → MoE expert transfer → FPGA / Blackwell GPU → agent sandboxes → cloud training scaffold.

---

## Focus

- **Agentic engineering** (primary passion): sandboxes, engineering-trajectory datasets, local GPU, shared memory
- **SAAQ** / MoE→SNN quantization on owned hardware; expert-block transfer into Spikenaut-SNN
- Neuromorphic stacks (Julia + Rust) + FPGA experiments
- Experimental SNN-HFT research — **not live trading**
- Future cloud training path ([Dioscuri-Cloud](https://github.com/rmems/Dioscuri-Cloud) scaffold)

---

## Projects

Many of these once lived under [Limen-Neural](https://github.com/Limen-Neural) as one monolithic workspace. They were modularized, then returned under [rmems](https://github.com/rmems) so personal research stays cohesive and the org keeps shared libraries.

### SAAQ · MoE → SNN · Grok-scale

| | |
|---|---|
| [**magere-brug**](https://github.com/rmems/magere-brug) | SAAQ lab — hybrid MoE/SNN quantization recipes, manifests, experiments |
| [**corinth-canal**](https://github.com/rmems/corinth-canal) | SAAQ reference pipeline (Rust) — MoE architecture → SNN quantization |
| [**Spikenaut-SNN**](https://github.com/rmems/Spikenaut-SNN) | Own SNN model from scratch; destination for MoE expert-block transfer |
| [**hybrid-fusion**](https://github.com/rmems/hybrid-fusion) | Hybrid architecture + MoE→SNN path so parts of expert blocks can transfer into Spikenaut-SNN |
| [**engram-parser**](https://github.com/rmems/engram-parser) | Extract frozen MoE “memories” (weights) into live spiking networks |
| [**cortex-tensor**](https://github.com/rmems/cortex-tensor) | Pure-Rust matrix multiplication and Transformer execution (SpikeLMo lineage) |
| [**xai-dissect**](https://github.com/rmems/xai-dissect) | Inspect raw open-weight Grok-1 JAX/Pickle shards (Rust CLI) |
| [**grok-ozempic**](https://github.com/rmems/grok-ozempic) | Grok-scale SNN-style quantization experiments (full open Grok-1 path) |
| [**XAIDissect_Viz.jl**](https://github.com/rmems/XAIDissect_Viz.jl) | GPU-accelerated viz of Grok-1 MoE routing and xai-dissect reports (CUDA.jl / Blackwell) |
| [**combine-for-AI**](https://github.com/rmems/combine-for-AI) | Neutral quantization benchmark harness (accuracy, throughput, latency, VRAM, routing) |
| [**agoge-forger**](https://github.com/rmems/agoge-forger) | Training forge — PyTorch-first with Rust (Burn, Candle, dfdx) and JAX options |

### Neuromorphic core

| | |
|---|---|
| [**LiquidCortex.jl**](https://github.com/rmems/LiquidCortex.jl) | GPU-accelerated sparse Liquid State Machine — CUDA LSM + STDP |
| [**SpikeStream.jl**](https://github.com/rmems/SpikeStream.jl) | Streaming SNN features (Hurst, Hawkes intensity, GBM surprise Z-score) |
| [**NeuroPulse.jl**](https://github.com/rmems/NeuroPulse.jl) | NERO — multi-lobe SNN relevance scoring with cross-lobe inhibition |
| [**TemporalFocus.jl**](https://github.com/rmems/TemporalFocus.jl) | Spike-coincidence attention kernel (attention as spike-time correlation) |
| [**SynapticDistill.jl**](https://github.com/rmems/SynapticDistill.jl) | Monte Carlo SNN training + FPGA distillation (E-prop, Q8.8 `.mem` export) |
| [**spike-viz**](https://github.com/rmems/spike-viz) | PyTorch + CUDA toolkit for visualizing SNN encodings and activity |

### Hardware · FPGA · workstation

| | |
|---|---|
| [**silicon-hdl**](https://github.com/rmems/silicon-hdl) | Neuromorphic/SNN FPGA primitives (SystemVerilog, Basys 3) — learning field, not production HFT silicon |
| [**silicon-bridge**](https://github.com/rmems/silicon-bridge) | SNN→FPGA deployment (Q8.8 export, Vivado `$readmemh`, UART spike readback) |
| [**thalamic-relay**](https://github.com/rmems/thalamic-relay) | Rust hardware orchestration relay — compute telemetry → SNN drive |
| [**Ship-of-Theseus-HPC**](https://github.com/rmems/Ship-of-Theseus-HPC) | Workstation notes — Bio-MEMS sim, RTL, hardware diagnostics |

### Telemetry · symbolic / viz

| | |
|---|---|
| [**gaming-telemetry**](https://github.com/rmems/gaming-telemetry) | High-demand GPU telemetry (DLSS / path tracing) for neuromorphic research |
| [**Theseus-Quarry**](https://github.com/rmems/Theseus-Quarry) | Crypto mining telemetry extraction for neuromorphic computing |
| [**spikenaut-telemetry-etl**](https://github.com/rmems/spikenaut-telemetry-etl) | Fail-loud cleaning between Theseus-Quarry collectors and published HF datasets |
| [**Surrogate_Viz.jl**](https://github.com/rmems/Surrogate_Viz.jl) | Symbolic regression on telemetry (SymbolicRegression.jl) — co-origin of the SAAQ term |

### Agentic systems · local GPU

| | |
|---|---|
| [**worktrees-hives**](https://github.com/rmems/worktrees-hives) | Multi-agent hypothesis lab in isolated git worktrees; mandatory findings; never auto-merges |
| [**operation-prometheus**](https://github.com/rmems/operation-prometheus) | Engineering-trajectory datasets (issue→review→patch→validation) for local coding agents |
| [**NeuralForge-Memory**](https://github.com/rmems/NeuralForge-Memory) | Experimental RAG / vector DB with MCP |
| [**blackwell-kernel-lab**](https://github.com/rmems/blackwell-kernel-lab) | Local **agentic GPU infrastructure** path on NVIDIA Blackwell / RTX 5080 |

### SNN trading research (not live capital)

Hub: [**Limen-Capital**](https://github.com/rmems/Limen-Capital) — experimental SNN-HFT research stack (Julia neuromorphic brain + Rust execution muscle). **Not live capital.**

| | |
|---|---|
| [**DendriteTrader.jl**](https://github.com/rmems/DendriteTrader.jl) | SNN-based trading research |
| [**kinetic-signals**](https://github.com/rmems/kinetic-signals) | Streaming feature extraction for high-velocity stochastic signals |
| [**limbic-critic**](https://github.com/rmems/limbic-critic) | Modulator mapping — dopamine / serotonin / cortisol-style constrained f32 vectors |
| [**metabolic-ledger**](https://github.com/rmems/metabolic-ledger) | Bio-inspired simulation ledger (ATP metaphors, Kelly energy, metabolic cost) |
| [**corpus-ipc**](https://github.com/rmems/corpus-ipc) | ZMQ float-vector IPC backend (input vectors → output vectors) |

### Libraries ([Limen-Neural](https://github.com/Limen-Neural))

Shared org libraries. Personal modular research lives under [rmems](https://github.com/rmems). **Only [neuromod](https://github.com/Limen-Neural/neuromod) is on crates.io today (v0.5.1)**; the rest are still maturing toward later publish.

| | |
|---|---|
| [**neuromod**](https://github.com/Limen-Neural/neuromod) | Rust SNN library (LIF, Izhikevich, Hebbian, Nagumo, Lapicque, Hodgkin–Huxley) — **crates.io v0.5.1** |
| [**nir-rs**](https://github.com/Limen-Neural/nir-rs) | Pure-Rust Neuromorphic Intermediate Representation (NIR) interchange |
| [**brainstem-daemon**](https://github.com/Limen-Neural/brainstem-daemon) | High-performance headless SNN inference runtime (Rust) |
| [**myelin-accelerator**](https://github.com/Limen-Neural/myelin-accelerator) | CUDA/Rust spiking-network kernels for Blackwell |
| [**axon-encoder**](https://github.com/Limen-Neural/axon-encoder) | SNN sensory preprocessing / neuroscience-inspired encoding abstractions |
| [**synaptic-mesh**](https://github.com/Limen-Neural/synaptic-mesh) | SNN mesh for wiring, topology, and temporal delays |
| [**plasticity-lab**](https://github.com/Limen-Neural/plasticity-lab) | Offline / closed-loop training lab |

### Infrastructure (future)

| | |
|---|---|
| [**Dioscuri-Cloud**](https://github.com/rmems/Dioscuri-Cloud) | Scaffold for future multi-cloud / **cloud training** infrastructure |

Paused: [recoverly-sim](https://github.com/rmems/recoverly-sim) (on hold).

---

## How I work

I normally go from **issue → pull request**, either from a **local CLI** or through **Linear** (cloud).

- **Agents** I use day to day: Grok Build, Codex, Claude, Meta Muse, Cursor, Devin, Kilo, OpenCode and others — plus shared memory (Ogham / Chroma). Humans merge.  
- **PR review** (rough order): Codex → CodeRabbit → Devin when I want a strong extra pass → Cursor Bugbot · Copilot · CodeAnt · Qodana (local + cloud).  To keep engaging in the act of learning programming I will perdically review PR's with my Rust textbook checking to see if the bots have correctly identify any real bugs or errors.
  - **Before I open or push a PR**, I like to run local checks from each repo’s **`REVIEW.md`** and **Qodana CLI** so issues surface on my machine first.
  - **CI:** GitHub Actions on **pull requests and pushes** to main repos.  Instead of me having to manually review every PR with CLI commands, I rely on CI to catch issues early.  In way indirectly acts like a benchmark for me to see how well my agents can implement codes, including myself as I can't always trust that my code will work. 

---

## Currently

- **Agent sandboxes:** [worktrees-hives](https://github.com/rmems/worktrees-hives) — multi-agent hypothesis lab in isolated git worktrees (no auto-merge)
- **Agentic engineering datasets:** [operation-prometheus](https://github.com/rmems/operation-prometheus) — issue→review→patch→validation history for local agents
- **Local agentic GPU:** [blackwell-kernel-lab](https://github.com/rmems/blackwell-kernel-lab) — Blackwell / RTX 5080 path toward personal agentic GPU infrastructure
- **SAAQ lab + pipeline:** [magere-brug](https://github.com/rmems/magere-brug) + [corinth-canal](https://github.com/rmems/corinth-canal) (**Spiking Adaptive Activity Quantization**)
- **MoE → Spikenaut:** [hybrid-fusion](https://github.com/rmems/hybrid-fusion) + [engram-parser](https://github.com/rmems/engram-parser) → [Spikenaut-SNN](https://github.com/rmems/Spikenaut-SNN) (own SNN from scratch; expert-block transfer)
- **Grok-scale experiments:** [xai-dissect](https://github.com/rmems/xai-dissect) / [grok-ozempic](https://github.com/rmems/grok-ozempic) (+ [XAIDissect_Viz.jl](https://github.com/rmems/XAIDissect_Viz.jl))
- **Neuromorphic core (limen-return stack):** [LiquidCortex.jl](https://github.com/rmems/LiquidCortex.jl) · [SpikeStream.jl](https://github.com/rmems/SpikeStream.jl) · [NeuroPulse.jl](https://github.com/rmems/NeuroPulse.jl) · [TemporalFocus.jl](https://github.com/rmems/TemporalFocus.jl) · [SynapticDistill.jl](https://github.com/rmems/SynapticDistill.jl) — compose toward one runtime story
- **Telemetry → SNN data path:** [gaming-telemetry](https://github.com/rmems/gaming-telemetry) · [Theseus-Quarry](https://github.com/rmems/Theseus-Quarry) · [spikenaut-telemetry-etl](https://github.com/rmems/spikenaut-telemetry-etl) · [Surrogate_Viz.jl](https://github.com/rmems/Surrogate_Viz.jl)
- **Hardware path:** [silicon-hdl](https://github.com/rmems/silicon-hdl) · [silicon-bridge](https://github.com/rmems/silicon-bridge) · [thalamic-relay](https://github.com/rmems/thalamic-relay) (FPGA + orchestration; still early on the HDL curve)
- **Cloud training scaffold:** [Dioscuri-Cloud](https://github.com/rmems/Dioscuri-Cloud)
- **Libraries:** [neuromod](https://github.com/Limen-Neural/neuromod) **v0.5.1 on crates.io**; remaining Limen-Neural crates still in progress toward publish
- **Education:** Pursuing AI Engineering @ WGU

---

<sub>README updated by me (rmems) and with Grok Build: Grok 4.5 (high)</sub>
