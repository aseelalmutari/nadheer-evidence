# NADHEER Evidence Index

This index maps public claims to approved, sanitized evidence artifacts and states the interpretation boundary for each claim.

## SYS-001

- **Claim:** An implemented NADHEER dashboard and system interface exist.
- **Artifact:** [Sanitized dashboard screenshot](media/images/nadheer_live_system.png)
- **SHA-256:** `86C36E5CC04B021F885BEEAE1B548ECB4E9EF249CC3227624F372F3A6B4A34AF`
- **Source type:** Project screenshot captured from the implemented interface.
- **Scope:** Interface implementation evidence.
- **Limitation:** The screenshot visibly reports `demo mode`; it is not a live field experiment, accuracy result, or operational validation.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## VIDEO-PLATFORM-001

- **Claim:** A recorded demonstration shows operation of the implemented NADHEER dashboard and its principal interfaces.
- **Artifact:** [Platform demonstration](media/videos/nadheer_platform_demo.mp4)
- **SHA-256:** `FDCE904226076208479DB167BF9622955BC2EA94198D07EF4197D4FFD00FF243`
- **Source type:** Owner-supplied project recording; video stream copied without re-encoding and silent audio track removed.
- **Scope:** Visible implementation, interface operation, live status updates, offline audio-analysis interface, and AECE Decision Lab replay.
- **Limitation:** Demonstration evidence only; not detection-accuracy, field-performance, false-alarm-rate, operational-range, or external-validation evidence.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## TRAIN-001

- **Claim:** The clean acoustic CRNN achieved accuracy 0.9911, recall 0.9909, and false-positive rate 0.0085 on a 2,370-sample held-out internal test split at decision threshold 0.50 (TN=932, FP=8, FN=13, TP=1,417).
- **Artifact:** [Sanitized classifier summary](evidence/training/classifier_summary.json)
- **SHA-256:** `BC70C02FBC40A1067248F95BB25F89FDEE648FA4D1E176431492CF7031D90AED`
- **Source type:** Sanitized derivative of the clean-provenance CRNN per-clip evaluation and result summary.
- **Scope:** Internal dataset-based evaluation.
- **Limitation:** Not field performance; not an outdoor or deployment false-alarm estimate.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## AECE-002

- **Claim:** In the H8-M controlled paired mechanistic experiment, clean retention was 53/53 for both policies and modified-control reliance was 53/53 for classifier-only versus 2/53 for classifier-plus-AECE; AECE non-reliance was 51/53 = 96.23%.
- **Artifact:** [Sanitized H8-M summary](evidence/aece/h8m_public_summary.json)
- **SHA-256:** `76E0C2E162EFB4BB82EE9EFE0318795F909A0D39103A93D64247E2BA509C284A`
- **Frozen result identity SHA-256:** `547BD9E1E0DF965715E951234DC2A9FFDA422FF2163BA90ACD1F1CD154F005DF`
- **Source type:** Sanitized derivative of the frozen H8-M result.
- **Scope:** Controlled paired mechanistic evidence using a phase-only artificial intervention.
- **Limitation:** Not natural-confuser testing, not field or external validation, and not a real-world false-alarm estimate.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## AECE-RESULT-001

- **Claim:** The approved H8-M aggregate values can be visualized without exposing implementation rules.
- **Artifact:** [Sanitized reliance chart](media/images/h8m_reliance_chart.png)
- **SHA-256:** `8BAFF41C6ADAE8EF1DE0F4966C87FC3F4BA8331F89AF78947DA1F190A5E2FF3D`
- **Scope:** Visualization of AECE-002 only.
- **Limitation:** The chart has the same controlled, artificial-intervention, non-field boundaries as AECE-002.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## AECE-UI-001

- **Claim:** The AECE Decision Lab deterministically replays the frozen H8-M evidence.
- **Artifact:** [Decision Lab screenshot](media/images/aece_decision_lab.png)
- **SHA-256:** `2A3329FE39EC2B55667557264CB1C4A27984A10419D531985B05271F5832E717`
- **Source type:** Project screenshot captured from the implemented interface.
- **Scope:** Interface and deterministic replay evidence.
- **Fingerprint clarification:** The truncated fingerprint visible in the image identifies the archived copy of the result file with Windows (CRLF) line endings. After line-ending normalization it matches the frozen H8-M result identity (547BD9E1…05DF).
- **Limitation:** Not a new experiment; AECE is not yet part of the live detection loop.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## AECE-ARCH-001

- **Claim:** AECE has a high-level decision-conditioned path, independent reference path, observability gate, physical compatibility state, and reliance-control output.
- **Artifact:** [High-level diagram](media/images/aece_dual_path.png)
- **SHA-256:** `F4C1A15AD40955CA27C148EFAAA581E65AE95A4741ECE0A522F5FC45C6670F78`
- **Source type:** Project conceptual diagram.
- **Scope:** Conceptual architecture only.
- **Limitation:** Rules, thresholds, equations, calibration, code, and raw inputs are intentionally omitted.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## VIDEO-AECE-001

- **Claim:** The platform demonstration shows the AECE Decision Lab replaying the aggregate H8-M evidence.
- **Artifact:** [Platform demonstration (Decision Lab segment)](media/videos/nadheer_platform_demo.mp4)
- **SHA-256:** `FDCE904226076208479DB167BF9622955BC2EA94198D07EF4197D4FFD00FF243`
- **Source type:** Same recording as VIDEO-PLATFORM-001.
- **Scope:** Interface replay of the published aggregate H8-M evidence.
- **Limitation:** Not a new experiment, not disclosure of protected implementation rules, and not field or external validation.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## AECE-003

- **Claim:** A decision-agnostic coherence check retained 53/53 clean cases and withheld reliance on 53/53 H8-M phase-modified controls (H8-N).
- **Artifact:** [Follow-up summary](evidence/aece/h8_followup_public_summary.json)
- **SHA-256:** `B50378B4A05533FE1A17F5CEA917D0908ED463104175CDC66571438EDBFD9CEB`
- **Source type:** Sanitized derivative of the frozen post-hoc result files (identities listed in the artifact).
- **Scope:** Post-hoc baseline comparison on the H8-M cases.
- **Limitation:** Shows that H8-M alone does not distinguish AECE from a generic coherence check; not field validation.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## AECE-004

- **Claim:** Under decision-localized phase invalidation AECE withheld reliance in 51/53 sessions and under equal-size off-decision invalidation in 0/53; the coherence check withheld in 30/53 and 34/53 (H8-O).
- **Artifact:** [Follow-up summary](evidence/aece/h8_followup_public_summary.json)
- **SHA-256:** `B50378B4A05533FE1A17F5CEA917D0908ED463104175CDC66571438EDBFD9CEB`
- **Source type:** Sanitized derivative of the frozen post-hoc result files (identities listed in the artifact).
- **Scope:** Post-hoc controlled test of decision conditioning.
- **Limitation:** The off-decision result follows from AECE design; reference path held at its clean value; artificial intervention; not field validation.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## RUN-001

- **Claim:** Median processing time is 2.59 s (p95 2.94 s) per one-second decision window on an Intel Core i7-10750H CPU (H8-P).
- **Artifact:** [Follow-up summary](evidence/aece/h8_followup_public_summary.json)
- **SHA-256:** `B50378B4A05533FE1A17F5CEA917D0908ED463104175CDC66571438EDBFD9CEB`
- **Source type:** Sanitized derivative of the frozen post-hoc result files (identities listed in the artifact).
- **Scope:** Runtime of the unoptimised research implementation.
- **Limitation:** Not real-time; not edge-device timing.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## TEST-001

- **Claim:** Preserved logs report 267 AECE-specific, 36 project smoke, and 70/70 multimodal passed tests.
- **Artifact:** [Sanitized software-verification summary](evidence/software_verification/test_summary.json)
- **SHA-256:** `606BE8C1340DB5D9AA8C165E38C8DF3C8749B01FEB9E76271E0A854FFF958FDB`
- **Scope:** Software verification.
- **Limitation:** Not scientific performance, field accuracy, or external validation.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## DATA-001

- **Claim:** The project documents source provenance for UaVirBASE, DroneNoise, DADS, and ESC-50.
- **Artifact:** [Dataset sources](datasets/README.md)
- **SHA-256:** `5B4A7EF4139F1A21400109A756954F7F77927E8CB8B8E697F19F8D513A674F02`
- **Scope:** Source links, project role, and attribution/licence notes.
- **Limitation:** No third-party audio is included or redistributed.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## REF-001

- **Claim:** The project has a DOI/publisher-verified scientific background and a bounded research-gap statement.
- **Artifact:** [Selected scientific references](references/README.md)
- **SHA-256:** `0047118824F9FAD480596F92ACCB3F3FC02FCD4928A8B213D865D70729B9E161`
- **Scope:** Selected primary literature from the documented reference audit.
- **Limitation:** Not a patent-scope conclusion or universal novelty claim.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## IP-001

- **Claim:** Saudi application `SA 1020268824` was filed on 2 September 2026; it is not publicly published, has no publication number, and has not been granted.
- **Artifact:** [Public administrative notice](README.md#11-intellectual-property-notice)
- **Source type:** Administrative filing information from the official application summary.
- **Scope:** Administrative status only.
- **Limitation:** No claim-scope, publication-stage, examination-outcome, or cross-jurisdiction conclusion.
- **Status:** `APPROVED FOR PUBLIC RELEASE`

## Public release scope

This index includes only the evidence items approved for the repository. Items outside this index are not part of the release package.
