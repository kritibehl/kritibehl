# Kriti Behl

**Backend · Distributed Systems · Reliability**

Backend engineer focused on correctness under failure, observability, and production-shaped systems tooling. I build and validate systems with fault injection, deterministic debugging, resilience analysis, and measurable recovery behavior.

Two merged PRs in the Temporal Go SDK. Additional Azure Go SDK contributions under review.

---

## Open Source

- **Temporal Go SDK** — merged fixes in workflow and test behavior, including goroutine-leak prevention and workflow-context handling improvements
- **Azure Go SDK for Go** — contributions around retry error surfacing and distributed tracing / W3C trace-context propagation
- Interested in reliability, debugging, observability, workflow systems, and failure-oriented engineering

---

## Selected Projects

### [Faultline](https://github.com/kritibehl/faultline)
Distributed job execution system designed for correctness under crashes, lease expiry, retries, and worker races.

- Built lease-based worker ownership with fencing tokens and stale-write prevention
- Added deterministic fault-injection paths to reproduce race conditions and validate recovery behavior
- Exposed operational metrics for claim failures, retries, reconnects, stale-commit prevention, and recovery flow visibility

### [KubePulse](https://github.com/kritibehl/KubePulse)
Kubernetes resilience validation framework for measuring service behavior under infrastructure and network faults.

- Simulates DNS failures, latency, packet loss, and related degradation scenarios in Kubernetes environments
- Produces Prometheus / Grafana-backed resilience insights with recovery-oriented observability
- Focused on service health, failure impact visibility, and production-style reliability analysis

### [AutoOps-Insight](https://github.com/kritibehl/AutoOps-Insight)
Operator-facing incident and CI failure analysis platform for recurring failure detection and triage support.

- Built configurable incident classification, auditability, and rule-driven failure-family grouping
- Added workflows for rollback preview, remediation guidance, and incident correlation
- Designed to reduce triage ambiguity and improve operator-facing debugging clarity

### [DetTrace](https://github.com/kritibehl/dettrace)
Deterministic replay and concurrency-debugging toolkit for analyzing race-prone behavior through trace comparison.

- Compares expected vs. actual execution traces to surface behavioral divergence
- Supports invariant verification and replay-oriented debugging for concurrency-sensitive systems
- Built to make hard-to-reproduce failures easier to reason about and validate

---

## More Projects

- [FairEval Suite](https://github.com/kritibehl/FairEval-Suite) — deterministic evaluation and regression analysis tooling for GenAI systems
- [Portfolio Website](https://github.com/kritibehl/portfolio) — personal site highlighting projects, writing, and technical focus
- Additional backend, infra, and evaluation work across debugging, reliability, and system validation

---

## Technical Focus

**Languages:** Go, Python, C++17, Java, TypeScript, SQL  
**Infrastructure:** Kubernetes, Docker, GitHub Actions, Prometheus, Grafana, OpenTelemetry  
**Data & Storage:** PostgreSQL, Redis, SQLite, MongoDB  
**Areas:** distributed systems, reliability engineering, observability, deterministic debugging, fault injection, incident analysis

---

## Writing

- [Detecting Silent Regressions in GenAI Systems at Scale](https://medium.com/@kriti0608)
- [The Day My Distributed System Failed — and Why That Was the Point](https://medium.com/@kriti0608)

---

## Links

- **LinkedIn:** [linkedin.com/in/kriti-behl](https://www.linkedin.com/in/kriti-behl/)
- **GitHub:** [github.com/kritibehl](https://github.com/kritibehl)
- **Medium:** [medium.com/@kriti0608](https://medium.com/@kriti0608)
- **Email:** kriti0608@gmail.com

---

## What I’m Looking For

I’m most interested in backend, distributed systems, reliability, SRE, platform, and production engineering roles where correctness, observability, and failure handling matter.
