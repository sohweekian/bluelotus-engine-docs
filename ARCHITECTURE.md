# Architecture at a Glance

```text
                    ┌─────────────────────────────────────┐
                    │         YOUR DATA LAYER             │
                    │  dataset_raw.json (BYO or demo)     │
                    └─────────────────┬───────────────────┘
                                      │
                    ┌─────────────────▼───────────────────┐
                    │      GOVERNANCE LAYER (law)         │
                    │  contract validation · gate ·       │
                    │  scenario overlay · regression      │
                    └─────────────────┬───────────────────┘
                                      │
                    ┌─────────────────▼───────────────────┐
                    │    REPORT LAYER (deterministic)     │
                    │  TXT · XLSX · DOCX · publish gate   │
                    └─────────────────┬───────────────────┘
                                      │
                    ┌─────────────────▼───────────────────┐
                    │   ZONE A — DETERMINISTIC CLERK      │
                    │  contradiction map · no LLM         │
                    │  operator verdicts · portfolio math │
                    └─────────────────┬───────────────────┘
                                      │
              ┌───────────────────────┼───────────────────────┐
              │                       │                       │
┌─────────────▼─────────────┐ ┌───────▼────────┐ ┌───────────▼──────────────┐
│      NITE-PEI             │ │   BGTM-V1      │ │      SLICDO v2           │
│  Bayesian thesis update   │ │ Nash · QRE · CE│ │  claims · replay ·       │
│  CKRI · Kelly advisory    │ │ Geo-LR bridge  │ │  CIO-gated promotions    │
└─────────────▲─────────────┘ └───────┬────────┘ └──────────────────────────┘
              │                       │
              │    Geo-LR blend       │
              └───────────────────────┘
                    (α = min(1, n/30))
```

## BGTM-V1 — geopolitical overlay

The **Game Theory & Nash Equilibrium Tool Pack** sits beside NITE-PEI, not instead of it:

| Step | Component |
|------|-----------|
| 1 | Expert-initialised payoff tensors (`games/*.py`) |
| 2 | Nash multiplicity → Correlated Equilibrium envelope |
| 3 | QRE softening (bounded rationality) |
| 4 | Outcome probabilities → **Geo-LR** (clamped [0.1, 10.0]) |
| 5 | Blend with static NITE-PEI LRs → Bayesian posterior |

Full detail: [BGTM.md](BGTM.md)

---

## What we deliberately removed from the public package

| Component | Why excluded |
|-----------|----------------|
| `bluelotus_publisher.py` | GitHub Pages deploy — private ops |
| Telegram push | Operator notifications — private |
| `run_v3_grand_cycle` | LLM agent council — quarantined legacy |
| Live broker fetchers | API keys · private mandate |

## What stayed

The **cognition kernel**: governed math, auditable artifacts, reproducible clerk cycles — **including BGTM-V1** (`geo_game_theory/`).

That is the part worth studying.
