# Decision Report: Mecha Trace

A feature attributed report review SDK and viewer: every sentence in a Mecha draft links to a named SAE feature, a saliency overlay on the image, and a one click accept/reject that re renders the report and writes an audit row to a verifiable log.

## Evidence-Grounded Findings

CLAIM: interpretable policy boundary should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=1.708. [EVID: ev_0033]
CLAIM: mecha drift should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=2.5. [EVID: ev_0022]
CLAIM: mecha evidence recall should `block release until replay is understood` because blocks=3 reviews=3 mean_severity=1.875. [EVID: ev_0132]
CLAIM: model failure replay should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=3.333. [EVID: ev_0044]
CLAIM: state gap should `block release until replay is understood` because blocks=3 reviews=2 mean_severity=3.333. [EVID: ev_0011]
CLAIM: state reviewer handoff should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=2.583. [EVID: ev_0121]
