<!-- KRITI BEHL — GitHub Profile README -->
<!-- Paste this into kritibehl/kritibehl/README.md -->

```
╔══════════════════════════════════════════════════════════════════╗
║  kriti@github:~$ whoami                                          ║
║                                                                  ║
║  Kriti Behl — reliability / infrastructure engineer              ║
║  builds systems that reason about when other systems are wrong   ║
╚══════════════════════════════════════════════════════════════════╝
```

[![Temporal SDK](https://img.shields.io/badge/Temporal_Go_SDK-5_merged_PRs-3fb950?style=flat-square&logo=go&logoColor=white)](https://github.com/temporalio/sdk-go/pulls?q=author%3Akritibehl)
[![Azure SDK](https://img.shields.io/badge/Azure_Go_SDK-1_merged_1_in_review-d29922?style=flat-square&logo=microsoftazure&logoColor=white)](https://github.com/Azure/azure-sdk-for-go/pulls?q=author%3Akritibehl)
[![UF](https://img.shields.io/badge/M.S._UF-GPA_3.8-58a6ff?style=flat-square)](https://www.cise.ufl.edu/)
[![Open to work](https://img.shields.io/badge/open_to-relocation-a5a6f6?style=flat-square)]()

---

## `$ ls -la projects/`

| project | what it catches | stack | proof |
|---|---|---|---|
| **[Faultline](https://github.com/kritibehl/faultline)** | stale workers corrupting distributed job state | Go · PostgreSQL · Docker | `0.0%` duplicate commits vs `1.0–2.5%` naive · 1,500+ failure scenarios · 0 invariant violations |
| **[KubePulse](https://github.com/kritibehl/KubePulse)** | deployment regressions that health probes miss | Go · Terraform · K8s · Prometheus | p95 drifted `+333%` with probes still green · 5 scenarios · 0 false-safe decisions |
| **[DetTrace](https://github.com/kritibehl/dettrace)** | the exact event where a system became incorrect | C++17 · Swift · Python · Go | 20 I/O transport scenarios · 10,000+ validations · confidence 0.93 · 0 false positives |
| **[AgentGrid](https://github.com/kritibehl/agentgrid-demo)** | silent failures in AI retrieval and tool execution | Python · FastAPI · React | retrieval 80% · tools 80% · p95 880ms · eval gates + human review |
| **[FairEval](https://github.com/kritibehl/FairEval-Suite)** | AI models that regress under real serving load | Python · FastAPI · SciPy | 16 false allows prevented · blocked `+47.1%` p95 regression despite score parity |
| **[Enterprise Process Lab](https://github.com/kritibehl/enterprise-process-lab)** | ERP integration failures and controls violations | Python · ABAP Reporting · pytest | SAP → Oracle → ServiceNow → Workday · 4 integrations · 5 controls · DO_NOT_RELEASE |
| **[AccelSim-Lite](https://github.com/kritibehl/accelsim-lite)** | throughput and latency bottleneck transitions | C++17 · CMake · GoogleTest | `3.64×` optimization speedup · `+51.22%` p95 regression detected and gated |
| **[AutoOps-Insight](https://github.com/kritibehl/AutoOps-Insight)** | CI/CD failures before they reach production | Python · FastAPI · React · Scikit-learn | 12 customers at risk · `+40%` escalation growth · DependencyError classified |

---

## `$ cat oss.log`

```bash
[2026-03-02]  PR #2200  MERGED  Temporal Go SDK  fix: goroutine leak in test runtime shutdown
[2026-03-12]  PR #2212  MERGED  Temporal Go SDK  fix: propagation headers missing in mock matcher
[2026-04-20]  PR #2298  MERGED  Temporal Go SDK  fix: async future reports ready while callers blocked
[2026-04-28]  PR #26051 MERGED  Azure Go SDK     fix: azcore retry policy, errors.Join
[in review ]  PR #26106 REVIEW  Azure Go SDK     feat: W3C Trace Context (traceparent/tracestate)
```

---

## `$ ./identity.sh`

```
> I build systems that reason about when other systems are wrong.

  Faultline             ── proves correctness when distributed workers fail
  KubePulse             ── catches regressions that health probes never see
  DetTrace              ── isolates the exact event where behavior became wrong
  AgentGrid             ── makes AI agent behavior observable and gateable
  FairEval              ── blocks AI releases that regress under real serving load
  Enterprise Process Lab── validates ERP integrations and controls compliance
  AccelSim-Lite         ── names the bottleneck and gates the regression
  AutoOps-Insight       ── detects CI failures before they become production outages

  M.S. Computer & Information Science · University of Florida · GPA 3.8
```

---

## `$ cat skills.conf`

```ini
[languages]
primary  = Go
other    = Python, C++17, Swift, Java, SQL, Bash, JavaScript

[backend]
apis     = REST, FastAPI, Node.js, Express, PostgreSQL
patterns = fault injection, fencing tokens, distributed job execution,
           idempotency, transactional correctness, ERP integrations

[infrastructure]
cloud    = AWS (EKS, ECS, VPC)
tools    = Kubernetes, Terraform, Docker, Git, GitHub Actions

[observability]
stack    = Prometheus, Grafana, Datadog, OpenTelemetry
practice = SLO enforcement, incident response, replay-based debugging,
           release gating, eval ops

[focus]
core     = correctness under failure, resilience validation,
           deterministic replay, AI reliability, enterprise systems
```

---

## `$ ping kriti`

```
email      kriti0608@gmail.com
linkedin   linkedin.com/in/kriti-behl
portfolio  kriti-portfolio-six.vercel.app
location   Chicago IL → open to full relocation
status     actively searching · SRE / Backend / Infra / Enterprise Apps · OPT/STEM OPT
```

---

<sub>Seeking SRE · Backend · Infrastructure · Platform · Enterprise Applications roles · M.S. completed Dec 2025</sub>
