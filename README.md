# Kriti Behl

**Software Engineer | Backend · Distributed Systems · Reliability**

M.S. Computer Science, University of Florida · Dec 2025 · GPA 3.8
Open-source contributor to **Temporal Go SDK** and **Azure SDK for Go**
Chicago, IL · Open to relocation

[![Temporal Go SDK](https://img.shields.io/badge/Temporal_Go_SDK-7_merged_PRs-3fb950?style=flat-square&logo=go&logoColor=white)](https://github.com/temporalio/sdk-go/pulls?q=author%3Akritibehl)
[![Azure SDK](https://img.shields.io/badge/Azure_Go_SDK-1_merged_1_in_review-d29922?style=flat-square&logo=microsoftazure&logoColor=white)](https://github.com/Azure/azure-sdk-for-go/pulls?q=author%3Akritibehl)
[![University of Florida](https://img.shields.io/badge/M.S._Computer_Science-UF-58a6ff?style=flat-square)](https://www.cise.ufl.edu/)

> I build backend and infrastructure systems that stay correct when failures, concurrency, and regressions make behavior difficult to reason about.

---

## Open Source

**Temporal Go SDK — 7 merged PRs**

- Fixed goroutine leak in test runtime shutdown — [#2200](https://github.com/temporalio/sdk-go/pull/2200)
- Fixed `OnWorkflow` mock to see propagated context headers — [#2212](https://github.com/temporalio/sdk-go/pull/2212)
- Added task poller-type instrumentation for scalable task pollers — [#2248](https://github.com/temporalio/sdk-go/pull/2248)
- Fixed already-ready future chaining to properly complete destination futures — [#2298](https://github.com/temporalio/sdk-go/pull/2298)
- Documented worker activity rate-limit timeout caveat — [#2367](https://github.com/temporalio/sdk-go/pull/2367)
- Added external-storage support for query results — [#2459](https://github.com/temporalio/sdk-go/pull/2459)
- Fixed legacy query task failure reporting — [#2639](https://github.com/temporalio/sdk-go/pull/2639)

**Azure SDK for Go**

- Fixed `azcore` retry-policy error composition using `errors.Join` — [#26051](https://github.com/Azure/azure-sdk-for-go/pull/26051) (merged)
- W3C Trace Context support (traceparent/tracestate) — [#26106](https://github.com/Azure/azure-sdk-for-go/pull/26106) (in review)

---

## Selected Projects

### [Faultline](https://github.com/kritibehl/faultline) — distributed job execution correctness

Lease-based job systems have a gap: lease expiry stops the *next* worker from waiting, but it does not stop the *old* worker from writing late after it recovers from a crash or network partition. That stale write is what corrupts ledgers and causes double-charges.

Faultline closes that gap by rejecting stale writes **at the database boundary**, not in application logic — a `UNIQUE(job_id, fencing_token)` constraint in Postgres means a recovered worker holding an old token gets rejected by the database itself, regardless of what the application code does. Each job claim increments a fencing token; if worker A stalls and worker B takes over and commits with a newer token, worker A's eventual late commit is rejected because its token is strictly older.

Validated across 1,500+ injected failure scenarios (crash, lease takeover, retry storm under 50+ concurrent retries, duplicate submission, partial write + crash) with **0 duplicate commits and 0 invariant violations**, benchmarked against a naive queue that produced 12 duplicates under the same 20% fault-injection rate. Includes a reconciler that repairs incomplete jobs and converges stale state, a Go inspector API for live lease-risk state, and Prometheus/OTEL instrumentation for stale-rejection rate and claim latency.

`Python (primary) · Go (inspector API) · PostgreSQL · Docker · Prometheus · OpenTelemetry`

### [KubePulse](https://github.com/kritibehl/KubePulse) — release-safety validation across the stack

Kubernetes readiness probes check whether a container is alive, not whether the deployment is safe for users. A service can pass every probe while DNS is failing, p95 latency has tripled, and the error budget is at zero — and the next deployment wave rolls out anyway.

KubePulse runs a 4-layer validation gate (health signals → network validation → SLO/error-budget evaluation → probe-integrity divergence check) and issues an explicit release decision. In controlled testing it blocked 5 dangerous deployments that all showed `probes_say_healthy: true`, including a cascade where p95 latency rose **+333%** and error rate hit 8% while every readiness probe stayed green.

It also includes a validated networking layer underneath the Kubernetes-facing tooling: a two-AS eBGP topology built with FRRouting and Linux network namespaces, with explicit prefix import/export policies and measured **251ms median / 270ms p95** data-plane recovery across 10 fault-injection runs tracing withdrawals from the BGP RIB into the kernel FIB; and a Layer-2 lab (VLAN-aware bridges, 802.1Q trunks, router-on-a-stick inter-VLAN routing) where a deliberately introduced trunk fault produced 100% loss isolated to a single VLAN, diagnosed and rolled back with packet-capture evidence.

`Python · FastAPI · Kubernetes · Terraform · FRRouting · Prometheus · Docker Compose`

### [DetTrace](https://github.com/kritibehl/dettrace) — first-failure isolation via deterministic replay

Debugging concurrent and distributed failures is asymmetric: failures are easy to observe and hard to locate, because logs record state changes after they happen — the event that actually caused the failure often isn't logged at all.

DetTrace generates an expected deterministic trace, replays the divergent execution, and binary-searches over the two to isolate the **first divergence index** — not the last visible symptom. Validated across a 20-scenario I/O transport corpus (SPI, I2C, UART, GPIO interrupt races, and a distributed retry-storm scenario) with 10,000+ trace validations, 0.93 root-cause confidence, and 0 false positives in the validation corpus (documented ~7% false-positive rate on identified root cause in general use, with downstream confidence scoring to catch most of them). The C++17 replay engine passes 47 GoogleTest cases clean under AddressSanitizer and UndefinedBehaviorSanitizer; a Swift async/await layer handles concurrent analysis of large trace corpora without analysis-time races.

The README is explicit about scope: firmware scenarios are trace simulations, not driver/kernel-level implementations, and the API layer is a proof of concept — a distinction worth being able to explain in an interview as clearly as the mechanism itself.

`C++17 · CMake · GoogleTest · Swift · Python (FastAPI)`

### [AgentGrid](https://github.com/kritibehl/agentgrid) — making AI agent failure modes observable

Production GenAI systems fail in ways that are hard to see in aggregate metrics: retrieval misses the relevant document, a tool call silently returns a stale result, an answer generates without grounding. A single pass-rate number hides all of this.

AgentGrid instruments every stage of an agent pipeline (triage → retrieval → tool execution → generation → eval gate → optional human review) with per-stage metrics rather than one end-to-end score, and gates releases on retrieval hit rate, tool success rate, p95 latency, and drift signals. Current measured state: 80% retrieval hit rate, 80% tool success rate, 880ms p95 — gated to a `HOLD` decision rather than shipped, with the hold reason (quality risk on an entity-search scenario) surfaced explicitly rather than averaged away. 57 tests passing.

`Python · FastAPI · React/TypeScript · Redis · Prometheus`

<details>
<summary><b>More projects</b></summary>

- [FairEval](https://github.com/kritibehl/FairEval-Suite) — blocks AI releases that regress under real serving load
- [AccelSim-Lite](https://github.com/kritibehl/accelsim-lite) — names throughput/latency bottlenecks and gates the regression
- [AutoOps-Insight](https://github.com/kritibehl/AutoOps-Insight) — detects CI/CD failures before they reach production
- [Enterprise Process Lab](https://github.com/kritibehl/enterprise-process-lab) — validates ERP integrations and controls compliance

</details>

---

## Experience

**Meta × MLH — Production Engineering Fellow** (June–September 2026)
- Deployed and operated a Linux-hosted Flask service on a cloud VPS with SSH access, DuckDNS routing, host/port binding, Python virtualenv dependency management, and tmux-based process persistence
- Automated redeployment with a Bash script covering 6+ manual operational steps: GitHub sync, repo reset, virtualenv activation, dependency installation, stale tmux cleanup, and Flask service restart
- Built Bash/Python automation for API parsing, regex matching, process debugging, and Apache log analysis across a 237MB multi-million-line dataset, extracting 2.9M+ unique source IPs and HTTP status-code distributions

---

## Technical Skills

**Languages:** Python, Go, C++, Java, SQL, Bash, JavaScript
**Backend:** REST APIs, FastAPI, PostgreSQL, distributed job execution, concurrency, idempotency
**Infrastructure:** Kubernetes, Docker, Terraform, AWS, GitHub Actions
**Systems:** Linux, TCP/IP, distributed systems, fault tolerance, transactional correctness
**Observability:** Prometheus, Grafana, OpenTelemetry, Datadog

---

## Contact

email: kriti0608@gmail.com
linkedin: [linkedin.com/in/kriti-behl](https://www.linkedin.com/in/kriti-behl/)
portfolio: [kriti-portfolio-six.vercel.app](https://kriti-portfolio-six.vercel.app)

**Open to Software Engineering opportunities in the U.S. · Open to relocation**
