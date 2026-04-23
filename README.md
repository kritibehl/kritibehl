# Kriti Behl

```
┌─────────────────────────────────────────────────────────────────────┐
│  reliability / infrastructure engineer                               │
│  builds systems that reason about when other systems are wrong       │
└─────────────────────────────────────────────────────────────────────┘
```

**3 merged PRs** in the [Temporal Go SDK](https://github.com/temporalio/sdk-go) · **2 PRs** under review in the Azure Go SDK  
M.S. Computer & Information Science · University of Florida · GPA 3.8  
Open to relocation · OPT/STEM OPT

---

## $ ls -la projects/

| project | what it does | stack | proof |
|---|---|---|---|
| **[Faultline](https://github.com/kritibehl/faultline)** | exactly-once distributed job execution under fault injection | Go · PostgreSQL · Docker | 0.0% duplicate commits vs 1.0–2.5% naive baseline · 1,500+ failure scenarios · zero invariant violations |
| **[KubePulse](https://github.com/kritibehl/KubePulse)** | deployment gate that catches what Kubernetes probes miss | Go · Terraform · K8s · Prometheus | p95 drifted 333%, error rate up 8% — probes still said healthy · blocked AMD MI300X rollout at +608% latency regression |
| **[DetTrace++](https://github.com/kritibehl/dettrace)** | failure forensics across distributed + firmware-style traces | Python · Go · C++17 · Swift | isolates first divergence at event index · covers race conditions, retry storms, cascading failures, UART IRQ, timer, GPIO |
| **[AutoOps-Insight](https://github.com/kritibehl/AutoOps-Insight)** | CI failure detection + release decision engine | Python · PostgreSQL · React | detects recurring failure patterns · generates confidence-scored release decisions |
| **[FairEval-Suite](https://github.com/kritibehl/FairEval-Suite)** | AI model release gate — quality + serving behavior | Python | blocked candidate with 47.1% p95 latency regression despite score parity · live on HuggingFace |
| **[AccelSim-Lite](https://github.com/kritibehl/accelsim-lite)** | C++ pipeline simulator for throughput + latency modeling | C++ · Python | 87% throughput improvement, 39% latency reduction demonstrated via what-if simulation |

---

## $ cat oss_contributions.log

```bash
# Temporal Go SDK — merged
[2026-03-02] PR #2200  MERGED  fix: goroutine leak in test runtime shutdown sequence
[2026-03-12] PR #2212  MERGED  fix: propagation headers missing in workflow mock matcher
[2026-04-20] PR #2298  MERGED  fix: async future reports ready while callers still blocked

# Azure Go SDK — under review
[2026-??-??] PR #26051 REVIEW  fix: azcore retry policy, errors.Join
[2026-??-??] PR #26106 REVIEW  feat: W3C Trace Context (traceparent/tracestate)
```

---

## $ ./career_identity.sh

```
> I build systems that reason about when other systems are wrong.

  Faultline  ─── proves correctness when workers fail
  KubePulse  ─── catches what health checks miss
  DetTrace++ ─── isolates the exact moment a system became incorrect
  FairEval   ─── blocks AI releases that regress under real load
  AutoOps    ─── detects CI failures before they become outages
```

---

## $ cat skills.conf

```ini
[languages]
primary    = Go
secondary  = Python, Java, JavaScript, SQL
systems    = C++, Bash

[backend]
apis       = REST, Node.js, Express
databases  = PostgreSQL, Alembic
patterns   = distributed job execution, fault injection, fencing tokens

[infrastructure]
cloud      = AWS (EKS, ECS, VPC)
containers = Kubernetes, Docker, Terraform
ci_cd      = GitHub Actions, CI pipelines

[observability]
tools      = Prometheus, Grafana, Datadog
practices  = SLO enforcement, incident response, replay-based debugging

[systems]
focus      = correctness under failure, resilience validation,
             deterministic replay, firmware-style trace analysis
```

---

## $ ping me

```
email     kriti0608@gmail.com
linkedin  linkedin.com/in/kriti-behl
portfolio kriti-portfolio-six.vercel.app
location  Gainesville, FL — open to relocation
```

---

<sub>Currently searching for SRE / Backend / Infrastructure roles · M.S. completed Dec 2025</sub>
