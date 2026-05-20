# Operator Brief: Mecha Health

Mecha Health gets a local, deterministic pressure test around mecha, state, and model. The useful part is the repeatable evidence path from fixture to failure to operator action.

## Highest-leverage checks

- mecha evidence replay -> block release until cited evidence is regenerated (mecha_coverage, evidence ev_0088).
- interpretable operator packet -> accept only if decision claims cite fixture evidence (state_risk, evidence ev_0011).
- model regression harness -> open a regression issue with trace and benchmark delta (model_precision, evidence ev_0110).
- state boundary probe -> route to reviewer with evidence packet (interpretable_latency, evidence ev_0033).

## What makes this useful

The workflow is intentionally local and deterministic. A reviewer can run the same fixture set, inspect the evidence IDs, open the dashboard, and see exactly why a recommendation passed, went to review, or blocked.
