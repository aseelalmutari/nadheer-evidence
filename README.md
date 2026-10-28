# NADHEER - From Scientific Research to a Working System

NADHEER addresses the limitations of isolated drone-detection signals by integrating acoustic sensing, visual detection, and decision-level physical-consistency verification in a working edge platform. Documented model training, software verification, and controlled paired experiments provide traceable evidence of the implemented system; no completed field validation is claimed.

![NADHEER implemented multimodal research dashboard](media/images/nadheer_live_system.png)

### [View AECE Controlled Evidence](evidence/aece/README.md)

### [Explore Training & Experimental Results](#8-experimental-results)

> NADHEER is an implemented research system supported by documented development, interface evidence, and verifiable experimental records.

## 1. Project Overview

NADHEER is a local, edge-oriented multimodal research platform for detecting and evaluating possible drone-related events. Its implemented software joins acoustic classification, multichannel direction estimation when array input is available, visual detection, object tracking, decision fusion, evidence logging, and a browser dashboard. [Evidence: SYS-001](EVIDENCE_INDEX.md#sys-001)

AECE, the Acoustic Evidence Consistency Evaluation, is a decision-level verification layer implemented as a research module and evaluated on preserved recordings; it is not yet part of the live detection loop. The public description is intentionally functional and does not expose protected implementation details or source code.

## 2. Research Problem

An acoustic classifier can produce a confident positive decision even when environmental sounds or altered spatial structure do not support the physical interpretation suggested by that decision. A deployable system therefore needs more than a classifier confidence score: it needs a documented way to examine whether relevant multichannel evidence is physically observable and consistent before relying on that positive decision.

## 3. Scientific Motivation

Prior work demonstrates acoustic UAV classification, microphone-array localization, target-conditioned spatial processing, and evidence weighting. The bounded gap identified in the reviewed sources is the combination of decision-relevant evidence, a matching multichannel reference path, physical-source compatibility states, observability-aware unavailability, and direct control of reliance on the original classification decision. This is a bounded literature finding, not a universal novelty claim. [Evidence: REF-001](EVIDENCE_INDEX.md#ref-001)

## 4. Implemented System

The implemented platform provides:

- acoustic event classification;
- optional multichannel direction-of-arrival processing;
- camera-based visual detection and tracking;
- decision fusion and alert-state computation;
- append-only event evidence logging;
- a live browser dashboard; and
- documented AECE controlled experimental evidence.

The dashboard screenshot establishes implementation of the interface. Because it visibly reports `demo mode`, it is not presented as a field experiment or accuracy result. [Evidence: SYS-001](EVIDENCE_INDEX.md#sys-001)

## 5. Development Evidence

The project contains traceable development records for dataset preparation, classifier hardening, controlled AECE studies, software verification, interface development, and evidence hashing. This repository does not include Git history, source code, raw logs, or model weights. It publishes bounded sanitized summaries and approved evidence artifacts.

## 6. Dataset Sources

Documented sources include UaVirBASE, DroneNoise, Drone Audio Detection Samples (DADS), and ESC-50. Their roles, source links, and attribution/licence notes are listed in the [dataset provenance page](datasets/README.md). No third-party audio is distributed in this repository. [Evidence: DATA-001](EVIDENCE_INDEX.md#data-001)

## 7. Training Evidence

The clean acoustic CRNN was trained after a provenance review corrected 208 two-second rows and 416 derived one-second rows while preserving the historical dataset. The clean split contained 10,913 training, 2,238 validation, and 2,370 held-out internal test samples. The test split contained 1,430 drone and 940 non-drone samples. [Evidence: TRAIN-001](EVIDENCE_INDEX.md#train-001)

The clean CRNN achieved accuracy 0.9911, recall 0.9909, and a false-positive rate of 0.0085 on the 2,370-sample test split at decision threshold 0.50. The confusion matrix was TN=932, FP=8, FN=13, and TP=1,417. These are **internal dataset-based evaluation** results and **not field performance**. [Evidence: TRAIN-001](EVIDENCE_INDEX.md#train-001)

Read the [training evidence and limitations](evidence/training/README.md) or inspect the [sanitized machine-readable summary](evidence/training/classifier_summary.json).

## 8. Experimental Results

### Clean CRNN classifier

| Evidence | Verified result | Interpretation boundary |
|---|---|---|
| Dataset | 15,521 samples; 2,370 held-out internal test samples | Internal dataset-based evaluation; not field performance |
| Clean CRNN | Accuracy 0.9911; recall 0.9909 at decision threshold 0.50 | Does not establish outdoor accuracy or operational range |
| Held-out false-positive rate | 0.0085 | Not a deployment false-alarm rate |

[Evidence: TRAIN-001](EVIDENCE_INDEX.md#train-001)

### H8-M controlled AECE experiment

H8-M was a **controlled paired mechanistic experiment** with 53 paired sessions and 106 evaluated cases. Clean-case reliance was retained in 53/53 cases for both policies. On phase-modified controls with the classifier score held unchanged, classifier-only reliance was 53/53 and classifier-plus-AECE reliance was 2/53. AECE therefore withheld reliance in 51/53 controls, or 96.23% (Wilson 95% interval 87.25%-98.96%). [Evidence: AECE-002](EVIDENCE_INDEX.md#aece-002)

This phase-only artificial intervention was not natural-confuser testing, **not field or external validation**, and **not a real-world false-alarm estimate**. All 53 sessions of an outcome-blind, hash-based held-out split were included without exclusion; retention applies to classifier-gate-pass sessions from one dataset, not general sensitivity.

[![H8-M decision reliance chart](media/images/h8m_reliance_chart.png)](evidence/aece/README.md#h8-m-result)

### Follow-up analyses (post-hoc)

Two follow-up analyses, each with a protocol frozen by SHA-256 before computation, test what H8-M can and cannot show. [Evidence: AECE-003](EVIDENCE_INDEX.md#aece-003) · [Evidence: AECE-004](EVIDENCE_INDEX.md#aece-004)

- **H8-N:** a decision-agnostic inter-channel coherence check also retained 53/53 clean cases and withheld reliance on 53/53 phase-modified controls. H8-M therefore shows sensitivity to spatial invalidation but does not by itself distinguish AECE from a generic coherence check.
- **H8-O:** phase was randomized only in the time-frequency regions supporting the classifier decision (A) or in an equal number of other regions (B).

| Condition | Classifier + AECE withheld | Coherence check withheld |
|---|---|---|
| Clean | 0/53 | 0/53 |
| A: decision-supporting regions modified | 51/53 (Wilson 95% 87.25%-98.96%) | 30/53 |
| B: equal number of other regions modified | 0/53 (Wilson 95% 0%-6.76%) | 34/53 |

The B result follows from AECE's design, because its decision path reads only decision-supporting regions; H8-O verifies that decision conditioning works as designed. Machine-readable values are in the [follow-up summary](evidence/aece/h8_followup_public_summary.json).

### Runtime

In the unoptimised research implementation, processing takes a median 2.59 s (p95 2.94 s) per one-second decision window on an Intel Core i7-10750H CPU. This is not real-time; optimisation and edge-device timing are future work. [Evidence: RUN-001](EVIDENCE_INDEX.md#run-001)

### Software verification

Preserved logs report 267 AECE-specific tests, 36 project smoke tests, and 70/70 multimodal tests passed. These counts are software verification only; they are not scientific performance or field validation. [Evidence: TEST-001](EVIDENCE_INDEX.md#test-001)

## 9. Limitations

- No completed open-field validation is claimed.
- No real-world deployment false-alarm rate or operational detection range is claimed.
- H8-M uses a controlled phase-only artificial intervention rather than natural environmental confusers.
- H8-M did not exercise the Unavailable state; all 53 phase-modified controls resolved to a decisive state, so observability-aware unavailability is untested in this experiment.
- Classifier metrics come from an internal dataset-based split and are not field performance.
- The dashboard screenshot establishes visible interface implementation only.
- Third-party datasets are referenced, not redistributed; see [datasets/README.md](datasets/README.md) for licence and attribution notes.
- Software-test counts establish covered implementation behavior, not scientific generalization.
- H8-N and H8-O are post-hoc analyses; in H8-L and H8-O the reference hypothesis was held at its clean value, so the reference path's response to modified recordings was not tested.
- AECE is a research module and is not yet part of the live detection loop; current runtime is not real-time.
- The application has not been granted, and no absolute world-first novelty is claimed.

## 10. Scientific References

The [selected references](references/README.md) cover microphone-array UAV sensing, acoustic classification and tracking, target-masked localization, phase-aware spatial processing, and relevance-weighted acoustic representations. [Evidence: REF-001](EVIDENCE_INDEX.md#ref-001)

## 11. Intellectual Property Notice

> A Saudi patent application relating to the AECE technology was filed on 2 September 2026 under application number SA 1020268824. The application has not been granted and is not publicly published. This repository provides selected scientific documentation and evidence; implementation details are intentionally withheld.

This notice reports administrative status only. It does not characterize claim scope, examination outcome, publication, or protection outside the filed application. The application documents, claims, amendment material, and examiner communications are not included. [Evidence: IP-001](EVIDENCE_INDEX.md#ip-001)

## 12. Evidence Index

Every principal claim above maps to a sanitized artifact and an explicit interpretation boundary in the [Evidence Index](EVIDENCE_INDEX.md).
