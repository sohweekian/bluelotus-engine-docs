# Download BlueLotus Engine

**Version:** 3.0.0 (frozen — no further software updates planned)  
**License:** MIT · Research only · No advice · No orders

---

## Option 1 — pip install from GitHub release (recommended)

```bash
pip install https://github.com/sohweekian/bluelotus-engine/releases/download/v3.0.0/bluelotus_engine-3.0.0-py3-none-any.whl
```

Verify:

```bash
python -m bluelotus_engine.cli --help
```

---

## Option 2 — Download files manually

Go to the release page and download what you need:

**https://github.com/sohweekian/bluelotus-engine/releases/tag/v3.0.0**

| File | Use |
|------|-----|
| `bluelotus_engine-3.0.0-py3-none-any.whl` | pip install (fastest) |
| `bluelotus_engine-3.0.0.tar.gz` | Source distribution / audit |

Install from a downloaded wheel:

```bash
pip install path\to\bluelotus_engine-3.0.0-py3-none-any.whl
```

---

## Option 3 — Clone source

```bash
git clone https://github.com/sohweekian/bluelotus-engine.git
cd bluelotus-engine
pip install -e .
```

---

## First run (demo data included)

```bash
mkdir bluelotus-lab && cd bluelotus-lab
python -m bluelotus_engine.cli init-workspace
python -m bluelotus_engine.cli pipeline --once --dry-run
python -m bluelotus_engine.cli clerk
```

This uses **synthetic demo data** — no API keys, no real portfolio.

---

## Requirements

- Python **3.11+**
- Windows, macOS, or Linux
- Dependencies install automatically: PyYAML, openpyxl, python-docx, jsonschema

---

## Documentation bundle (read before you run)

| Document | URL |
|----------|-----|
| What is it? | [WHAT_IS_BLUELOTUS.md](https://github.com/sohweekian/bluelotus-engine-docs/blob/main/WHAT_IS_BLUELOTUS.md) |
| Who is it for? | [WHO_IS_IT_FOR.md](https://github.com/sohweekian/bluelotus-engine-docs/blob/main/WHO_IS_IT_FOR.md) |
| Architecture | [ARCHITECTURE.md](https://github.com/sohweekian/bluelotus-engine-docs/blob/main/ARCHITECTURE.md) |
| Story | [README.md](https://github.com/sohweekian/bluelotus-engine-docs/blob/main/README.md) |
| Theses | [bluelotus-research](https://github.com/sohweekian/bluelotus-research) |

---

## What is not in the download

- Live broker / Moomoo fetchers
- GitHub Pages publisher
- Telegram notifications
- LLM agent council (quarantined legacy)
- Private production configuration or work orders

Bring your own `dataset_raw.json` for real research (see `schemas/dataset_raw.schema.json` in the engine repo).
