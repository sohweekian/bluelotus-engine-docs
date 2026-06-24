# BGTM-V1 — Game Theory & Nash Equilibrium Tool Pack

**BlueLotus Geopolitical Game Theory Model (BGTM-V1)**

The only open-source family-office intelligence stack we know of that ships a **formal N-player game theory engine** wired into Bayesian thesis updating — not as a slide deck, as runnable Python.

> Full academic treatment: [BGTM PhD Thesis](https://github.com/sohweekian/bluelotus-research/blob/main/BGTM_V1_PhD_Thesis_GameTheory_NashEquilibrium_2026.md)

---

## What it is

BGTM-V1 is BlueLotus's **geopolitical overlay layer**. It takes multi-player strategic situations (Hormuz, global rates, space-sector capital rotation, Iran–US–Israel dynamics) and produces:

1. **Nash Equilibrium** analysis (with multiplicity resolution)
2. **Quantal Response Equilibrium (QRE)** — bounded rationality, not infinite-rationality fiction
3. **Correlated Equilibrium envelope** — when multiple NE exist, a single outcome distribution
4. **Global games thresholds** — kill-condition style regime switches
5. **Geo-LR Bridge** — game-derived likelihood ratios fed into **NITE-PEI** Bayesian thesis updates

```text
Geopolitical game spec
    → Nash / QRE / CE solvers (deterministic NumPy)
    → Outcome probability distribution
    → Geo-LR (bounded [0.1, 10.0])
    → Blend with static NITE-PEI LRs (cold-start safe: α = min(1, n/30))
    → Bayesian thesis posterior update
```

**Governance:** Advisory only. `manual_execution_required: true`. No LLM in the solver path. Expert-initialised payoffs — not empirical forecasts (BLV3-DOCTRINE-008).

---

## Core modules (`geo_game_theory/`)

| Module | Role |
|--------|------|
| `qre_solver.py` | Logit QRE fixed-point solver (McKelvey–Palfrey); N-player payoff tensors |
| `ce_envelope.py` | Correlated equilibrium over surviving Nash equilibria |
| `global_games.py` | Threshold classification for kill-condition style triggers |
| `geo_lr_bridge.py` | Geo-LR, cold-start blend, Bayesian posterior helper |
| `games/hormuz_2026.py` | 7-player Hormuz signalling game (thesis §7) |
| `games/global_rates_2026.py` | Global rates / central-bank game (thesis §8) |
| `games/iran_us_israel_2026.py` | Three-way geopolitical game |
| `games/space_rotation_7p_2026.py` | 7-player space-sector capital rotation |

Config wiring: `config/pl_nash_tables.yaml`, `config/pl_player_catalog.yaml`

---

## Why this matters (and why almost nobody else has it)

| Typical “finance AI” on GitHub | BlueLotus BGTM-V1 |
|-------------------------------|-------------------|
| Sentiment scores from LLMs | **Nash equilibrium** over explicit player strategies |
| Narrative geopolitical “risk off” | **Probability distribution over terminal outcomes** |
| Static thesis labels | **Dynamic Geo-LRs** updating NITE-PEI posteriors |
| Black-box agent opinions | **Deterministic solvers** cross-validated against MATLAB oracle (13/13 checks) |

GitHub search finds **zero** public repos combining: N-player Nash + QRE + geo-LR bridge + live thesis Bayesian engine.

---

## Example: Hormuz game output shape

The Hormuz spec encodes surviving Nash equilibria (e.g. talks vs standoff), maps them to market outcomes (talks, threat sustained, breakthrough, partial closure, full closure), and softens player choices via QRE — then feeds the Geo-LR bridge.

This is how BlueLotus turns **“what will Iran / US / Gulf states do?”** into **“how should our thesis probabilities move?”** — without letting an LLM guess.

---

## Math snapshot

**Nash equilibrium (concept):** No player improves payoff by unilateral deviation.

**QRE choice probabilities:**

$$\sigma_i(a_i) = \frac{e^{\lambda \cdot u_i(a_i)}}{\sum_{a_i'} e^{\lambda \cdot u_i(a_i')}}$$

**Geo-LR bridge:**

$$LR_{geo} = \frac{P(move \mid thesis\_true)}{P(move \mid thesis\_false)}$$

**Cold-start blend into NITE-PEI:**

$$LR_{adj} = (1-\alpha)\cdot LR_{static} + \alpha \cdot LR_{geo}, \quad \alpha = \min(1, n/30)$$

---

## Who should use BGTM-V1

- Researchers studying **game theory → asset pricing** bridges
- CIOs modelling **geopolitical scenario trees** with formal equilibria
- Developers extending BlueLotus with new `games/*.py` specs
- Readers of the [Von Neumann & Nash tribute](https://sohweekian.github.io/bluelotus/gametheory-tribute.html) who want the **actual engine**, not just the story

---

## Run it (public engine)

```python
from geo_game_theory.games import hormuz_2026

result = hormuz_2026.run()  # see module for full output dict
print(result)
```

Requires: `pip install` bluelotus-engine (includes `geo_game_theory` package).

---

## Live dashboard

- [BGTM thesis page](https://sohweekian.github.io/bluelotus/bgtm-thesis.html)
- [Game theory tribute — Von Neumann & Nash](https://sohweekian.github.io/bluelotus/gametheory-tribute.html)

---

*BGTM-V1 · Deterministic · Advisory only · The CIO decides*
