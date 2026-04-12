<div align="center">

# Kriti Behl

**Backend · Distributed Systems · Reliability Engineering**

*MS Computer & Information Science, University of Florida (Dec 2025) · GPA 3.8*

[![Portfolio](https://img.shields.io/badge/Portfolio-kriti--portfolio--six.vercel.app-000000?style=flat-square&logo=vercel&logoColor=white)](https://kriti-portfolio-six.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-kriti--behl-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/kriti-behl)
[![Medium](https://img.shields.io/badge/Writing-Medium-000000?style=flat-square&logo=medium&logoColor=white)](https://medium.com/@kriti0608)
[![HuggingFace](https://img.shields.io/badge/Demo-Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://huggingface.co/kriti0608)

</div>

---

## What I build

Systems that stay correct under failure — and tools that prove it.

Production backend experience at Thales Group. Merged PRs in the Temporal Go SDK. Projects focused on one question: **what actually breaks, how do you know, and how do you prove it didn't happen twice?**

---

## Projects

### [Faultline](https://github.com/kritibehl/faultline) — Distributed correctness under failure

Crash-safe job execution system enforcing exactly-once semantics through fencing tokens and database-level invariant validation.

**The benchmark:** 0.0% duplicate commits at 5%, 10%, and 20% fault injection rates — versus 1.0–2.5% in naive lease-only systems across 200-job runs. 1,500+ simulated failure scenarios. Zero invariant violations.

**The finding:** Nearly 46% of execution time is coordination overhead. Measured, not assumed.

`Python` `PostgreSQL` `Prometheus` `OpenTelemetry` `Docker`

---

### [KubePulse](https://github.com/kritibehl/KubePulse) — When probes lie

Kubernetes resilience validation system that detects probe-level false positives and blocks unsafe deployments.

**Demonstrated:** `probes_say_healthy=true`, `safe_to_operate=false`, `recommendation_action=block` — with p95 latency at 780ms (+333% drift), p99 at 1200ms (+275% drift), 8% error rate, resilience score 46 — while readiness probes stayed green.

**Infrastructure:** Terraform-provisioned AWS EKS. CI-integrated resilience gate. AI service scenario packs.

`Python` `Kubernetes` `Prometheus` `Terraform` `GitHub Actions`

---

### [DetTrace](https://github.com/kritibehl/dettrace) — First-failure isolation

Deterministic replay and incident forensics system for concurrency and distributed failures.

**What it does:** Records execution as an event sequence. Replays identically. Isolates first divergence at exact event-index granularity. Predicts downstream failure propagation. Learns patterns across incidents.

**Demonstrated:** First divergence isolated at event index 5. Cross-incident similarity matching at 1.0 confidence. Control-loop replay across sensor fault, actuator saturation, and timing jitter scenarios.

Swift companion with `async/await` and actor isolation for safe concurrent artifact analysis.

`C++17` `Swift` `CMake` `JSONL`

---

### [FairEval](https://github.com/kritibehl/FairEval-Suite) — Release gating for AI systems

LLM regression gating system — evaluates model candidates, detects silent regressions, and makes automated SHIP/BLOCK deployment decisions.

**Run against Gemini Flash:** 0.367 avg score, 40% pass rate, gate decision: BLOCK. Live demo on Hugging Face. Technical report on Zenodo.

`Python` `PyTorch` `FastAPI` `SciPy` `HuggingFace`

&nbsp;&nbsp;[**Live demo →**](https://huggingface.co/spaces/kriti0608/FairEval-Suite) &nbsp;&nbsp; [**Research report →**](https://doi.org/10.5281/zenodo.17625268)

---

### [AgentGrid-Demo](https://github.com/kritibehl/agentgrid-demo) — Agentic document triage

LangGraph agentic workflow that classifies construction and project documents, extracts operational risks, and routes each document to the right owner with a structured action plan — demonstrating multi-step agent execution over a real document processing pipeline.

`Python` `LangGraph`

---

### [AutoOps-Insight](https://github.com/kritibehl/AutoOps-Insight) — CI failure intelligence

Operator-facing incident triage tool. Classifies CI failures into named families, generates stable fingerprints, detects recurrence, correlates with nearby changes, simulates rule changes, and generates rollout guidance.

React dashboard · Fleet health views · Rule simulation · Power BI export.

`Python` `FastAPI` `React` `PostgreSQL` `Alembic`

---

### [AccelSim-Lite](https://github.com/kritibehl/accelsim-lite) — Accelerator pipeline simulation

Deterministic workload-level simulator: throughput (0.14–0.33 ops/cycle), latency (10–23.8 cycles), bottleneck transitions (WaitingDependency → NoMemoryPort → NoComputeUnit) across compute-heavy, memory-bound, and queue-pressure workloads. ~2.4× throughput degradation under memory pressure — the same behavior transformer inference sees under KV-cache bandwidth saturation.

`C++` `CMake`

---

## Open Source

Two merged PRs in the **Temporal Go SDK** (production durable-execution framework):

- **[#2200](https://github.com/temporalio/sdk-go/pull/2200)** — Fixed goroutine leak in child-workflow test environment. Added `sync.Once` idempotent closure with regression test.
- **[#2212](https://github.com/temporalio/sdk-go/pull/2212)** — Fixed `OnWorkflow` mock to observe propagated context headers.

Two PRs under review in the **Azure Go SDK**.

---

## Writing

Technical writing grounded in production systems — not career content.

- [How I Built a Distributed Job Queue That Stays Correct Under Crashes, Races, and Network Faults](https://medium.com/@kriti0608/how-i-built-a-distributed-job-queue-that-stays-correct-under-crashes-races-and-network-faults-48bc50eec723)
- [Detecting Silent Regressions in GenAI Systems at Scale](https://medium.com/@kriti0608/detecting-silent-regressions-in-genai-systems-at-scale-039ec03db1e4)
- [I Thought I Built Observability. Then an Incident Proved I Didn't.](https://medium.com/@kriti0608/i-thought-i-built-observability-then-an-incident-proved-i-didnt-9b749e0d4ff3)
- [FairEval: A Human-Aligned Evaluation Framework for Generative Models](https://medium.com/@kriti0608/faireval-a-human-aligned-evaluation-framework-for-generative-models-d822bfd5c99d)

---

## Stack

```
Languages:     Go · Python · C++17 · Swift · Java · TypeScript · SQL
Backend:       FastAPI · Flask · Node.js/Express · REST APIs
Storage:       PostgreSQL · Redis · MongoDB · SQLite
Infrastructure: Docker · Kubernetes · AWS · Azure · Terraform · GitHub Actions
Observability:  Prometheus · Grafana · OpenTelemetry · structured logging · fault injection
Systems:       Distributed systems · fault tolerance · concurrency control · idempotency · deterministic replay
```

---

<div align="center">
<sub>Open to full-time SWE roles · Dec 2025 · OPT (STEM extension eligible) · Open to relocation</sub>
</div>
