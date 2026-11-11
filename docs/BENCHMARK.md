# Benchmark and Evaluation Protocol

The normative definitions of decipherment outcomes, autonomy, evidence requirements, and validation gates are in [Decipherment Success Criteria](DECIPHERMENT_SUCCESS_CRITERIA.md).

## Evaluation principles

A benchmark must measure a defined task, preserve uncertainty, and avoid leakage. Agreement with a published transcription is not automatically proof of correctness; reference readings may be incomplete or contested. Candidate generation is not decipherment. A system must be allowed to abstain.

## Separate evaluation tracks

### Track A — concealed-known blind recovery
- Use cases with defensible published readings hidden from the system.
- Prevent target leakage through training data, prompts, retrieval indexes, duplicate images, and near-duplicate artifacts.
- Split by physical artifact/source/context, never random image crops alone.
- Measure recovery, evidence quality, calibration, abstention, and cost.
- Report contested or weak references separately.

This measures recovery of known scholarship, not discovery of new knowledge.

### Track B — unresolved-case discovery
- Separate genuinely unresolved, disputed, damaged, and contextually difficult cases.
- Freeze case packages and evaluation budgets before runs.
- Record candidate novelty against a dated literature/database snapshot.
- Assess evidence quality, discriminative power, counter-evidence handling, holdout predictions, and abstention.
- Do not claim correctness solely from model confidence or internal consensus.

### Track C — autonomous end-to-end operation
- Measure the proportion of eligible cases completed without case-specific human intervention.
- Log intervention events, tool failures, runtime, token/compute usage, and cost.
- Report autonomous validated resolution, autonomous abstention, and autonomous failure separately.
- Post-run independent adjudication must not feed back into the frozen run.

## Task metrics

| Task | Candidate metrics | Notes |
|---|---|---|
| Detection | mAP, precision, recall | Report IoU thresholds and class definitions |
| Segmentation | IoU, boundary F1 | Evaluate alternate plausible boundaries where relevant |
| Visual retrieval | Recall@k, mAP, nDCG | Group variants and near-duplicates carefully |
| Graph classification | top-k accuracy, macro-F1 | Include open-set/unknown cases |
| Transcription | CER, WER | Only where a defensible reference exists |
| Interpretation | evidence rubric and independent adjudication | Preserve disagreement and alternatives |
| Calibration | Brier score, log loss, reliability diagrams | Only when labels and sample size support calibration |
| Abstention | coverage-versus-risk, selective risk | Report answered coverage and error together |

## Data splitting and leakage control

- Split by physical artifact or source, not random image crops.
- Keep duplicate photographs, rubbings, crops, and near-identical impressions in the same split.
- Prevent test examples and their readings from appearing in training data, retrieval indexes, prompt examples, or external caches where controllable.
- Document training, validation, test, and retrieval-index identifiers.
- Use time-based or source-held-out evaluation where feasible.
- Record the limitations of auditing foundation-model pretraining data; do not claim leakage-free status when it cannot be established.

## Baselines

Compare:
1. classical image-processing and feature-matching methods;
2. open-source computer-vision and multimodal models;
3. frontier multimodal models;
4. retrieval-augmented workflows;
5. multi-agent workflows only when a simpler baseline exists.

Human reference readings may define Track A labels and post-run adjudication, but case-specific human assistance is prohibited during the autonomous run. A complex system must demonstrate improvement over simpler baselines, not merely produce longer explanations.

## Confidence and reporting

- Keep evidence quality, dimension-level scores, calibrated probability, and outcome status distinct.
- Do not average visual, structural, semantic, historical, and contextual scores into an overall probability without a validated statistical model.
- Keep overall calibrated probability null until calibration has been demonstrated on appropriate held-out data.
- Report calibration curves and Brier score or log loss where sample size permits.
- Report selective risk as coverage changes; a high-confidence subset must not conceal low overall coverage.
- A high score cannot override a failed validation gate.

## Independent adjudication

Post-run reviewers or independent adjudicators assess frozen evidence dossiers, not steer the autonomous run. Record the adjudication method, blinding, rubric, disagreements, corrections, and date. Where independent adjudication is unavailable, retain a provisional status rather than claiming validated decipherment.

## Reporting checklist

Every benchmark report should state:
- dataset version, rights status, inclusion criteria, and unit of analysis;
- artifact/source-level split method and leakage audit limitations;
- reference quality and annotation/adjudication protocol;
- exact model IDs, prompts, parameters, tools, and run dates;
- autonomy definition and all case-specific intervention events;
- metric definitions, denominators, exclusions, and confidence intervals where feasible;
- calibration and abstention behavior;
- error categories and representative failure cases;
- compute, latency, and cost where measurable;
- limitations, unresolved cases, and conflicts of interest.
