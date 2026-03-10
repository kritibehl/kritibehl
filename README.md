# Kriti Behl

**MS CS, University of Florida (Dec 2025) · GPA 3.8 · Gainesville, FL (Open to Relocation)**

I build correctness-first distributed systems and reliability tooling — crash-safe execution, deterministic debugging, resilience validation and ML evaluation infrastructure.

---

## Featured Projects

| Project | What it does | Key proof |
|---|---|---|
| [Faultline](https://github.com/kritibehl/faultline) | Crash-safe distributed job queue — lease-based ownership, fencing tokens, idempotent commit guards | 0 duplicate commits · 1,500 stale-write rejections across 1,500 fault-injected race reproductions (0/5/10% fault rates) |
| [KubePulse](https://github.com/kritibehl/KubePulse) | Kubernetes resilience validation — declarative disruption scenarios, automated scorecards, readiness false-positive detection | 8s recovery · ~210ms p95 · resilience score 86/100 |
| [DetTrace](https://github.com/kritibehl/dettrace) | C++17 deterministic concurrency replay + Swift companion analyzer (async/await, actor-isolated state) | First divergence isolated at event index 5 · 3 passing Swift tests |
| [FairEval Suite](https://github.com/kritibehl/FairEval-Suite) | CI-integrated GenAI evaluation and regression gating — real DistilBERT inference, release gate blocks score drops > 0.05 | 8 automated tests · [Hugging Face demo](https://huggingface.co/spaces/kriti0608/FairEval-Suite) · [Zenodo](https://doi.org/10.5281/zenodo.17625268) |
| [AutoOps-Insight](https://github.com/kritibehl/autoops-insight) | CI/infra failure analytics — 11 failure families, recurrence tracking, release-risk reporting | 11 FastAPI endpoints · 5 Prometheus counters · 14 passing tests |
| [ResuMate](https://github.com/kritibehl/ResuMate) | API-first document analysis workflow engine — batch jobs, run-to-run diffing, SHA-256 fingerprinting | 12 endpoints · 34 Python files · 10 test files |

---

## Open Source Contributions

| Repo | Contribution | Status |
|---|---|---|
| [Temporal Go SDK](https://github.com/temporalio/sdk-go) | Fixed goroutine leak in child-workflow test paths — enforced idempotent closure with sync.Once across exit paths | ✅ **Merged** |
| [Azure Go SDK (azcore)](https://github.com/Azure/azure-sdk-for-go) | Surfaced realClose() transport errors in retry policy using errors.Join — preserves transport-layer signal | 🔄 PR under review · CI passing |
| [Temporal Go SDK](https://github.com/temporalio/sdk-go) | Applied workflow context propagators in mock execution paths — closed gap between test and real runtime semantics | 🔄 PR under review |
| [Azure Go SDK](https://github.com/Azure/azure-sdk-for-go) | Implemented W3C Trace Context propagation (traceparent/tracestate) via OpenTelemetry in HTTP tracing pipeline | 🔄 PR under review · CI passing |

---

## ML & AI Safety Work

| Project | What it does | Links |
|---|---|---|
| [JailBreakDefense](https://github.com/kritibehl/JailBreakDefense) | Intent-preserving jailbreak defense — routes adversarial prompts through intent repair instead of blunt refusal | [Demo](https://huggingface.co/spaces/kriti0608/JailBreakDefense) · [Zenodo](https://doi.org/10.5281/zenodo.17694184) |
| [SpeechIntentEval](https://github.com/kritibehl/SpeechIntentEval) | Intent regression suite for indirect, polite, sarcastic, and ambiguous phrasing in assistant systems | [Demo](https://huggingface.co/spaces/kriti0608/SpeechIntentEval) |

---

## Tech Stack

**Languages:** Python · Go · C++ · Swift · Java · TypeScript · SQL  
**Backend:** FastAPI · Flask · Node.js/Express · REST APIs  
**Infra:** Docker · Kubernetes · AWS · Azure · GitHub Actions · CI/CD  
**Databases:** PostgreSQL · SQLite · MongoDB · Redis  
**Observability:** Prometheus · Grafana · structured logging  
**ML:** PyTorch · HuggingFace Transformers · DistilBERT · evaluation pipelines  
**Systems:** Distributed Systems · Concurrency Control · Fault Tolerance · Deterministic Replay · Network Fault Injection · Release Gating

---

## Writing

Technical posts on distributed system failures, reliability engineering, deterministic debugging, and GenAI regression detection.  
[Medium @kriti0608](https://medium.com/@kriti0608)

---

## Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-kriti--behl-0077B5?style=flat&logo=linkedin)](https://linkedin.com/in/kriti-behl)
[![Portfolio](https://img.shields.io/badge/Portfolio-kriti--portfolio-1F4E79?style=flat)](https://kriti-portfolio-six.vercel.app)
[![Email](https://img.shields.io/badge/Email-kriti0608@gmail.com-D14836?style=flat&logo=gmail)](mailto:kriti0608@gmail.com)
