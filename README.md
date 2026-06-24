# BlueLotus V3 — Documentation

**Governed investment intelligence — frozen public release v3.0.0**

[![Download](https://img.shields.io/badge/Download-v3.0.0-4fc3f7?style=for-the-badge)](DOWNLOAD.md)
[![Engine](https://img.shields.io/badge/Code-bluelotus--engine-181717?style=for-the-badge&logo=github)](https://github.com/sohweekian/bluelotus-engine)
[![Research](https://img.shields.io/badge/Theses-bluelotus--research-533483?style=for-the-badge&logo=github)](https://github.com/sohweekian/bluelotus-research)
[![Dashboard](https://img.shields.io/badge/Dashboard-LIVE-4ade80?style=for-the-badge)](https://sohweekian.github.io/bluelotus)

---

## Start here

| I want to… | Read this |
|------------|-----------|
| **Download the software** | [DOWNLOAD.md](DOWNLOAD.md) |
| **Understand what it does** | [WHAT_IS_BLUELOTUS.md](WHAT_IS_BLUELOTUS.md) |
| **Know if it's for me** | [WHO_IS_IT_FOR.md](WHO_IS_IT_FOR.md) |
| **See the architecture** | [ARCHITECTURE.md](ARCHITECTURE.md) |
| **Read the full story** | [The Clerk Who Never Lies](#the-story) below |
| **Read academic theses** | [bluelotus-research](https://github.com/sohweekian/bluelotus-research) |

---

## In one sentence

BlueLotus is a **family-office intelligence OS** that maps contradictions and governs truth for a CIO who executes manually — released as **frozen research infrastructure** (not a trading product).

---

## Quick download

```bash
pip install https://github.com/sohweekian/bluelotus-engine/releases/download/v3.0.0/bluelotus_engine-3.0.0-py3-none-any.whl
python -m bluelotus_engine.cli init-workspace
python -m bluelotus_engine.cli pipeline --once --dry-run
```

---

## Release status

| Item | Status |
|------|--------|
| Engine software | **Frozen at v3.0.0** — no further updates planned |
| Documentation | This repository — stable reference |
| Theses | [bluelotus-research](https://github.com/sohweekian/bluelotus-research) — may receive new papers |
| Private production stack | **Proprietary** — not published |

See [PUBLIC_RELEASE_NOTICE.md](https://github.com/sohweekian/bluelotus-research/blob/main/PUBLIC_RELEASE_NOTICE.md) for the public vs proprietary boundary.

---

## The story

*The Clerk Who Never Lies* — why we removed LLM agents from production and open-sourced the deterministic engine.

<details>
<summary><strong>Read the full narrative</strong></summary>

### Act I — The seduction of agents

June 2026. Nine local Qwen agents. A 65-step pipeline. Every 39 minutes, a council of specialists would read the tape and write briefings.

Then the CIO asked: *"Did you read all of it?"*

Frontier LLMs skimmed multi-megabyte packages, hallucinated missing sections, and could not distinguish stale from fresh news. **Temporal blindness** — not a prompt bug, an architectural ceiling.

### Act II — The doctrine

Seven written doctrines: no LLM orders, manual execution, no broker write access, governance before publish, append-only audit.

The job is narrower:

> Map what the data says. Map what contradicts. Map what still needs human eyes. **Stop.**

### Act III — Zone A

**Deterministic Chief Clerk** — pure Python, no GPU inference. Same inputs → same outputs → auditable artifacts.

### Act IV — What we gave the world

Sanitized **`bluelotus-engine` v3.0.0**: governance, clerk, NITE-PEI, SLICDO. No publish, no telegram, no broker connectors.

**The CIO decides.**

</details>

---

## Authorship

**Soh Wee Kian** · CIO · BlueLotus Fund Singapore

MIT license on public engine code. Research and documentation only — not financial advice.

🌸 *Built with precision · Governed by doctrine*
