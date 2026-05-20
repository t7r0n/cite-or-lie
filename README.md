# Cite Or Lie

A grounded citation auditor for AI answer engines: every claimed citation in a Mimos report is verified against the answer engine's own retrieval trace (when available) and a deterministic re prompt protocol, returning a per citation (grounded | memorized | hallucinated) verdict with confidence - the compliance substrate AEO has been missing.

## Why This Exists

Every AEO tool - including Mimos - has the same hidden bug: when an LLM cites a domain, it might be citing (a) a retrieval surfaced by the answer engine's grounding (Bing / Perplexity index), (b) a training set memorization, or (c) a generation hallucination with a plausible looking URL. For a regulated wealth management or telehealth firm, distinction (a) vs. (c) is the difference between "we're winning AI search" and "we have a compliance incident in the making.

## What It Builds

- Replays synthetic `mimos` and `hidden` cases against the project's evidence rules.
- Scores `mimos_coverage`, `hidden_risk`, and `cites_precision` so regressions are visible in CSV and JSON.
- Plants `mimos drift` and `hidden gap` failures as negative controls.
- Writes citation-locked decision claims; unsupported claims fail verification.
- Exports a review dashboard and demo pack for `cite-or-lie` without hosted services.

## Local Run

```bash
uv sync
uv run cite-or-lie all
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/analysis.json`
- `outputs/scenario_report.csv`
- `outputs/decision_report.md`
- `outputs/evidence_packet.md`
- `outputs/domain_rubric.json`
- `outputs/failure_matrix.md`
- `outputs/trace_graph.mmd`
- `outputs/dashboard.html`
- `outputs/demo_pack.zip`

## Sources

- https://www.ycombinator.com/companies/mimos
- https://www.startuphub.ai/startups/mimos/
- https://www.fondo.com/blog/mimos-launches
- https://www.linkedin.com/in/michael-korovkin/
- https://www.linkedin.com/in/rohit-sirosh/
- https://aiclicks.io/blog/best-ai-search-monitoring-tools-for-chatgpt
- https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/overview

## Boundary

This repository uses synthetic fixtures only. It has no credentials, no customer data, no outreach data, and no dependency on a hosted API.
