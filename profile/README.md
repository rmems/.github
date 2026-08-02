# Raul Montoya Cardenas

San Marcos, Texas · montoyaraul34@gmail.com

---

> *Making large models run on hardware you can actually own.*

My core research is **SAAQ** (Spiking Adaptive Activity Quantization) — treating quantization as an instrument to discover sparse MoE routing and adaptation laws under real hardware pressure, then transferring them toward a native SNN (**Spikenaut**) under the **SEMM** (Spiking Experts Mixture Mechanism) program. I also work on Grok-scale checkpoint analysis, neuromorphic telemetry, quantization benchmarks, and multi-agent engineering tooling under [rmems](https://github.com/rmems).

Related modular SNN libraries live under [Limen Neural](https://github.com/Limen-Neural).

---

## 🧠 Active Projects

| Project | Description | Stack |
|---|---|---|
| [**magere-brug**](https://github.com/rmems/magere-brug) | **SAAQ lab** — artifact registry, recipes, manifests, and CPU validation for Spiking Adaptive Activity Quantization | Rust |
| [**corinth-canal**](https://github.com/rmems/corinth-canal) | SAAQ reference loop: telemetry → spiking layer → projector/router → latent calibration | Rust · CUDA |
| [**xai-dissect**](https://github.com/rmems/xai-dissect) | Static structural analysis of Grok-family open-weight MoE checkpoints | Rust |
| [**grok-ozempic**](https://github.com/rmems/grok-ozempic) | Ternary SNN-inspired quantization for Grok-scale MoE routing fidelity | Rust |
| [**Surrogate_Viz.jl**](https://github.com/rmems/Surrogate_Viz.jl) | Symbolic regression + validation dashboards for SAAQ telemetry | Julia |
| [**XAIDissect_Viz.jl**](https://github.com/rmems/XAIDissect_Viz.jl) | Interactive Grok-1 MoE atmosphere from xai-dissect reports | Julia · Makie |
| [**spike-viz**](https://github.com/rmems/spike-viz) | Visualize SNN encodings and activity (paint layer for spike exports) | Python · PyTorch |
| [**gaming-telemetry**](https://github.com/rmems/gaming-telemetry) | High-frequency GPU/CPU telemetry → Parquet for SNN training | Rust · NVML |
| [**Theseus-Quarry**](https://github.com/rmems/Theseus-Quarry) | Mining ops telemetry (hashrate/power/temp) for neuromorphic datasets | Rust |
| [**Limen-Capital**](https://github.com/rmems/Limen-Capital) | Experimental SNN-HFT stack (Julia neuromorphic + Rust execution) — not live capital | Julia · Rust |
| [**agoge-forger**](https://github.com/rmems/agoge-forger) | Local-first GPU training forge (QLoRA/LoRA, RTX 5080-aware) | Python · PyTorch |
| [**combine-for-AI**](https://github.com/rmems/combine-for-AI) | Neutral benchmark harness for model quantization experiments | Python |
| [**operation-prometheus**](https://github.com/rmems/operation-prometheus) | Engineering trajectories (issue→review→merge) as agent training data | Python |
| [**worktree-hive**](https://github.com/rmems/worktree-hive) | Multi-agent issue→PR orchestration with isolated worktrees | Rust · Python |

Also: [`Spikenaut-SNN`](https://github.com/rmems/Spikenaut-SNN) · [`NeuralForge-Memory`](https://github.com/rmems/NeuralForge-Memory) · [`Dioscuri-Cloud`](https://github.com/rmems/Dioscuri-Cloud) · [`blackwell-kernel-lab`](https://github.com/rmems/blackwell-kernel-lab)

---

## 🤖 Multi-Agent Engineering

I ship research with a multi-agent stack across **Grok Build**, **Codex**, **Claude** (incl. Claude Code), **Cursor**, **Devin**, **Kilo**, **OpenCode**, **Cline**, and related agent CLIs (e.g. Mimo, Jules). Agents share durable context via **Ogham** and **Chroma**, babysit PRs (CI + review threads), and work in isolated worktrees. Humans merge — agents prepare, never auto-merge.

Tooling: [`worktree-hive`](https://github.com/rmems/worktree-hive).

### PR review

PRs use a deliberate review stack:

1. **Codex** — primary deep review (main heavy hitter)  
2. **CodeRabbit** — second-pass AI review  
3. **Devin** — extra high-quality review when I want a strong second opinion  
4. **Cursor Bugbot** — PR automation  
5. **GitHub Copilot** code review (GitHub Pro)  
6. **CodeAnt AI** — free reviewer on all repos  
7. **Qodana** — static analysis locally and in the cloud  

Agents babysit CI and reply to review threads; humans merge.

---

## ✅ CI & quality

Research repos run on **GitHub Actions** with layered gates — build/test first, then coverage, static analysis, security, and optional release observability.

- **Build/test** — Rust (`fmt` · `clippy -D warnings` · `cargo test --locked`) · Julia · Python smokes  
- **Coverage** — Codecov (`cargo-llvm-cov` where wired)  
- **Static analysis** — **Qodana** (local + cloud)  
- **Security** — Aikido · Snyk · `cargo audit` · CodeQL on flagships  
- **Observability** — optional Sentry release markers on `main`  
- **Hardware** — CUDA/Docker (e.g. 13.2) and self-hosted Ryzen runners where the work needs them ([`corinth-canal`](https://github.com/rmems/corinth-canal))

| Flagship | Focus |
|---|---|
| [**corinth-canal**](https://github.com/rmems/corinth-canal/actions) | Dual-runner CPU CI · CUDA/GPU · security · coverage |
| [**magere-brug**](https://github.com/rmems/magere-brug/actions) | SAAQ lab: CI · docs · manifest validate · Docker |
| [**xai-dissect**](https://github.com/rmems/xai-dissect/actions) | Hardened Rust gate · Codecov · Qodana · Sentry |
| [**grok-ozempic**](https://github.com/rmems/grok-ozempic/actions) | Rust + Python + Docker + audit + Aikido + Qodana |
| [**worktree-hive**](https://github.com/rmems/worktree-hive/actions) | Split Rust/Python · Security · Qodana · Release |

[![corinth-canal CI](https://github.com/rmems/corinth-canal/actions/workflows/ci.yml/badge.svg)](https://github.com/rmems/corinth-canal/actions/workflows/ci.yml)
[![magere-brug CI](https://github.com/rmems/magere-brug/actions/workflows/ci.yml/badge.svg)](https://github.com/rmems/magere-brug/actions/workflows/ci.yml)
[![xai-dissect CI](https://github.com/rmems/xai-dissect/actions/workflows/ci.yml/badge.svg)](https://github.com/rmems/xai-dissect/actions/workflows/ci.yml)
[![grok-ozempic Rust](https://github.com/rmems/grok-ozempic/actions/workflows/rust.yml/badge.svg)](https://github.com/rmems/grok-ozempic/actions/workflows/rust.yml)
[![worktree-hive Rust](https://github.com/rmems/worktree-hive/actions/workflows/rust.yml/badge.svg)](https://github.com/rmems/worktree-hive/actions/workflows/rust.yml)

---

## 🔬 Research Focus

- **SAAQ / SEMM** — Spiking Adaptive Activity Quantization lab (`magere-brug`) + reference loop (`corinth-canal`); dual-rule Δq laws; path toward **Spikenaut**
- **Grok-scale MoE** — Structural dissect (`xai-dissect`), SNN-inspired quant (`grok-ozempic`), routing viz (`XAIDissect_Viz.jl`)
- **Neuromorphic telemetry** — Gaming/GPU (`gaming-telemetry`) and mining ops (`Theseus-Quarry`) as SNN training signals
- **Symbolic regression** — Compact equation discovery from latent/telemetry streams (`Surrogate_Viz.jl`)
- **Agent trajectories** — High-signal issue→PR history as datasets (`operation-prometheus`)
- **Experimental SNN-HFT** — Research stack only; not live capital (`Limen-Capital`)

---

## 🛠️ Tech Stack

Actively learning and building with:

```
Languages:   Julia · Rust · Python · CUDA/C++ · HCL
Frameworks:  PyTorch · CUDA.jl · SymbolicRegression.jl · ort (ONNX)
Infra:       Terraform · Multi-cloud · NVIDIA Blackwell (RTX 5080)
CI:          GitHub Actions · Codecov · Qodana · Aikido/Snyk · cargo-audit · Sentry
Review:      Codex · CodeRabbit · Devin · Cursor Bugbot · Copilot · CodeAnt · Qodana
Agents:      Grok Build · Codex · Claude · Cursor · Devin · Kilo · OpenCode · Cline
Memory:      Ogham · Chroma
```

---

## 📍 Currently

- 🧪 Running the **SAAQ lab** in [`magere-brug`](https://github.com/rmems/magere-brug) with the reference loop in [`corinth-canal`](https://github.com/rmems/corinth-canal)
- 🔥 Grok-scale work: [`xai-dissect`](https://github.com/rmems/xai-dissect) + [`grok-ozempic`](https://github.com/rmems/grok-ozempic) + spike/routing viz
- 📡 Telemetry feeds: [`Theseus-Quarry`](https://github.com/rmems/Theseus-Quarry) + [`gaming-telemetry`](https://github.com/rmems/gaming-telemetry)
- 💹 Experimental SNN-HFT research app: [`Limen-Capital`](https://github.com/rmems/Limen-Capital) (not live capital)
- 🤖 Multi-agent PR/worktree workflows via [`worktree-hive`](https://github.com/rmems/worktree-hive) + trajectory forge [`operation-prometheus`](https://github.com/rmems/operation-prometheus)
- 🎓 B.S. in AI Engineering @ WGU — deepening Julia, Rust, Python, CUDA, and HCL in real repos

---

<sub>README updated with Grok Build: Grok 4.5 (high)</sub>

<!--
**rmems/.github** is a ✨ _special_ ✨ repository because its `profile/README.md` (this file) appears on your GitHub profile.
-->
