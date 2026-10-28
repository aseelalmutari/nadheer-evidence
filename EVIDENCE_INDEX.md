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
