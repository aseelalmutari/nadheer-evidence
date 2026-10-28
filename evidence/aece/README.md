# AECE Controlled Experimental Evidence

AECE is implemented in NADHEER as a decision-level physical-consistency evaluation. At a public functional level, it checks whether decision-relevant spatial evidence is observable and compatible with a physical-source hypothesis before controlling reliance on the original acoustic classification decision.

## H8-M result

H8-M is a **controlled paired mechanistic experiment** over 53 paired sessions (106 evaluated cases). Both policies retained reliance on all clean cases (53/53). For phase-modified controls with the classifier score held unchanged, classifier-only reliance was 53/53 and classifier-plus-AECE reliance was 2/53. AECE withheld reliance in 51/53 controls (96.23%; Wilson 95% interval 87.25%-98.96%).

![Decision reliance in H8-M](../../media/images/h8m_reliance_chart.png)

The exact two-sided paired secondary analysis value was `8.881784197001252e-16`. The frozen result identity is `547BD9E1E0DF965715E951234DC2A9FFDA422FF2163BA90ACD1F1CD154F005DF`.

Machine-readable public values are in the [sanitized H8-M summary](h8m_public_summary.json).

## Mandatory limitations

- H8-M used a phase-only artificial intervention that changed phase structure while preserving the controlled classifier score.
- This was not natural-confuser testing.
- This was **not field or external validation**.
- The 96.23% result is **not a real-world false-alarm estimate**.
- All 53 sessions of an outcome-blind, hash-based held-out split were included without exclusion; retention applies to classifier-gate-pass sessions from one dataset, not general sensitivity.
- H8-M did not exercise the Unavailable state; all 53 phase-modified controls resolved to a decisive state, so observability-aware unavailability is untested in this experiment.

