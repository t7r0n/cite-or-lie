# Operator Brief: Mimos

Mimos gets a local, deterministic pressure test around mimos, hidden, and cites. The useful part is not the dashboard; it is the repeatable evidence path from fixture to failure to operator action.

## Highest-leverage checks

- mimos evidence replay -> block release until cited evidence is regenerated (mimos_coverage, evidence ev_0044).
- domain operator packet -> accept only if decision claims cite fixture evidence (hidden_risk, evidence ev_0055).
- cites regression harness -> open a regression issue with trace and benchmark delta (cites_precision, evidence ev_0110).
- hidden boundary probe -> route to reviewer with evidence packet (domain_latency, evidence ev_0121).

## What makes this useful

The workflow is intentionally local and deterministic. A reviewer can run the same fixture set, inspect the evidence IDs, open the dashboard, and see exactly why a recommendation passed, went to review, or blocked.
