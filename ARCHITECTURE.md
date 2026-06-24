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
              ┌───────────────────────┴───────────────────────┐
              │                                               │
┌─────────────▼─────────────┐               ┌───────────────▼──────────────┐
│      NITE-PEI             │               │         SLICDO v2            │
│  Bayesian thesis update   │               │  claims · replay · proposals │
│  CKRI · Kelly advisory    │               │  CIO-gated promotion ledger  │
└───────────────────────────┘               └──────────────────────────────┘
```

## What we deliberately removed from the public package

| Component | Why excluded |
|-----------|----------------|
| `bluelotus_publisher.py` | GitHub Pages deploy — private ops |
| Telegram push | Operator notifications — private |
| `run_v3_grand_cycle` | LLM agent council — quarantined legacy |
| Live broker fetchers | API keys · private mandate |

## What stayed

The **cognition kernel**: governed math, auditable artifacts, reproducible clerk cycles.

That is the part worth studying.
