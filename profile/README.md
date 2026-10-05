# Raul Montoya Cardenas

**Early-Career AI Engineer | AI Systems, Model Evaluation & ML Infrastructure**

B.S. AI Engineering student, Western Governors University — Expected September 2027

San Marcos, Texas · montoyaraul34@gmail.com

[GitHub Projects](https://github.com/rmems?tab=projects) · [Hugging Face](https://huggingface.co/rmems) · [Limen Neural](https://github.com/Limen-Neural)

I build open-source tools for reproducible training experiments, spiking neural networks, and ANN–SNN hybrid research. I focus on modular work that others can inspect, test, and reuse. Ten of my Rust libraries are published on [crates.io](https://crates.io/users/rmems), and I publish trajectory and evaluation datasets on [Hugging Face](https://huggingface.co/rmems) (60 datasets).

**Technical focus:** Python, Rust, Julia, CUDA · data provenance and validation · post-training and evaluation · neuromorphic models and interfaces.

## Start here

- [**Rust libraries on crates.io**](https://crates.io/users/rmems) — 10 published crates (neuromod, nir-rs, axon-encoder, kinetic-signals, silicon-bridge, myelin-accelerator, …): versioned, documented, and tested.
- [**Synthetic Factory](https://github.com/rmems/synthetic-factory)&#32;/&#32;[Agoge Forger](https://github.com/rmems/agoge-forger)** — inspect data generators and eligibility checks, run the documented smoke checks, and explore frozen training/evaluation contracts.
- [**Spikenaut-SNN**](https://github.com/rmems/Spikenaut-SNN) — inspect telemetry-driven model artifacts, replay tools, and Q8.8 export contracts, including the documented limits of the experiments.
- [**Limen Neural**](https://github.com/Limen-Neural) — explore reusable Rust components for signal encoding, neuron dynamics, and neuromorphic graphs; follow each repository's examples and tests.

## Selected upstream contributions

- **UsagePal:** merged Linux support and telemetry work for [Antigravity (#56)](https://github.com/Halloweedev/usagepal/pull/56) and [Devin (#48)](https://github.com/Halloweedev/usagepal/pull/48).
- **agent-afk:** merged [xAI/Grok provider support (#1019)](https://github.com/griffinwork40/agent-afk/pull/1019) and [OAuth CLI compatibility (#1242)](https://github.com/griffinwork40/agent-afk/pull/1242).

## Current priorities

- Reduce technical debt across [writ](https://github.com/rmems/writ), [synthetic-factory](https://github.com/rmems/synthetic-factory), [operation-prometheus](https://github.com/rmems/operation-prometheus), and [agoge-forger](https://github.com/rmems/agoge-forger): improve reliability, tests, documentation, and reproducibility while simplifying unnecessary complexity. This work is ongoing.
- Keep writ collaboration-first: remove redundant enforcement while preserving safeguards for existing work and other contributors' changes.
- Prepare controlled training/evaluation comparisons with independently eligible data, frozen contracts, and reproducible artifacts. Research outcomes remain unproven.

---

## Flagship research programs

These are three research directions, each spanning several repositories. Component maturity is labeled separately in the component map; research outcomes are not claimed in advance.

<a name="synthetic-supervision"></a>

### Synthetic supervision / training pipeline

| Question | My work and distinction | Evidence to inspect |
| --- | --- | --- |
| How can synthetic supervision and real engineering trajectories support reproducible post-training experiments? | I develop generation and curation tooling, trajectory extraction, and training/evaluation contracts, separating data production, eligibility, and held-out comparisons through versioned artifacts. | Generators, schemas, extracted trajectory examples, validation tools, and evaluation implementations. Controlled comparisons remain planned; no training improvement is claimed. |

Planned data flow (separate potential inputs):

```text
Synthetic Factory: synthetic examples ───────────┐
                                                ├─→ Provenance, license, and
Operation Prometheus: real engineering ──────────┘   project-policy eligibility gates
                      trajectories                            │
                                                              ▼
                                                    Agoge Forger
                                                    training / evaluation
```

Synthetic Factory's generation and validation tools, [Operation Prometheus](https://github.com/rmems/operation-prometheus)'s trajectory collection tools, and [Agoge Forger](https://github.com/rmems/agoge-forger)'s training/evaluation contracts are implemented in their respective repositories. The converging arrows describe the intended experiment design, not a completed end-to-end integration. Each input must independently pass provenance, license, and project-policy gates before training; hosted frontier-model outputs remain research-only and excluded from model-weight updates.

Deeper: [generator lanes and rights](https://github.com/rmems/synthetic-factory#generator-lanes-and-rights) · [trajectory collection and eligibility](https://github.com/rmems/operation-prometheus/tree/main/docs) · [frozen split and evaluation contracts](https://github.com/rmems/agoge-forger/blob/main/docs/frozen_split_and_eval_contracts.md).

<a name="spikenaut"></a>

### Spikenaut / neuromorphic systems

| Question | My work and distinction | Evidence to inspect |
| --- | --- | --- |
| Can a small SNN represent machine state over time and support bounded supervisory behavior? | I investigate telemetry-to-SNN representations, model/export artifacts, and composition of encoding, neuron, and hardware-interface components. Learned systems propose actions; deterministic software retains safety control. | Model artifacts, Q8.8 export contracts, replay tools, and telemetry. This remains experimental: validated supervisory behavior and software–FPGA parity are unproven. |

[SynapticDistill.jl](https://github.com/rmems/SynapticDistill.jl) houses the separate Spikenaut trainer. Limen Neural libraries provide reusable encoding, neuron, graph, and wiring components; [silicon-bridge](https://github.com/rmems/silicon-bridge) provides checked parameter export. Each integration has a defined scope; these components do not establish a validated deployment chain.

Deeper: [research question and system model](https://github.com/rmems/Spikenaut-SNN#the-research-question).

<a name="hybrid-quantization"></a>

### ANN–SNN hybrid / quantization research

**Research reference:&#32;[corinth-canal](https://github.com/rmems/corinth-canal).**

| Question | My work and distinction | Evidence to inspect |
| --- | --- | --- |
| How can spiking representations, ANN/MoE routing, and quantization be combined while assessing fidelity and computational tradeoffs? | I develop the reference experiment loop, reusable orchestration contracts, checkpoint inspection, and quantization tooling, separating integrated research from reusable component interfaces. | Reference implementations, validation runners, manifests, telemetry outputs, and experiment documentation. Implemented tooling does not establish a successful research outcome. |

Corinth is the integrated research reference. [hybrid-fusion](https://github.com/rmems/hybrid-fusion) defines backend-independent orchestration contracts; [xai-dissect](https://github.com/rmems/xai-dissect) supplies checkpoint manifests for [grok-ozempic](https://github.com/rmems/grok-ozempic) quantization experiments.

Deeper: [architecture](https://github.com/rmems/corinth-canal/blob/main/docs/ARCHITECTURE.md) · [run profiles and artifacts](https://github.com/rmems/corinth-canal/blob/main/docs/RUN_PROFILES.md).

---

## Component map

<details>
<summary>Repositories, responsibilities, and maturity</summary>

**Published** — on crates.io: versioned, documented, tested. **Active** — maintained with documented functionality, without implying production readiness. **Research** — exploratory research direction: the code is real and maintained (often Published too), but the research outcomes are unproven and no validated result is claimed. **Archived** — explicitly retired or superseded artifact.

Program links group research responsibilities. Libraries can also be reused independently; membership does not imply a runtime dependency.

### Data, supervision, and evaluation

| Repository | Responsibility | Status | Program |
| --- | --- | --- | --- |
| [synthetic-factory](https://github.com/rmems/synthetic-factory) | Generate, curate, and validate synthetic data with provenance and eligibility gates | Active | [Synthetic supervision](#synthetic-supervision) |
| [operation-prometheus](https://github.com/rmems/operation-prometheus) | Extract and normalize real engineering trajectories | Active | [Synthetic supervision](#synthetic-supervision) |
| [agoge-forger](https://github.com/rmems/agoge-forger) | Post-training, evaluation, checkpoint, and reproducibility tooling | Active | [Synthetic supervision](#synthetic-supervision) |

### Neuromorphic models and reusable components

| Repository | Responsibility | Status | Program |
| --- | --- | --- | --- |
| [nir-rs](https://github.com/Limen-Neural/nir-rs) | Typed neuromorphic graphs and optional NIR file interchange | Published | [Spikenaut / SNN](#spikenaut) |

**Research components**

| Repository | Responsibility | Status | Program |
| --- | --- | --- | --- |
| [Spikenaut-SNN](https://github.com/rmems/Spikenaut-SNN) | Telemetry-driven model artifacts, replay, and export contracts | Research | [Spikenaut / SNN](#spikenaut) |
| [SynapticDistill.jl](https://github.com/rmems/SynapticDistill.jl) | Spikenaut sidecar trainer; generic e-prop/OTTT rules remain stubs | Research | [Spikenaut / SNN](#spikenaut) |
| [neuromod](https://github.com/Limen-Neural/neuromod) | Reusable neuron dynamics and spiking-network primitives | Published · Research | [Spikenaut / SNN](#spikenaut) |
| [axon-encoder](https://github.com/Limen-Neural/axon-encoder) | Convert continuous signals into spikes | Published · Research | [Spikenaut / SNN](#spikenaut) |
| [synaptic-wiring](https://github.com/Limen-Neural/synaptic-wiring) | Network topology, connectivity, and temporal delays | Published · Research | [Spikenaut / SNN](#spikenaut) |

### Hybrid orchestration and quantization

| Repository | Responsibility | Status | Program |
| --- | --- | --- | --- |
| [xai-dissect](https://github.com/rmems/xai-dissect) | Inspect Grok-1 checkpoints and export structural manifests | Active | [Hybrid / quantization](#hybrid-quantization) |

**Research components**

| Repository | Responsibility | Status | Program |
| --- | --- | --- | --- |
| [corinth-canal](https://github.com/rmems/corinth-canal) | Reference telemetry-to-spiking-to-MoE loop and SAAQ validation | Research | [Hybrid / quantization](#hybrid-quantization) |
| [hybrid-fusion](https://github.com/rmems/hybrid-fusion) | Backend-independent ANN–SNN orchestration contracts | Research | [Hybrid / quantization](#hybrid-quantization) |
| [grok-ozempic](https://github.com/rmems/grok-ozempic) | Streaming Grok-1 quantization and fidelity experiments | Research | [Hybrid / quantization](#hybrid-quantization) |

### Hardware interfaces and acceleration

**Research components**

| Repository | Responsibility | Status | Program |
| --- | --- | --- | --- |
| [silicon-bridge](https://github.com/rmems/silicon-bridge) | Checked Q8.8 parameter export and host UART codecs | Published · Research | [Spikenaut / SNN](#spikenaut) |
| [myelin-accelerator](https://github.com/Limen-Neural/myelin-accelerator) | Reusable Rust/CUDA primitives for SNN, routing, and packed ternary operations | Published · Research | Hardware acceleration |

</details>

Explore all repositories and projects: [rmems](https://github.com/rmems?tab=repositories) · [Limen Neural](https://github.com/orgs/Limen-Neural/repositories) · [GitHub Projects](https://github.com/rmems?tab=projects).

---

## From monolith to modular systems

This ecosystem originated in a larger neuromorphic / AI research workspace. As interfaces and research directions matured, I progressively decomposed it into focused, interoperable repositories. Clearer boundaries support independent testing and releases, reuse, replaceable components, and experimentation, while making it easier to return to work after time away and compose larger research systems.

---

## Selected Hugging Face artifacts

[Full Hugging Face portfolio](https://huggingface.co/rmems)

- [**Spikenaut-SNN-Telemetry**](https://huggingface.co/datasets/rmems/Spikenaut-SNN-Telemetry) — telemetry for neuromorphic representation and replay experiments.
- [**Agentic Coding Trajectories**](https://huggingface.co/datasets/rmems/agentic-coding-trajectories) — historical synthetic coding episodes, distinct from Prometheus's real engineering trajectories. Raw, not training-ready, and blocked from model-weight updates under current project policy.

A published dataset or artifact does not establish training readiness or research success. Hosted frontier-model outputs remain research-only; training inputs require independent provenance, license, and project-policy eligibility.

---

## Attribution

Primary author and maintainer: **Raul Montoya Cardenas (rmems)**.

 Project-specific AI contributions remain attributed in commits, pull requests, experiment records, and release provenance.