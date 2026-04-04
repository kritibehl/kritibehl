# Kriti Behl

I build backend and distributed systems that stay correct under failure and make failures easier to diagnose.

Built production backend systems at Thales Group, contributed merged fixes to the Temporal Go SDK, and built systems with proof like 0 duplicate commits across 1,500 race reproductions and probe-healthy / system-unsafe detection under failure.

**If you're hiring for backend, infrastructure, reliability, or production engineering roles, start here:**
- [Faultline](https://github.com/kritibehl/faultline) — crash-safe job execution, fencing tokens, race validation
- [KubePulse](https://github.com/kritibehl/KubePulse) — resilience validation, recovery measurement, unsafe-state detection
- [Temporal Go SDK PRs](https://github.com/temporalio/sdk-go/pulls?q=is%3Apr+author%3Akritibehl) — merged OSS fixes in workflow/runtime behavior
---

## What these projects prove

| Project | What it proves |
|---|---|
| [Faultline](https://github.com/kritibehl/faultline) | I can design execution systems that preserve correctness under crashes, lease expiry, and race conditions |
| [KubePulse](https://github.com/kritibehl/KubePulse) | I can validate real recovery behavior, not just surface-level health signals |
| [AutoOps-Insight](https://github.com/kritibehl/AutoOps-Insight) | I can turn noisy operational failures into structured incident signals and operator-facing decisions |
| [DetTrace](https://github.com/kritibehl/dettrace) | I can isolate first-failure points and reconstruct divergent system behavior deterministically |

---
## Open Source Contributions

- Temporal Go SDK: 2 merged PRs and 1 open PR across workflow test reliability and context propagation behavior
- Azure Go SDK: 2 PRs under review in retry/error handling and trace context propagation

## Selected Writing

- [How I Built a Distributed Job Queue That Stays Correct Under Crashes, Races, and Network Faults](https://medium.com/@kriti0608/how-i-built-a-distributed-job-queue-that-stays-correct-under-crashes-races-and-network-faults-48bc50eec723)
-  [I Thought I Built Observability. Then an Incident Proved I Didn’t.](https://medium.com/@kriti0608/i-thought-i-built-observability-then-an-incident-proved-i-didnt-9b749e0d4ff3)
- [Detecting Silent Regressions in GenAI Systems at Scale](https://medium.com/@kriti0608/detecting-silent-regressions-in-genai-systems-at-scale-039ec03db1e4)

---
## Why this profile is different

Most entry-level profiles show projects that work.

This profile is built around systems that are tested under:
- crashes
- retries
- lease expiry
- stale writes
- degraded dependencies
- misleading health signals

The goal is not just building software that runs. It is building software that stays correct, exposes unsafe behavior, and leaves behind enough evidence to debug failures precisely.
---

## Focus Areas

Backend infrastructure · Distributed systems · Reliability engineering · Incident analysis · Developer tooling

---
## Connect

[LinkedIn](https://linkedin.com/in/kritibehl) · [GitHub](https://github.com/kritibehl) · [Medium](https://medium.com/@kriti0608) · kriti0608@gmail.com

---

*If you're hiring for backend, infrastructure, reliability or production engineering roles, start with Faultline and KubePulse.*
\n\n
## What I build

I build systems that:

1. execute correctly under failure  
   **Faultline** — crash-safe execution, replayable races, and correctness under partial failure

2. detect unsafe system behavior  
   **KubePulse** — resilience validation, timing-aware diagnostics, and unsafe-state detection under faults

3. diagnose failures precisely  
   **DetTrace** — deterministic replay, first-divergence isolation, and replay-based debugging for concurrent, distributed, and control-loop systems
\n
