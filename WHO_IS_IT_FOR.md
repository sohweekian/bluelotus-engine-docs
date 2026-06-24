# Who Is BlueLotus For?

## This software is for you if…

### Researchers & academics
You study **governed financial AI**, Bayesian inference in capital markets, **game theory & Nash equilibrium in geopolitical risk**, institutional memory systems, or the failure modes of LLMs in live intelligence work.

- Download the engine and run it on **synthetic demo data**
- Read the theses in [bluelotus-research](https://github.com/sohweekian/bluelotus-research) — including the [BGTM PhD thesis](https://github.com/sohweekian/bluelotus-research/blob/main/BGTM_V1_PhD_Thesis_GameTheory_NashEquilibrium_2026.md)
- Cite the deterministic transition, NITE-PEI framework, and BGTM-V1 tool pack

### Quantitative developers & open-source builders
You want a **reference implementation** of:

- Governance gates before publish
- Contradiction registers with priority levels
- Bayesian thesis updating from news events
- **N-player Nash / QRE solvers** with Geo-LR bridge (BGTM-V1)
- Learning spines with promotion ledgers (not blind auto-tuning)

You will bring your own `dataset_raw.json`. The public package does not ship broker connectors.

### Family-office & CIO practitioners (study only)
You run or advise a small mandate and want to see how a **single-CIO intelligence OS** can be architected:

- Manual execution doctrine
- Broker-reported P/L as authoritative truth
- Eight-lens situation maps
- Kill conditions and CKRI zones

This is a **research snapshot**, not a supported commercial product.

### Students of financial systems design
You want a case study in how a real system evolved: dashboard → intelligence OS → agent experiment → **deterministic clerk** — with doctrines written from failures, not slide decks.

---

## This software is *not* for you if…

| You want… | BlueLotus public edition is not… |
|-----------|----------------------------------|
| Auto-trading or order routing | Orders are disabled by design |
| Investment advice or signals | Research-only; no recommendations |
| A maintained SaaS product | Frozen at v3.0.0 |
| Bloomberg replacement with live feeds | No live fetchers in public package |
| An LLM agent trading council | Agents quarantined; clerk is deterministic |
| Production support or SLAs | Community release; no vendor |

---

## Audience map

```text
                    ┌─────────────────────────────────────┐
                    │         PUBLIC (frozen v3.0.0)       │
                    ├─────────────────────────────────────┤
  Researchers  ────►│  bluelotus-engine (download)        │
  Readers      ────►│  bluelotus-engine-docs (story)      │
  Academics    ────►│  bluelotus-research (theses)        │
  Visitors     ────►│  Live dashboard (publish surface)   │
                    └─────────────────────────────────────┘
                                      │
                    ┌─────────────────▼───────────────────┐
                    │      PRIVATE (proprietary, not public) │
                    │  Production pipeline · work orders     │
                    │  Broker truth · live 39-min loop       │
                    │  CIO operating configuration           │
                    └─────────────────────────────────────┘
```

---

## How to get started (by role)

| Role | Start here |
|------|------------|
| **I want to download and run it** | [DOWNLOAD.md](DOWNLOAD.md) |
| **I want to understand what it is** | [WHAT_IS_BLUELOTUS.md](WHAT_IS_BLUELOTUS.md) |
| **I want the story** | [README.md](README.md) |
| **I want the math & theses** | [bluelotus-research](https://github.com/sohweekian/bluelotus-research) |
| **I want game theory / Nash** | [BGTM.md](BGTM.md) |
| **I want the live demo dashboard** | [sohweekian.github.io/bluelotus](https://sohweekian.github.io/bluelotus) |

---

## Authorship & license

**Principal architect:** Soh Wee Kian (CIO), BlueLotus Fund Singapore  
**Public engine license:** MIT (see [bluelotus-engine/LICENSE](https://github.com/sohweekian/bluelotus-engine/blob/main/LICENSE))  
**Disclaimer:** Research and documentation only. Not financial advice.

The private production system and internal work orders remain proprietary. The public release is a **frozen research contribution** — use it to learn, extend, and cite; not to expect ongoing maintenance.
