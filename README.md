<!-- Profile banner -->
<h1 align="center"> Talent Nyota — Cloud & Platform Engineering • Cloud Security</h1>
<p align="center">
  Toronto • Hybrid/Remote
  <br/>
  <a href="mailto:trnyota@gmail.com">Email</a> ·
  <a href="https://www.linkedin.com/in/talentnyota/">LinkedIn</a> ·
  <a href="https://github.com/devtalent2030">GitHub</a>
</p>

<p align="center">
  <img alt="AWS" src="https://img.shields.io/badge/AWS-232F3E?logo=amazonaws&logoColor=white">
  <img alt="Azure" src="https://img.shields.io/badge/Azure-0078D4?logo=microsoftazure&logoColor=white">
  <img alt="GCP" src="https://img.shields.io/badge/GCP-1a73e8?logo=googlecloud&logoColor=white">
  <img alt="Terraform" src="https://img.shields.io/badge/Terraform-7B42BC?logo=terraform&logoColor=white">
  <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white">
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white">
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white">
</p>

---

### What I do
I architect cloud platforms that **scale securely**. From VPCs to SOCs—automated, instrumented, production-ready.

**Stack:** `AWS · Azure · GCP · Terraform · CDK · Docker · Python ·`

---

## Featured builds

**SecuriScan** — OWASP scanners → executive-ready reports (Next.js/TS). Findings mapped to action, not noise.  
[![SecuriScan](https://github-readme-stats.vercel.app/api/pin/?username=devtalent2030&repo=SecuriScan)](https://github.com/devtalent2030/SecuriScan)

**Cloud Security Visibility** — Multi-cloud SOC patterns (Terraform) across **AWS/Azure/GCP**: central logs, anomaly alerts, asset registry.  
[![Cloud Security Visibility](https://github-readme-stats.vercel.app/api/pin/?username=devtalent2030&repo=cloud-security-visibility)](https://github.com/devtalent2030/cloud-security-visibility)

**Enterprise Accounts & Users** — **Foundations/IAM** at scale: org/account/subscription structure, region guardrails, least-privilege onboarding.  
[![Enterprise Accounts & Users](https://github-readme-stats.vercel.app/api/pin/?username=devtalent2030&repo=cloud-enterprise-accounts-and-users)](https://github.com/devtalent2030/cloud-enterprise-accounts-and-users)

**TriForge** — 3-agent LLM orchestrator (offline stub + Claude/OpenAI) that **plans → writes → tests** with CI.  
[![TriForge](https://github-readme-stats.vercel.app/api/pin/?username=devtalent2030&repo=triforge)](https://github.com/devtalent2030/triforge)

---

## Learning Showcase (auto-rotates)
<!-- SHOWCASE_START -->

## TriForge — Multi‑Agent DevKit (3 Agents in Parallel)

**What it is**
TriForge is a Python toolkit that runs **three LLM agents in parallel** (Architect, Coder, Reviewer), merges their outputs, and ships runnable artifacts with tests and CI.

**Why it matters**

* **Speed:** parallel agents cut design → code → tests to minutes.
* **Quality:** baked‑in test scaffolding + linting; repeatable runs via CLI.
* **Portable:** provider‑agnostic (Anthropic, OpenAI) with an **offline stub** for demos.

**How it works**

```
Spec (YAML) → Orchestrator → [OpenAI | Anthropic | Stub] → Code/Tests/Docs → Merged Artifacts
```

**Quick run**

```bash
# clone + venv
git clone YOUR_FORK_URL triforge && cd triforge
python3 -m venv .venv && source .venv/bin/activate
pip install -U pip && pip install -e .[dev]

# offline demo first
export LLM_PROVIDER=stub

# run a sample specification
python -m triforge run --spec docs/samples/string_calculator.yaml

# verify
pytest -q && ruff check .
```

**Provider switch (optional)**

```bash
# choose a live provider when ready
export LLM_PROVIDER=anthropic   # or: openai
# export ANTHROPIC_API_KEY=...
# export OPENAI_API_KEY=...
```

**What you’ll see**

* A concise **design** from the Architect agent
* Generated **code + tests** from the Coder/Reviewer
* **CI‑friendly** artifacts ready to drop into a repo

**Receipts**

* CLI, providers, tests, demo spec under `docs/samples/string_calculator.yaml`
* README demo + architecture diagram in the TriForge repo

<!-- SHOWCASE_END -->

---

## Proof

| Outcome | How | Receipts |
|---|---|---|
| **TTFB ↓ ~60%** (HA Web) | CloudFront CachingOptimized + ALB health | `cloud-security-visibility/AWS/logging/` · `docs/ha-ttfb.png` |
| **Live Sentinel dashboards** | Connectors + workbooks (offenders/anomalies) | `cloud-security-visibility/Azure/soc/` · `docs/sentinel-dash.png` |
| **Auto triage on GCP** | SCC → Pub/Sub → Cloud Functions with labels | `cloud-security-visibility/GCP/soc/` · `GCP/soc/main.py` |
| **Safe-by-default foundations** | Region policies + least-priv IAM | `cloud-enterprise-accounts-and-users/*/region-locking/` |

---

## What I own end-to-end

- **Platform engineering:** VPC/networking, IAM/SSO, secrets, containers, observability.  
- **Security visibility:** centralized logs, detections, dashboards, and response hooks.  
- **Foundations:** org/account/subscription hierarchy, policies, break-glass.  
- **App hardening:** OWASP scans → prioritized fix paths with clear owners.

---

### Contact/Hire Me!
Need a cloud platform that scales and secures? I bring initiative, code, and results 
**Email:** `devtalent208@gmail.com` · **Toronto** · **Hybrid/Remote**

<sup>Last updated: Fri Nov 28 18:33:35 UTC 2025</sup>
