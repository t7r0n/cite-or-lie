# Decision Report: Cite Or Lie

A grounded citation auditor for AI answer engines: every claimed citation in a Mimos report is verified against the answer engine's own retrieval trace (when available) and a deterministic re prompt protocol, returning a per citation (grounded | memorized | hallucinated) verdict with confidence - the compliance substrate AEO has been missing.

## Evidence-Grounded Findings

CLAIM: every drift should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=2.5. [EVID: ev_0022]
CLAIM: every evidence recall should `block release until replay is understood` because blocks=3 reviews=3 mean_severity=1.875. [EVID: ev_0132]
CLAIM: hidden policy boundary should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=1.708. [EVID: ev_0033]
CLAIM: including gap should `block release until replay is understood` because blocks=3 reviews=2 mean_severity=3.333. [EVID: ev_0011]
CLAIM: including reviewer handoff should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=2.583. [EVID: ev_0121]
CLAIM: mimos failure replay should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=3.333. [EVID: ev_0044]
