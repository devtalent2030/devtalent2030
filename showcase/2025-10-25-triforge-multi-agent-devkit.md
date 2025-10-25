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
