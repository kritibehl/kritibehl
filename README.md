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

[![Temporal SDK](https://img.shields.io/badge/Temporal_Go_SDK-4_merged_PRs-3fb950?style=flat-square&logo=go&logoColor=white)](https://github.com/temporalio/sdk-go/pulls?q=author%3Akritibehl)
[![Azure SDK](https://img.shields.io/badge/Azure_Go_SDK-2_PRs_in_review-d29922?style=flat-square&logo=microsoftazure&logoColor=white)](https://github.com/Azure/azure-sdk-for-go/pulls?q=author%3Akritibehl)
[![UF](https://img.shields.io/badge/M.S._UF-GPA_3.8-58a6ff?style=flat-square)](https://www.cise.ufl.edu/)
[![Open to work](https://img.shields.io/badge/open_to-relocation-a5a6f6?style=flat-square)]()

---

## `$ ls -la projects/`

| project | what it catches | stack | proof |
|---|---|---|---|
| **[Faultline](https://github.com/kritibehl/faultline)** | stale workers corrupting distributed job state | Go · PostgreSQL · Docker | `0.0%` duplicate commits vs `1.0–2.5%` naive · 1,500+ failure scenarios · 0 invariant violations |
| **[KubePulse](https://github.com/kritibehl/KubePulse)** | deployment regressions that health probes miss | Go · Terraform · K8s · Prometheus | p95 drifted `333%` with probes still green · blocked AMD MI300X rollout at `+608%` latency regression |
| **[DetTrace++](https://github.com/kritibehl/dettrace)** | the exact event where a system became incorrect | Python · Go · C++17 · Swift | UART IRQ · timer missed-tick · GPIO race · retry storms · cascading failures |
| **[FairEval-Suite](https://github.com/kritibehl/FairEval-Suite)** | AI models that regress under real serving load | Python · Gemini API | blocked candidate with `47.1%` p95 regression despite score parity · live on HuggingFace |
| **[AutoOps-Insight](https://github.com/kritibehl/AutoOps-Insight)** | recurring CI failures before they hit production | Python · PostgreSQL · React | pattern-grouped failures · confidence-scored release decisions |
| **[AccelSim-Lite](https://github.com/kritibehl/accelsim-lite)** | throughput and latency bottleneck transitions | C++ · Python | `87%` throughput gain · `39%` latency reduction · bottleneck shift proven via what-if |

---

## `$ cat oss.log`

```bash
[2026-03-02]  PR #2200  MERGED  Temporal Go SDK  fix: goroutine leak in test runtime shutdown
[2026-03-12]  PR #2212  MERGED  Temporal Go SDK  fix: propagation headers missing in mock matcher
[2026-04-20]  PR #2298  MERGED  Temporal Go SDK  fix: async future reports ready while callers blocked
[in review ]  PR #26051 REVIEW  Azure Go SDK     fix: azcore retry policy, errors.Join
[in review ]  PR #26106 REVIEW  Azure Go SDK     feat: W3C Trace Context (traceparent/tracestate)
```

---

## `$ ./identity.sh`

```
> I build systems that reason about when other systems are wrong.

  Faultline   ── proves correctness when distributed workers fail
  KubePulse   ── catches regressions that health probes never see
  DetTrace++  ── isolates the exact event where behavior became wrong
  FairEval    ── blocks AI releases that regress under real serving load
  AutoOps     ── detects CI failures before they become production outages

  M.S. Computer & Information Science · University of Florida · GPA 3.8 ▌
```

---

## `$ cat skills.conf`

```ini
[languages]
primary  = Go
other    = Python, Java, C++, SQL, Bash, JavaScript

[backend]
apis     = REST, Node.js, Express, PostgreSQL
patterns = fault injection, fencing tokens, distributed job execution

[infrastructure]
cloud    = AWS (EKS, ECS, VPC)
tools    = Kubernetes, Terraform, Docker, Git, GitHub Actions

[observability]
stack    = Prometheus, Grafana, Datadog
practice = SLO enforcement, incident response, replay-based debugging

[focus]
core     = correctness under failure, resilience validation,
           deterministic replay, firmware-style trace analysis
```

---

## `$ ping kriti`

```
email      kriti0608@gmail.com
linkedin   linkedin.com/in/kriti-behl
portfolio  kriti-portfolio-six.vercel.app
location   Gainesville FL → open to full relocation
status     actively searching · SRE / Backend / Infra · OPT/STEM OPT
```

---

<sub>Seeking SRE · Backend · Infrastructure · Platform roles · M.S. completed Dec 2025</sub>
