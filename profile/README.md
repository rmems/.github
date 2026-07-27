# Raul Montoya Cardenas

San Marcos, Texas · montoyaraul34@gmail.com

---

> *Making large models run on hardware you can actually own.*

My core research is **SAAQ** (Spiking Adaptive Activity Quantization) — compressing large-scale models so they run on consumer GPUs by turning them into spiking neural network representations. I also work on model interpretability, quantization benchmarking, and a modular neuromorphic stack under [Limen Neural](https://github.com/Limen-Neural).

---

## 🧠 Active Projects

| Project | Description | Stack |
|---|---|---|
| [**corinth-canal**](https://github.com/rmems/corinth-canal) | SAAQ reference loop: telemetry → spiking layer → projector/router → latent calibration | Rust · CUDA |
| [**xai-dissect**](https://github.com/rmems/xai-dissect) | Static structural analysis of Grok-family open-weight MoE checkpoints | Rust |
| [**grok-ozempic**](https://github.com/rmems/grok-ozempic) | Ternary SNN-inspired quantization for Grok-scale MoE routing fidelity | Rust |
| [**magere-brug**](https://github.com/rmems/magere-brug) | SAAQ experiment lab: manifests, recipes, artifact registry | Rust |
| [**Surrogate_Viz.jl**](https://github.com/rmems/Surrogate_Viz.jl) | Symbolic regression + validation dashboards for SAAQ telemetry | Julia |
| [**XAIDissect_Viz.jl**](https://github.com/rmems/XAIDissect_Viz.jl) | Interactive Grok-1 MoE atmosphere from xai-dissect reports | Julia · Makie |
| [**myelin-accelerator**](https://github.com/Limen-Neural/myelin-accelerator) | Blackwell-first CUDA kernels for neuromorphic inference | Rust · CUDA |
| [**agoge-forger**](https://github.com/rmems/agoge-forger) | Local-first GPU training forge (QLoRA/LoRA, RTX 5080-aware) | Python · PyTorch |
| [**combine-for-AI**](https://github.com/rmems/combine-for-AI) | Neutral benchmark harness for model quantization experiments | Python |
| [**Dioscuri-Cloud**](https://github.com/rmems/Dioscuri-Cloud) | Cloud ML lab: smoke tests, cost ledger, multi-provider runbooks | Terraform · Ops |
| [**gaming-telemetry**](https://github.com/rmems/gaming-telemetry) | High-frequency GPU/CPU telemetry → Parquet for SNN training | Rust · NVML |
| [**spike-viz**](https://github.com/rmems/spike-viz) | Visualize SNN encodings from axon-encoder exports | Python · PyTorch |
| [**NeuralForge-Memory**](https://github.com/rmems/NeuralForge-Memory) | Personal RAG + vector DB + MCP memory (Hermes tutor) | Rust · MCP |

---

## 🧬 Limen Neural

[**Limen Neural**](https://github.com/Limen-Neural) is my neuromorphic library org — hard repo boundaries, modular crates you can reuse, dual MIT/Apache-2.0 where applicable.

- **Rust infra:** [`neuromod`](https://github.com/Limen-Neural/neuromod) · [`axon-encoder`](https://github.com/Limen-Neural/axon-encoder) · [`cortex-tensor`](https://github.com/Limen-Neural/cortex-tensor) · [`nir-rs`](https://github.com/Limen-Neural/nir-rs) · [`myelin-accelerator`](https://github.com/Limen-Neural/myelin-accelerator)
- **Julia research:** [`TemporalFocus.jl`](https://github.com/Limen-Neural/TemporalFocus.jl) · [`LiquidCortex.jl`](https://github.com/Limen-Neural/LiquidCortex.jl) · [`NeuroPulse.jl`](https://github.com/Limen-Neural/NeuroPulse.jl)
- **Hardware path:** [`silicon-hdl`](https://github.com/Limen-Neural/silicon-hdl) · [`silicon-bridge`](https://github.com/Limen-Neural/silicon-bridge) (Q8.8 → FPGA)

---

## 🤖 Multi-Agent Engineering

I ship research with a multi-agent engineering stack across **Grok Build**, **Codex**, **Claude** (incl. Claude Code), **Cursor**, **Devin**, **Kilo**, **OpenCode**, **Cline**, and related agent CLIs (e.g. Mimo, Jules). Agents share durable context via **Ogham** and **Chroma**, babysit PRs (CI + review threads), and work in isolated worktrees so parallel edits stay safe. Humans merge — agents prepare, never auto-merge.

Tooling: [`worktree-hive`](https://github.com/rmems/worktree-hive) for issue → PR orchestration with isolated subagents.

---

## 🔬 Research Focus

- **SAAQ** — Spiking Adaptive Activity Quantization: frontier MoE models on consumer GPUs
- **SNN compression** — Low-bit, activity-aware quantization of large transformer MoE architectures
- **Symbolic regression** — Compact equation discovery from high-dimensional GPU/neuromorphic telemetry
- **Explainable MoE** — Dissect and visualize expert routing in open-weight models (no weight redistribution)

---

## 🛠️ Tech Stack

Actively learning and building with:

```
Languages:   Julia · Rust · Python · CUDA/C++ · HCL
Frameworks:  PyTorch · CUDA.jl · SymbolicRegression.jl · ort (ONNX)
Infra:       Terraform · Multi-cloud · NVIDIA Blackwell (RTX 5080)
Agents:      Grok Build · Codex · Claude · Cursor · Devin · Kilo · OpenCode · Cline
Memory:      Ogham · Chroma
```

---

## 📍 Currently

- 🔥 SAAQ reference path via [`corinth-canal`](https://github.com/rmems/corinth-canal) + Grok-scale quantization / dissect viz
- 🧬 Growing the Limen Neural stack: encode → dynamics → NIR → FPGA
- 🤖 Multi-agent PR and worktree workflows across the agent fleet above
- ⚡ Local Blackwell / RTX 5080 kernels and training loops
- 🎓 B.S. in AI Engineering @ WGU — deepening Julia, Rust, Python, CUDA, and HCL in real repos

---

<sub>README updated with Grok Build: Grok 4.5</sub>

<!--
**rmems/.github** is a ✨ _special_ ✨ repository because its `profile/README.md` (this file) appears on your GitHub profile.
-->
