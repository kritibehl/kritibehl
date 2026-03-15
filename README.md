# Kriti Behl

Backend and systems engineer focused on distributed systems correctness, fault-tolerant services, deterministic debugging, and reliability tooling.

Recently completed M.S. in Computer Science at the University of Florida. I build crash-safe execution systems, resilience validation tooling, and release-quality evaluation infrastructure.

---

## Featured Work

### [Faultline](https://github.com/kritibehl/faultline)
Crash-safe distributed job queue with lease-based ownership, fencing tokens, and idempotent commit guards.

**Proof:** 0 duplicate commits and 1,500 stale-write rejections across 1,500 fault-injected race reproductions at 0/5/10% fault rates.

### [KubePulse](https://github.com/kritibehl/KubePulse)
Kubernetes resilience validation framework with declarative disruption scenarios, automated scorecards, and readiness false-positive detection.

**Proof:** 8s recovery, ~210ms p95 latency, and resilience score 86/100 in validated stress scenarios.

### [DetTrace](https://github.com/kritibehl/dettrace)
Deterministic concurrency replay system in C++17 with a Swift companion analyzer for async/await and actor-isolated state.

**Proof:** isolated first divergence at event index 5 and validated Swift replay analysis with passing test coverage.

### [FairEval Suite](https://github.com/kritibehl/FairEval-Suite)
CI-integrated GenAI evaluation and regression gating with real DistilBERT inference and threshold-based release blocking.

**Proof:** automated regression gate for score drops > 0.05, plus [Hugging Face demo](https://huggingface.co/spaces/kriti0608/FairEval-Suite) and [Zenodo artifact](https://doi.org/10.5281/zenodo.17625268).

### [AutoOps-Insight](https://github.com/kritibehl/autoops-insight)
CI and infrastructure failure analytics platform for recurrence tracking, release-risk reporting, and operational visibility.

**Proof:** 11 FastAPI endpoints, 5 Prometheus counters, and 14 passing tests.

### [ResuMate](https://github.com/kritibehl/ResuMate)
API-first document analysis workflow engine with batch jobs, run-to-run diffing, auditability, and SHA-256 fingerprinting.

**Proof:** 12 endpoints, 34 Python files, and 10 test files.

---

## Open Source

### [Temporal Go SDK](https://github.com/temporalio/sdk-go)
- Fixed a goroutine leak in child-workflow test paths by enforcing idempotent closure with `sync.Once`. **Merged**
- Applied workflow context propagators in mock execution paths so tests observe propagated headers like real runtime. **Merged**

### [Azure Go SDK (azcore)](https://github.com/Azure/azure-sdk-for-go)
- Surfaced transport `realClose()` errors in retry policy with `errors.Join` so close-path failures are preserved. **PR under review**
- Implemented W3C Trace Context propagation (`traceparent` / `tracestate`) in the HTTP tracing pipeline. **PR under review**

---

## Additional Work

- [JailBreakDefense](https://github.com/kritibehl/JailBreakDefense) — intent-preserving jailbreak defense with [demo](https://huggingface.co/spaces/kriti0608/JailBreakDefense) and [Zenodo](https://doi.org/10.5281/zenodo.17694184)
- [SpeechIntentEval](https://github.com/kritibehl/SpeechIntentEval) — intent regression suite for indirect, polite, sarcastic, and ambiguous assistant prompts

---

## Tech

**Languages:** Python, Go, C++, Swift, Java, TypeScript, SQL  
**Backend:** FastAPI, Flask, Node.js/Express, REST APIs  
**Infra:** Docker, Kubernetes, AWS, Azure, GitHub Actions, CI/CD  
**Databases:** PostgreSQL, SQLite, MongoDB, Redis  
**Observability:** Prometheus, Grafana, structured logging  
**ML:** PyTorch, Hugging Face Transformers, DistilBERT, evaluation pipelines  
**Systems:** Distributed systems, concurrency control, fault tolerance, deterministic replay, network fault injection, release gating

---

## Writing

I write about distributed failures, reliability engineering, deterministic debugging and GenAI regression detection on [Medium](https://medium.com/@kriti0608).

---

## Connect

- [LinkedIn](https://linkedin.com/in/kriti-behl)
- [GitHub](https://github.com/kritibehl)
- [Portfolio](https://kriti-portfolio-six.vercel.app)
- [Medium](https://medium.com/@kriti0608)

---

Open to backend, systems, reliability, platform and infrastructure engineering roles.
