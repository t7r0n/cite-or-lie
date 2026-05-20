# Cite Or Lie

A grounded citation auditor for AI answer engines: every claimed citation in a Cite Or Lie report is verified against the answer engine's own retrieval trace (when available) and a deterministic re prompt protocol, returning a per citation (grounded | memorized | hallucinated) verdict with confidence — the compliance substrate AEO has been missing.

![Cite Or Lie working dashboard](outputs/project_working.svg)

## Why it exists

Every AEO tool — including Cite Or Lie — has the same hidden bug: when an LLM cites a domain, it might be citing (a) a retrieval surfaced by the answer engine's grounding (Bing / Perplexity index), (b) a training set memorization, or (c) a generation hallucination with a plausible looking URL. For a regulated wealth management or telehealth firm, distinction.

The project is intentionally built as a local replay harness instead of a slide. It creates fixtures, plants realistic failure modes, produces citation-locked evidence, and turns the result into a dashboard a reviewer can inspect without credentials or hosted services.

## What is inside

- Deterministic fixture generation for the company-specific risk surface.
- Strategy code in `src/cite_or_lie/strategy.py` with project-specific scoring and visual evidence.
- Citation-locked reports where every decision claim points to a generated evidence ID.
- Two regenerated visual artifacts: `outputs/project_working.svg` and `outputs/evidence_map.svg`.
- A portable demo pack with JSON, CSV, Markdown, HTML, SVG, benchmark, and test artifacts.

![Cite Or Lie evidence map](outputs/evidence_map.svg)

## Signals it measures

- `Cite Or Lie coverage`
- `hidden risk`
- `cites precision`
- `domain latency`

## Failure modes it plants

- Cite Or Lie drift
- hidden gap
- cites misroute
- domain blindspot

## Run it locally

```bash
uv sync
uv run cite-or-lie all
uv run pytest -q
uv run ruff check .
```

## Outputs worth opening

- `outputs/dashboard.html`
- `outputs/project_working.svg`
- `outputs/evidence_map.svg`
- `outputs/operator_brief.md`
- `outputs/decision_report.md`
- `outputs/strategy_model.json`
- `outputs/demo_pack.zip`

## Boundary

Everything runs locally against synthetic fixtures. There are no credentials, no customer records, no outreach files, and no hosted API dependency.
