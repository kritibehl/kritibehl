## Kriti Behl

MS CS @ University of Florida (Dec 2025) · Distributed Systems · Reliability Engineering · Backend Correctness

I build systems that stay correct under failure — lease-expiry races, network faults, concurrent crashes, production-like disruptions.

---

### Open Source

| PR | Repo | What | Status |
|---|---|---|---|
| [#2200](https://github.com/temporalio/sdk-go/pull/2200) | temporalio/sdk-go | Goroutine leak fix — child workflow test env (doneChannel not closed on all completion paths; idempotent sync.Once closure; regression test restructured per maintainer review) | ✅ Merged Mar 2, 2026 |
| [#2212](https://github.com/temporalio/sdk-go/pull/2212) | temporalio/sdk-go | OnWorkflow mock context propagation fix — ctxCopy missing header propagation before matcher evaluation; regression test added after maintainer request | ✅ Merged Mar 12, 2026 |
| [#26051](https://github.com/Azure/azure-sdk-for-go/pull/26051) | Azure/azure-sdk-for-go | Join request + body close errors in retry policy using errors.Join; realClose() errors no longer silently dropped | Under review |
| [#26106](https://github.com/Azure/azure-sdk-for-go/pull/26106) | Azure/azure-sdk-for-go | W3C Trace Context propagation (traceparent/tracestate) in HTTP trace policy | Under review |

Both Temporal PRs required maintainer-requested revisions. Both resolved in a single round.

---

### Projects

**[Faultline](https://github.com/kritibehl/faultline)** — Crash-safe distributed job queue. Prevents duplicate execution under lease-expiry races via fencing tokens + idempotent commits. Validated: 0 duplicate commits across 1,500 race reproductions at 0/5/10% network fault injection.

**[KubePulse](https://github.com/kritibehl/KubePulse)** — Kubernetes resilience validation. Declarative YAML disruption scenarios → automated scorecards (recovery time, p95 latency, error rate, readiness false-positive detection). CPU-stress: 8s recovery, ~210ms p95, score 86/100.

**[AutoOps-Insight](https://github.com/kritibehl/autoops-insight)** — CI failure analytics. Two-layer classification (rule-based + ML fallback), config-driven YAML rules, rule simulation engine, admin audit log, incident replay. 16 tests.

**[FairEval-Suite](https://github.com/kritibehl/FairEval-Suite)** — ML evaluation + regression-gating pipeline. DistilBERT inference, RAG-overlap scorer, release gate that blocks degraded candidates. Zenodo [doi:10.5281/zenodo.17625268](https://zenodo.org/record/17625268).

**[DetTrace](https://github.com/kritibehl/dettrace)** — Deterministic concurrency replay tool. C++17 + Swift. Identifies first divergence point in flaky concurrent runs. Swift companion: async/await, actor isolation, JSON+Markdown reports.

**[ResuMate](https://github.com/kritibehl/ResuMate)** — API-first document analysis workflow engine. Async job lifecycle, SHA-256 fingerprinting, schema-versioned contracts, role-gated access, audit trail. React/Next.js dashboard.

---

### Writing

[medium.com/@kriti0608](https://medium.com/@kriti0608) — distributed systems failures, reliability engineering, ML evaluation infrastructure

- [How I built a distributed job queue that stays correct under crashes, races, and network faults](https://medium.com/@kriti0608/how-i-built-a-distributed-job-queue-that-stays-correct-under-crashes-races-and-network-faults-48bc50eec723)
- [I thought I built observability. Then an incident proved I didn't.](https://medium.com/@kriti0608/i-thought-i-built-observability-then-an-incident-proved-i-didnt-9b749e0d4ff3)
- [Detecting silent regressions in GenAI systems at scale](https://medium.com/@kriti0608/detecting-silent-regressions-in-genai-systems-at-scale-039ec03db1e4)

---

📍 Gainesville, FL · Open to relocation · [LinkedIn](https://www.linkedin.com/in/kriti-behl/) · [Portfolio](https://kriti-portfolio-six.vercel.app)
