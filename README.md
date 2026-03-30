# Kriti Behl

Software engineer focused on backend infrastructure, distributed systems and reliability.

Built production backend systems at Thales Group, contributed merged fixes to the Temporal Go SDK, and developed systems around crash safety, resilience validation, incident analysis and release safety.

---

## What I Build

I build systems that do more than run — they prove correctness, surface failure modes, and generate evidence teams can trust before production.

My work sits at the intersection of distributed systems reliability, Kubernetes resilience, incident forensics, and ML evaluation infrastructure, with an emphasis on formal correctness guarantees, evidence-backed validation and production-minded operator tooling.

---

## Featured Projects

| Project | What It Does |
|---|---|
| [**Faultline**](https://github.com/kritibehl/faultline) | Crash-safe distributed job execution with fencing tokens and lease-based recovery, validated across 1,500 deterministic race reproductions |
| [**FairEval-Suite**](https://github.com/kritibehl/FairEval-Suite) | CI-integrated regression gating for GenAI systems that detects silent behavior drift across model, prompt, retrieval, and inference changes before deployment |
| [**AutoOps-Insight**](https://github.com/kritibehl/AutoOps-Insight) | Operator-facing incident triage that classifies failure logs, fingerprints recurring signatures, previews rule-change impact, and generates release-risk reports |
| [**DetTrace**](https://github.com/kritibehl/dettrace) | Distributed incident forensics that reconstructs cross-service failure timelines, identifies the first failing hop, infers blast radius, and semantically diffs regressions |
| [**KubePulse**](https://github.com/kritibehl/KubePulse) | Kubernetes resilience validation that measures real recovery behavior, catches readiness false positives, and produces scorecarded reports before rollout |

---

## Open Source and Writing

I write about the systems problems behind these projects — the failure modes that motivated them, the design decisions that matter and the guarantees that separate production systems from demos.

- Temporal Go SDK: 2 merged PRs and 1 open PR across workflow test reliability and context propagation behavior
- Azure Go SDK: 2 PRs under review in retry/error handling and trace context propagation

Selected writing:
- [How I Built a Distributed Job Queue That Stays Correct Under Crashes, Races, and Network Faults](https://medium.com/@kriti0608/how-i-built-a-distributed-job-queue-that-stays-correct-under-crashes-races-and-network-faults-48bc50eec723)
- [Detecting Silent Regressions in GenAI Systems at Scale](https://medium.com/@kriti0608/detecting-silent-regressions-in-genai-systems-at-scale-039ec03db1e4)
- [I Thought I Built Observability. Then an Incident Proved I Didn’t.](https://medium.com/@kriti0608/i-thought-i-built-observability-then-an-incident-proved-i-didnt-9b749e0d4ff3)
  
---

## What I Care About

- Correctness that holds under real failure conditions, not just happy paths
- Validation infrastructure that gives teams evidence, not just confidence
- Operator tooling that makes repeated incidents cheaper to triage and safer to fix
- Building systems where "it passed" means something specific and reproducible

---

## Connect

[LinkedIn](https://linkedin.com/in/kritibehl) · [GitHub](https://github.com/kritibehl) · [Medium](https://medium.com/@kriti0608) · kriti0608@gmail.com

---

*If you work on distributed systems, reliability, platform engineering, or AI infrastructure, start with Faultline or FairEval.*
