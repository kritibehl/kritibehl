<div align="center">

# Hi, I'm Kriti 👋

### Software Engineer | Backend · Distributed Systems · Reliability

**M.S. Computer Science, University of Florida** · Dec 2025 · GPA 3.8
📍 Chicago, IL · Open to relocation, US-wide

[![Temporal Go SDK](https://img.shields.io/badge/Temporal_Go_SDK-7_merged_PRs-3fb950?style=for-the-badge&logo=go&logoColor=white)](https://github.com/temporalio/sdk-go/pulls?q=author%3Akritibehl)
[![Azure SDK](https://img.shields.io/badge/Azure_Go_SDK-1_merged_1_in_review-d29922?style=for-the-badge&logo=microsoftazure&logoColor=white)](https://github.com/Azure/azure-sdk-for-go/pulls?q=author%3Akritibehl)
[![University of Florida](https://img.shields.io/badge/M.S._Computer_Science-UF-58a6ff?style=for-the-badge)](https://www.cise.ufl.edu/)

*I build backend and infrastructure systems that stay correct when failures, concurrency, and regressions make behavior hard to reason about.*

<br>

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

</div>

---

### ⚡ TL;DR

```
if you_read_one_thing:
    → 7 PRs merged into Temporal's production Go SDK by their maintainers.
    → Not a tutorial project. Not a clone. Code real engineers use, that I fixed.
```

<div align="center">
<table><tr>
<td align="center"><b>7</b><br><sub>merged Temporal PRs</sub></td>
<td align="center"><b>1,500+</b><br><sub>failure scenarios · Faultline</sub></td>
<td align="center"><b>0.93</b><br><sub>root-cause confidence · DetTrace</sub></td>
<td align="center"><b>+333%</b><br><sub>p95 spike caught · KubePulse</sub></td>
</tr></table>
</div>

---

## 📊 GitHub Activity

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=kritibehl&show_icons=true&theme=github_dark&hide_border=true&count_private=true" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=kritibehl&layout=compact&theme=github_dark&hide_border=true" />

<img src="https://github-readme-streak-stats.herokuapp.com/?user=kritibehl&theme=github-dark-blue&hide_border=true" />

</div>



---

## 🔓 Open Source

I don't just build my own systems — I've shipped fixes into ones other engineers depend on.

<table>
<tr><td width="50%" valign="top">

**🌀 Temporal Go SDK — `7 merged PRs`**

- 🐛 Fixed goroutine leak in test runtime shutdown — [#2200](https://github.com/temporalio/sdk-go/pull/2200)
- 🔧 Fixed `OnWorkflow` mock context propagation — [#2212](https://github.com/temporalio/sdk-go/pull/2212)
- ⚙️ Task poller-type instrumentation — [#2248](https://github.com/temporalio/sdk-go/pull/2248)
- 🔀 Fixed async future-chaining completion bug — [#2298](https://github.com/temporalio/sdk-go/pull/2298)
- 📝 Documented rate-limit timeout caveat — [#2367](https://github.com/temporalio/sdk-go/pull/2367)
- 💾 External-storage support for query results — [#2459](https://github.com/temporalio/sdk-go/pull/2459)
- 🩹 Fixed legacy query-task failure reporting — [#2639](https://github.com/temporalio/sdk-go/pull/2639)

</td><td width="50%" valign="top">

**☁️ Azure SDK for Go**

- ✅ **Merged** — `errors.Join` fix so a failed retry doesn't silently swallow a failed body-close — [#26051](https://github.com/Azure/azure-sdk-for-go/pull/26051)
- 🔍 **In review** — W3C Trace Context support (traceparent/tracestate) — [#26106](https://github.com/Azure/azure-sdk-for-go/pull/26106)

</td></tr>
</table>

---

## 🛠️ Selected Projects

> Four systems. One thread: **what happens when things fail, and how do you prove it stayed correct.**

### 🧱 [Faultline](https://github.com/kritibehl/faultline) — distributed job execution correctness

**`0.0%` duplicate commits across `1,500+` injected failures — vs. `12` on a naive queue under the same load.**

<details>
<summary>How it works ↓</summary>
<br>

Lease-based job systems have a hole: lease expiry stops the *next* worker from starting — it doesn't stop the *old* worker from writing late after it recovers from a crash. That stale write is what corrupts ledgers and causes double-charges.

Faultline closes the hole at the **database boundary**, not in app logic — a `UNIQUE(job_id, fencing_token)` constraint in Postgres means a recovered worker holding a stale token gets rejected by the DB itself. Each claim increments a token; a late commit from an old token is rejected because it's no longer the newest one, full stop.

Ships with a reconciler that repairs incomplete jobs, a Go inspector API for live lease-risk state, and Prometheus/OTEL instrumentation for stale-rejection rate and claim latency.

</details>

`Python (primary)` `Go (inspector API)` `PostgreSQL` `Docker` `Prometheus` `OpenTelemetry`

---

### 🌐 [KubePulse](https://github.com/kritibehl/KubePulse) — release-safety validation across the stack

**Caught a release where p95 latency spiked `+333%` while every Kubernetes readiness probe stayed green.**

<details>
<summary>How it works ↓</summary>
<br>

Readiness probes check whether a container is *alive* — not whether the release is *safe*. KubePulse runs a 4-layer gate (health signals → network validation → SLO/error-budget check → probe-integrity divergence) and issues an explicit ship/block decision.

Underneath the Kubernetes layer is a real networking lab: a two-AS eBGP topology (FRRouting, Linux network namespaces) with measured `251ms` median / `270ms` p95 data-plane recovery across 10 fault-injection runs — plus a Layer-2 lab (VLAN trunking, 802.1Q, router-on-a-stick) where a deliberately broken trunk isolated 100% packet loss to a single VLAN, diagnosed and rolled back with packet-capture evidence.

</details>

`Python` `FastAPI` `Kubernetes` `Terraform` `FRRouting` `Prometheus` `Docker Compose`

---

### 🔬 [DetTrace](https://github.com/kritibehl/dettrace) — first-failure isolation via deterministic replay

**Finds where execution *first* diverged — not just where it eventually broke. `0.93` root-cause confidence across `10,000+` validations.**

<details>
<summary>How it works ↓</summary>
<br>

Debugging distributed failures is asymmetric: failures are easy to *see*, hard to *locate* — logs record state changes after they happen, and the event that actually caused the failure often isn't logged at all.

DetTrace generates an expected deterministic trace, replays the divergent execution, and binary-searches to isolate the first divergence index. Validated across 20 I/O transport scenarios (SPI, I2C, UART, GPIO races, distributed retry storms) with 47 GoogleTest cases passing clean under AddressSanitizer and UndefinedBehaviorSanitizer.

Honest about its limits — the README documents a ~7% false-positive rate and states plainly that firmware scenarios are trace simulations, not kernel-level implementations. That's the kind of thing worth saying out loud in an interview, not hiding.

</details>

`C++17` `CMake` `GoogleTest` `Swift` `Python (FastAPI)`

---

### 🤖 [AgentGrid](https://github.com/kritibehl/agentgrid) — making AI agent failure modes observable

**Gated a release to `HOLD` instead of shipping it — because averaging hides exactly the failure you need to see.**

<details>
<summary>How it works ↓</summary>
<br>

Production GenAI systems fail quietly: retrieval misses the right doc, a tool call returns a stale result, an answer generates without grounding — and one aggregate pass-rate number hides all of it.

AgentGrid instruments every stage (triage → retrieval → tool execution → generation → eval gate → optional human review) with per-stage metrics, and gates releases on retrieval hit rate, tool success rate, p95 latency, and drift. Current state: 80% retrieval hit rate, 80% tool success rate, 880ms p95 — held, not shipped, with the hold reason surfaced explicitly. 57 tests passing.

</details>

`Python` `FastAPI` `React/TypeScript` `Redis` `Prometheus`

<details>
<summary><b>🗂️ More projects</b></summary>
<br>

- **[FairEval](https://github.com/kritibehl/FairEval-Suite)** — blocks AI releases that regress under real serving load
- **[AccelSim-Lite](https://github.com/kritibehl/accelsim-lite)** — names throughput/latency bottlenecks and gates the regression
- **[AutoOps-Insight](https://github.com/kritibehl/AutoOps-Insight)** — detects CI/CD failures before they reach production
- **[Enterprise Process Lab](https://github.com/kritibehl/enterprise-process-lab)** — validates ERP integrations and controls compliance

</details>

---

## 💼 Experience

**Meta × MLH — Production Engineering Fellow** `June – September 2026`
- Deployed and operated a Linux-hosted Flask service on a cloud VPS — SSH, DuckDNS routing, Python virtualenv, tmux-based process persistence
- Automated redeployment with a Bash script covering 6+ manual steps: GitHub sync, repo reset, dependency install, stale-process cleanup, service restart
- Built Bash/Python automation for API parsing, regex matching, and Apache log analysis across a 237MB dataset — extracted 2.9M+ unique source IPs and HTTP status-code distributions

---

## 🧰 Technical Skills

| | |
|---|---|
| **Languages** | Python · Go · C++ · Java · SQL · Bash · JavaScript |
| **Backend** | REST APIs · FastAPI · PostgreSQL · distributed job execution · concurrency · idempotency |
| **Infrastructure** | Kubernetes · Docker · Terraform · AWS · GitHub Actions |
| **Systems** | Linux · TCP/IP · distributed systems · fault tolerance · transactional correctness |
| **Observability** | Prometheus · Grafana · OpenTelemetry · Datadog |

---

<div align="center">

### 📫 Let's talk

[![Email](https://img.shields.io/badge/Email-kriti0608%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:kriti0608@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-kriti--behl-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kriti-behl/)
[![Portfolio](https://img.shields.io/badge/Portfolio-kriti--portfolio--six.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://kriti-portfolio-six.vercel.app)

**Open to Software Engineering opportunities in the U.S. · Open to relocation**

</div>
