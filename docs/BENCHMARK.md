# Benchmark and Evaluation Protocol

## Evaluation principles

A benchmark must measure a defined task, preserve uncertainty, and avoid leakage. Agreement with a published transcription is not automatically proof of correctness; reference readings may be incomplete or contested.

## Task metrics

| Task | Candidate metrics | Notes |
|---|---|---|
| Detection | mAP, precision, recall | Report IoU thresholds and class definitions |
| Segmentation | IoU, boundary F1 | Evaluate alternate plausible boundaries where relevant |
| Visual retrieval | Recall@k, mAP, nDCG | Group variants and near-duplicates carefully |
| Graph classification | top-k accuracy, macro-F1 | Include open-set/unknown cases |
| Transcription | CER, WER | Only where a defensible reference exists |
| Missing-position recovery | top-k, calibration, abstention | Keep damaged/unrecoverable cases distinct |
| Interpretation | expert rubric | Assess evidence, alternatives, and contextual fit |
| Hypothesis quality | blinded expert review | Record disagreement and confidence calibration |

## Data splitting

- Split by physical artifact or source, not random image crops.
- Keep duplicate photographs, rubbings, crops, and near-identical impressions in the same split.
- Prevent test examples from appearing in retrieval indexes or prompt examples.
- Document all training, validation, and test identifiers.
- Use a time-based or source-held-out evaluation where feasible.

## Baselines

Compare:
1. qualified human readers, with inter-annotator disagreement reported;
2. classical image-processing and feature-matching methods;
3. open-source computer-vision models;
4. open multimodal models;
5. frontier multimodal models;
6. retrieval-augmented and multi-agent workflows.

A complex multi-agent system should demonstrate improvement over simpler baselines, not merely produce longer explanations.

## Expert review rubric

Reviewers can score each dimension on a documented scale:
- fidelity to visible evidence;
- quality and relevance of comparanda;
- correctness of citations and source locators;
- linguistic and formulaic plausibility;
- engagement with counter-evidence;
- calibration and appropriate abstention;
- clarity about what remains unresolved.

Do not collapse all dimensions into a single score without publishing the component scores.

## Reporting checklist

Every benchmark report should state:
- dataset version, rights status, and inclusion criteria;
- artifact-level split method;
- annotation protocol and agreement;
- exact model IDs, prompts, parameters, and run dates;
- metric definitions and confidence intervals where appropriate;
- error categories and representative failure cases;
- performance on unknown, damaged, and disputed examples;
- compute, latency, and cost where measurable;
- limitations and conflicts of interest.