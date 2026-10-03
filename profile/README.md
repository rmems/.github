# Raul Montoya Cardenas

**Early-Career AI Engineer | Experimental AI Systems, Model Evaluation & ML Infrastructure**

B.S. AI Engineering student, Western Governors University — Expected September 2027

San Marcos, Texas · montoyaraul34@gmail.com

[GitHub Projects](https://github.com/rmems?tab=projects) · [Hugging Face](https://huggingface.co/rmems) · [Limen Neural](https://github.com/Limen-Neural)

I build experimental AI systems in Python, Rust, Julia, and CUDA: synthetic supervision and evaluation pipelines, neuromorphic systems, and hybrid model tools. My repositories are focused components designed for independent testing and reuse, with explicit interfaces for composing larger experiments.

---

## Flagship research programs

These are three research directions, each spanning several repositories. Component maturity is labeled separately in the system map; experimental outcomes are not claimed in advance.

<a name="synthetic-supervision"></a>

### Synthetic supervision / training pipeline

**Start here: [synthetic-factory](https://github.com/rmems/synthetic-factory).**

| Question | My work and distinction | Evidence to inspect |
|---|---|---|
| How can synthetic supervision and real engineering trajectories support reproducible post-training experiments? | I develop generation and curation tooling, trajectory extraction, and training/evaluation contracts, separating data production, eligibility, and held-out comparisons through versioned artifacts. | Generators, schemas, extracted trajectory examples, validation tools, and evaluation implementations. Controlled comparisons remain planned; no training improvement is claimed. |

Program overview:

```text
Synthetic Factory → Operation Prometheus → Agoge Forger
```

Synthetic Factory supplies the synthetic-supervision work; [Operation Prometheus](https://github.com/rmems/operation-prometheus) extracts real engineering trajectories; [Agoge Forger](https://github.com/rmems/agoge-forger) owns post-training and evaluation. The diagram groups the program: synthetic and real trajectories are distinct inputs to Agoge, and the arrows do not establish a working serial integration.

Deeper: [generator lanes and rights](https://github.com/rmems/synthetic-factory#generator-lanes-and-rights) · [trajectory collection and eligibility](https://github.com/rmems/operation-prometheus/tree/main/docs) · [frozen split and evaluation contracts](https://github.com/rmems/agoge-forger/blob/main/docs/frozen_split_and_eval_contracts.md).

<a name="spikenaut"></a>

### Spikenaut / neuromorphic systems

**Start here: [Spikenaut-SNN](https://github.com/rmems/Spikenaut-SNN).**

| Question | My work and distinction | Evidence to inspect |
|---|---|---|
| Can a small SNN represent machine state over time and support bounded supervisory behavior? | I investigate telemetry-to-SNN representations, model/export artifacts, and composition of encoding, neuron, and hardware-interface components. Learned systems propose actions; deterministic software retains safety control. | Model artifacts, Q8.8 export contracts, replay tools, and telemetry. This remains experimental: validated supervisory behavior and software–FPGA parity are unproven. |

[SynapticDistill.jl](https://github.com/rmems/SynapticDistill.jl) houses the separate Spikenaut trainer. Limen Neural libraries provide reusable encoding, neuron, graph, and wiring components; [silicon-bridge](https://github.com/rmems/silicon-bridge) provides checked parameter export. Each integration has a defined scope; these components do not establish a validated deployment chain.

Deeper: [research question and system model](https://github.com/rmems/Spikenaut-SNN#the-research-question).

<a name="hybrid-quantization"></a>

### ANN–SNN hybrid / quantization research

**Start here: [corinth-canal](https://github.com/rmems/corinth-canal).**

| Question | My work and distinction | Evidence to inspect |
|---|---|---|
| How can spiking representations, ANN/MoE routing, and quantization be combined while assessing fidelity and computational tradeoffs? | I develop the reference experiment loop, reusable orchestration contracts, checkpoint inspection, and quantization tooling, separating integrated research from reusable component interfaces. | Reference implementations, validation runners, manifests, telemetry outputs, and experiment documentation. Implemented tooling does not establish a successful research outcome. |

Corinth is the integrated research reference. [hybrid-fusion](https://github.com/rmems/hybrid-fusion) defines backend-independent orchestration contracts; [xai-dissect](https://github.com/rmems/xai-dissect) supplies checkpoint manifests for [grok-ozempic](https://github.com/rmems/grok-ozempic) quantization experiments.

Deeper: [architecture](https://github.com/rmems/corinth-canal/blob/main/docs/ARCHITECTURE.md) · [run profiles and artifacts](https://github.com/rmems/corinth-canal/blob/main/docs/RUN_PROFILES.md).

---

## System map

**Flagship** — polished repository intended for external inspection; **Active** — maintained component with documented functionality, without implying production readiness; **Experimental** — research prototype or experimental implementation; **Archived** — explicitly retired or superseded artifact.

Program links group research responsibilities. Libraries can also be reused independently; membership does not imply a runtime dependency.

### Data, supervision, and evaluation

| Repository | Responsibility | Status | Program |
|---|---|---|---|
| [synthetic-factory](https://github.com/rmems/synthetic-factory) | Generate, curate, and validate synthetic data with provenance and eligibility gates | Active | [Synthetic supervision](#synthetic-supervision) |
| [operation-prometheus](https://github.com/rmems/operation-prometheus) | Extract and normalize real engineering trajectories | Active | [Synthetic supervision](#synthetic-supervision) |
| [agoge-forger](https://github.com/rmems/agoge-forger) | Post-training, evaluation, checkpoint, and reproducibility tooling | Active | [Synthetic supervision](#synthetic-supervision) |

### Neuromorphic models and reusable components

| Repository | Responsibility | Status | Program |
|---|---|---|---|
| [nir-rs](https://github.com/Limen-Neural/nir-rs) | Typed neuromorphic graphs and optional NIR file interchange | Active | [Spikenaut / SNN](#spikenaut) |

**Experimental components**

| Repository | Responsibility | Status | Program |
|---|---|---|---|
| [Spikenaut-SNN](https://github.com/rmems/Spikenaut-SNN) | Telemetry-driven model artifacts, replay, and export contracts | Experimental | [Spikenaut / SNN](#spikenaut) |
| [SynapticDistill.jl](https://github.com/rmems/SynapticDistill.jl) | Spikenaut sidecar trainer; generic e-prop/OTTT rules remain stubs | Experimental | [Spikenaut / SNN](#spikenaut) |
| [neuromod](https://github.com/Limen-Neural/neuromod) | Reusable neuron dynamics and spiking-network primitives | Experimental | [Spikenaut / SNN](#spikenaut) |
| [axon-encoder](https://github.com/Limen-Neural/axon-encoder) | Convert continuous signals into spikes | Experimental | [Spikenaut / SNN](#spikenaut) |
| [synaptic-wiring](https://github.com/Limen-Neural/synaptic-wiring) | Network topology, connectivity, and temporal delays | Experimental | [Spikenaut / SNN](#spikenaut) |

### Hybrid orchestration and quantization

| Repository | Responsibility | Status | Program |
|---|---|---|---|
| [xai-dissect](https://github.com/rmems/xai-dissect) | Inspect Grok-1 checkpoints and export structural manifests | Active | [Hybrid / quantization](#hybrid-quantization) |

**Experimental components**

| Repository | Responsibility | Status | Program |
|---|---|---|---|
| [corinth-canal](https://github.com/rmems/corinth-canal) | Reference telemetry-to-spiking-to-MoE loop and SAAQ validation | Experimental | [Hybrid / quantization](#hybrid-quantization) |
| [hybrid-fusion](https://github.com/rmems/hybrid-fusion) | Backend-independent ANN–SNN orchestration contracts | Experimental | [Hybrid / quantization](#hybrid-quantization) |
| [grok-ozempic](https://github.com/rmems/grok-ozempic) | Streaming Grok-1 quantization and fidelity experiments | Experimental | [Hybrid / quantization](#hybrid-quantization) |

### Hardware interfaces and acceleration

**Experimental components**

| Repository | Responsibility | Status | Program |
|---|---|---|---|
| [silicon-bridge](https://github.com/rmems/silicon-bridge) | Checked Q8.8 parameter export and host UART codecs | Experimental | [Spikenaut / SNN](#spikenaut) |
| [myelin-accelerator](https://github.com/Limen-Neural/myelin-accelerator) | Reusable Rust/CUDA primitives for SNN, routing, and packed ternary operations | Experimental | Hardware acceleration |

Explore all repositories and projects: [rmems](https://github.com/rmems?tab=repositories) · [Limen Neural](https://github.com/orgs/Limen-Neural/repositories) · [GitHub Projects](https://github.com/rmems?tab=projects).

---

## From monolith to modular systems

This ecosystem originated in a larger neuromorphic / AI research workspace. As interfaces and research directions matured, I progressively decomposed it into focused, interoperable repositories. Clearer boundaries support independent testing and releases, reuse, replaceable components, and experimentation, while making it easier to return to work after time away and compose larger research systems.

---

## Selected Hugging Face artifacts

[Full Hugging Face portfolio](https://huggingface.co/rmems)

- **[Spikenaut-SNN-Telemetry](https://huggingface.co/datasets/rmems/Spikenaut-SNN-Telemetry)** — telemetry for neuromorphic representation and replay experiments.
- **[Agentic Coding Trajectories](https://huggingface.co/datasets/rmems/agentic-coding-trajectories)** — historical synthetic coding episodes, distinct from Prometheus's real engineering trajectories. Raw, not training-ready, and blocked from model-weight updates under current project policy.

A published dataset or artifact does not establish training readiness or research success. Hosted frontier-model outputs remain research-only; training inputs require independent provenance, license, and project-policy eligibility.

---

## Selected upstream contributions

- **UsagePal:** Linux support and telemetry for [Antigravity (#56)](https://github.com/Halloweedev/usagepal/pull/56) and [Devin (#48)](https://github.com/Halloweedev/usagepal/pull/48).
- **agent-afk:** [xAI/Grok provider support (#1019)](https://github.com/griffinwork40/agent-afk/pull/1019) and [OAuth CLI compatibility (#1242)](https://github.com/griffinwork40/agent-afk/pull/1242).

---

## Attribution

Primary author and maintainer: **Raul Montoya Cardenas (rmems)**.

Profile structure and edits were developed with OpenAI ChatGPT / Codex. Project-specific AI contributions remain attributed in commits, pull requests, experiment records, and release provenance; see [Agoge contributor guidance](https://github.com/rmems/agoge-forger/blob/main/AGENTS.md) for repository boundaries and validation practices.
