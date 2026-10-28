# Clean Acoustic CRNN

The current acoustic CRNN was trained on the clean provenance dataset after review corrected 208 two-second rows and 416 derived one-second rows while preserving the historical dataset. The evidence reported here is an **internal dataset-based evaluation** and **not field performance**.

## Dataset and split

| Item | Count |
|---|---:|
| Training samples | 10,913 |
| Validation samples | 2,238 |
| Held-out internal test samples | 2,370 |
| Drone test samples | 1,430 |
| Non-drone test samples | 940 |

## Held-out internal result

| Metric | Result |
|---|---:|
| Decision threshold | 0.50 |
| Accuracy | 0.9911 |
| Recall | 0.9909 |
| False-positive rate | 0.0085 |
| Confusion matrix | TN=932, FP=8, FN=13, TP=1,417 |

Machine-readable values are available in the [sanitized classifier summary](classifier_summary.json).

## Interpretation boundary

These values describe one internal held-out split from the clean provenance dataset. They do not establish outdoor detection performance, operational range, performance against unseen natural confusers, or a deployment false-alarm rate.
