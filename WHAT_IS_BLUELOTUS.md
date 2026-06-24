# What Is BlueLotus?

**BlueLotus V3** is a governed investment intelligence system built for a single Chief Investment Officer running a private family office. It is **not** a trading bot, robo-adviser, or signal service.

It is a **research and contradiction-mapping engine** that:

1. Organizes market, portfolio, thesis, and scenario data
2. Runs **deterministic governance gates** before anything is treated as truth
3. Produces structured reports (TXT, XLSX, DOCX)
4. Maps **contradictions** — where data, operators, and portfolio math disagree
5. Updates **Bayesian thesis probabilities** from news events (NITE-PEI)
6. Runs **N-player Nash / QRE game theory** on geopolitical scenarios (BGTM-V1) and feeds **Geo-LR** into thesis updating
7. Maintains an **institutional learning spine** (SLICDO) with CIO-gated promotions

> **The pipeline calculates. The clerk maps contradictions. The CIO decides.**

---

## What it does *not* do

| Never | Doctrine |
|-------|----------|
| Place or route orders | `CIO_ONLY_MANUAL` |
| Generate trade instructions | No LLM order generation |
| Write to a broker | Read-only extraction only |
| Replace human judgment | Research and documentation only |

Outputs may be incomplete, stale, or wrong. Every decision requires independent human verification.

---

## The public release (frozen at v3.0.0)

In June 2026, a **sanitized research edition** was released as a contribution to the research community:

| Artifact | Location |
|----------|----------|
| **Downloadable engine** | [bluelotus-engine v3.0.0](https://github.com/sohweekian/bluelotus-engine/releases/tag/v3.0.0) |
| **Documentation & story** | [bluelotus-engine-docs](https://github.com/sohweekian/bluelotus-engine-docs) |
| **Theses & doctrines** | [bluelotus-research](https://github.com/sohweekian/bluelotus-research) |
| **Live dashboard** | [sohweekian.github.io/bluelotus](https://sohweekian.github.io/bluelotus) |

**Status:** Engine frozen at **v3.0.0**. No further software updates are planned. Thesis and doctrine papers may continue to be uploaded to `bluelotus-research`.

**Proprietary:** The private production stack, work orders, broker integrations, and live operating configuration remain the property of the author and are **not** published.

---

## Core modules (public engine)

| Module | Function |
|--------|----------|
| **Governance gate** | Fail-closed approval before reports are trusted |
| **Deterministic clerk (Zone A)** | Contradiction map from math and rules — no LLM agents |
| **NITE-PEI** | Bayesian thesis updating, CKRI kill-risk index, Kelly sizing advisory |
| **BGTM-V1** | Nash Equilibrium · QRE · Correlated Equilibrium · Geo-LR bridge into NITE-PEI |
| **SLICDO** | Institutional claims, resolutions, replay, promotion proposals |
| **Report generator** | Structured CIO intelligence package (TXT / XLSX / DOCX) |

**Excluded from public edition:** GitHub publish, Telegram push, LLM agent council, live broker fetchers, private portfolio data.

**Deep dive — game theory:** [BGTM.md](BGTM.md) · [PhD thesis](https://github.com/sohweekian/bluelotus-research/blob/main/BGTM_V1_PhD_Thesis_GameTheory_NashEquilibrium_2026.md)

---

## Why deterministic instead of agents?

After live field evaluation (June 2026), LLM agents were removed from the production path:

- **Temporal blindness** — stale and fresh news weighted equally
- **Partial read + hallucination** — skimmed packages, invented missing sections
- **Non-reproducibility** — same inputs did not yield same truth

Production now runs a **deterministic Chief Clerk** — pure Python, auditable, reproducible.

Full story: [The Clerk Who Never Lies](README.md) · [DETERMINISTIC_TRANSITION.md](https://github.com/sohweekian/bluelotus-research/blob/main/DETERMINISTIC_TRANSITION.md)

---

## One-line summary

**BlueLotus is governed financial cognition for a CIO who executes manually — with a formal Nash Equilibrium tool pack for geopolitical overlays — open-sourced as research infrastructure, not as a product.**
