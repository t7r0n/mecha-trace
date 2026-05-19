# Mecha Trace

A feature attributed report review SDK and viewer: every sentence in a Mecha draft links to a named SAE feature, a saliency overlay on the image, and a one click accept/reject that re renders the report and writes an audit row to a verifiable log.

## Why This Exists

Mecha has a state of the art model and 17,000 interpretable features (interpretability blog), but the AmeriRad rollout will not be gated on CheXbert F1 - it will be gated on PACS/DICOM ingestion at line rate and HL7 report write back without surprises, which is the load bearing operational layer they have not yet publicly shown. More importantly: when a radiologist disagrees with a draft, today's pipeline gives them a paragraph to edit.

## What It Builds

- Replays synthetic `mecha` and `state` cases against the project's evidence rules.
- Scores `mecha_coverage`, `state_risk`, and `model_precision` so regressions are visible in CSV and JSON.
- Plants `mecha drift` and `state gap` failures as negative controls.
- Writes citation-locked decision claims; unsupported claims fail verification.
- Exports a review dashboard and demo pack for `mecha-trace` without hosted services.

## Local Run

```bash
uv sync
uv run mecha-trace all
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/analysis.json`
- `outputs/scenario_report.csv`
- `outputs/decision_report.md`
- `outputs/evidence_packet.md`
- `outputs/dashboard.html`
- `outputs/demo_pack.zip`

## Sources

- https://www.ycombinator.com/launches/MeX-mecha-health-trustworthy-medical-image-reporting-using-ai
- https://www.mecha-health.ai/blog/Mecha-net-v0.1
- https://www.mecha-health.ai/blog/Interpreting-a-radiological-foundation-model
- https://www.mecha-health.ai/about-us
- https://radiologybusiness.com/press-release/mecha-health-raises-41m-seed-round-build-next-generation-foundation-models-radiology
- https://americanradiologysolutions.com/blog/amerirad-partners-with-mecha-health/
- https://arxiv.org/abs/2410.03334
- https://ucl-pond.github.io/author/ahmed-abdulaal-abdulaal/
- https://www.menlotimes.com/post/mecha-health-raises-4-1-million-seed-round-to-build-next-generation-foundation-models-for-radiology

## Boundary

This repository uses synthetic fixtures only. It has no credentials, no customer data, no outreach data, and no dependency on a hosted API.
