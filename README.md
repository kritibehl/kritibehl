<div align="center">

# Kriti Behl

**Backend · Distributed Systems · Reliability Engineering · AI Infrastructure**

*MS Computer & Information Science, University of Florida (Dec 2025) · GPA 3.8*

[![Portfolio](https://img.shields.io/badge/Portfolio-kriti--portfolio--six.vercel.app-000000?style=flat-square&logo=vercel&logoColor=white)](https://kriti-portfolio-six.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-kriti--behl-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/kriti-behl)
[![Medium](https://img.shields.io/badge/Writing-Medium-000000?style=flat-square&logo=medium&logoColor=white)](https://medium.com/@kriti0608)
[![HuggingFace](https://img.shields.io/badge/Demo-Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://huggingface.co/kriti0608)

</div>

---

## What I build

Systems that stay correct under failure — and tools that prove it.

Production backend experience at Thales Group. Three merged PRs in the Temporal Go SDK. Projects focused on one question: **what actually breaks, how do you know, and how do you prove it didn't happen twice?**

Most recently: extended KubePulse to real GPU inference serving on AMD MI300X hardware — same rollout-gating pipeline, real ROCm/vLLM stack, real latency regression that triggered a block decision.

---

## Projects

### [KubePulse](https://github.com/kritibehl/KubePulse) — Release safety for distributed systems and AI serving

Kubernetes resilience validation system that detects probe-level false positives and blocks unsafe deployments. Extended to real GPU inference serving on AMD MI300X hardware.

**Distributed systems result:** `probes_say_healthy=true`, `safe_to_operate=false`, `recommendation_action=block` — p95 latency at +333% drift, 8% error rate, resilience score 46 — readiness probes stayed green through all of it.

**AI serving result (AMD MI300X):** baseline p95 200.76 ms → burst p95 1422.07 ms (+608.34% regression) under long-prompt load — ROCm/vLLM serving stack, Phi-3-mini-4k-instruct, block decision generated from measured latency behavior.

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)](https://kubernetes.io)
[![AMD MI300X](https://img.shields.io/badge/AMD%20MI300X-ROCm%20%2B%20vLLM-ED1C24?style=flat-square&logo=amd&logoColor=white)](https://github.com/kritibehl/KubePulse/tree/main/amd_results)
[![Terraform](https://img.shields.io/badge/Terraform-AWS%20EKS-7B42BC?style=flat-square&logo=terraform&logoColor=white)](https://terraform.io)

---

### [Faultline](https://github.com/kritibehl/faultline) — Distributed correctness under failure

Crash-safe job execution system enforcing exactly-once semantics through fencing tokens and database-level invariant validation.

**The benchmark:** 0.0% duplicate commits at 5%, 10%, and 20% fault injection rates — versus 1.0–2.5% in naive lease-only systems across 200-job runs. 1,500+ simulated failure scenarios. Zero invariant violations.

**The finding:** Nearly 46% of execution time is coordination overhead. Measured, not assumed.

`Go` `PostgreSQL` `Docker`

---

### [FairEval](https://github.com/kritibehl/FairEval-Suite) — Release gating for AI systems

LLM regression gating system — evaluates model candidates, detects silent regressions, and makes automated SHIP/BLOCK deployment decisions.

**Run against Gemini Flash:** 0.367 avg score, 40% pass rate, gate decision: BLOCK. Live demo on Hugging Face. Technical report on Zenodo.

`Python` `PyTorch` `FastAPI` `SciPy` `HuggingFace`

&nbsp;&nbsp;[**Live demo →**](https://huggingface.co/spaces/kriti0608/FairEval-Suite) &nbsp;&nbsp; [**Research report →**](https://doi.org/10.5281/zenodo.17625268)

---

### [DetTrace](https://github.com/kritibehl/dettrace) — First-failure isolation

Deterministic replay and incident forensics system for concurrency and distributed failures.

**What it does:** Records execution as an event sequence. Replays identically. Isolates first divergence at exact event-index granularity. Predicts downstream failure propagation.

**Demonstrated:** First divergence isolated at event index 5. Cross-incident similarity matching at 1.0 confidence.

`C++17` `Swift` `CMake`

---

### [AutoOps-Insight](https://github.com/kritibehl/AutoOps-Insight) — CI failure intelligence

Operator-facing incident triage tool. Classifies CI failures into named families, generates stable fingerprints, detects recurrence, and generates rollout guidance.

`Python` `FastAPI` `React` `PostgreSQL` `Alembic`

---

### [AccelSim-Lite](https://github.com/kritibehl/accelsim-lite) — Accelerator pipeline simulation

Deterministic workload-level simulator: throughput (0.14–0.33 ops/cycle), latency (10–23.8 cycles), bottleneck transitions across compute-heavy, memory-bound, and queue-pressure workloads. ~2.4× throughput degradation under memory pressure — the same behavior transformer inference sees under KV-cache bandwidth saturation.

`C++` `CMake`

---

### [AgentGrid-Demo](https://github.com/kritibehl/agentgrid-demo) — Agentic document triage

LangGraph agentic workflow that classifies documents, extracts operational risks, and routes each to the right owner with a structured action plan.

`Python` `LangGraph`

---

## Open Source

Three merged PRs in the **Temporal Go SDK** (production durable-execution framework):

- **[#2200](https://github.com/temporalio/sdk-go/pull/2200)** — Tracked down a resource leak in the Go SDK test runtime; goroutines were silently accumulating on certain exit paths, causing flaky test behavior; fixed the shutdown sequence and added leak detection to the regression suite.
- **[#2212](https://github.com/temporalio/sdk-go/pull/2212)** — Fixed a silent correctness bug in workflow mock testing; propagation headers were missing during matcher evaluation, so tests passed incorrectly; added a regression test that reliably catches the failure.
- **[#2298](https://github.com/temporalio/sdk-go/pull/2298)** — Fixed a concurrency bug in async future chaining where a future could report ready while callers were still blocked; corrected the completion path to properly unblock waiters and propagate results to dependent futures.

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
Languages:      Go · Python · C++17 · Swift · Java · TypeScript · SQL
Backend:        FastAPI · Flask · Node.js/Express · REST APIs · vLLM
Storage:        PostgreSQL · Redis · MongoDB · SQLite
Infrastructure: Docker · Kubernetes · AWS · Azure · Terraform · GitHub Actions
Hardware:       AMD MI300X · ROCm
Observability:  Prometheus · Grafana · OpenTelemetry · structured logging · fault injection
Systems:        Distributed systems · fault tolerance · concurrency control · idempotency · AI serving validation
```

---

<div align="center">
<sub>Open to full-time SWE roles · Dec 2025 · OPT (STEM extension eligible) · Open to relocation</sub>
</div>
