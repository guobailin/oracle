# Phase 04 — AI baseline experiments

**Window:** Weeks 7–8  
**Goal:** Measure what current methods can and cannot do on the pilot corpus before attempting difficult decipherment.  
**Status:** TODO

## Work packages

### T4.1 — Detection and segmentation baseline
- **Priority:** P1 | **Depends on:** Phase 03
- **Steps:** Establish simple image-processing baselines and suitable learned detectors/segmenters; define annotation-compatible evaluation.
- **Deliverable:** Reproducible detection/segmentation experiment.
- **Acceptance:** Report precision, recall, F1 or IoU as appropriate, with per-condition breakdowns and failure examples.

### T4.2 — Visual similarity retrieval
- **Priority:** P1 | **Depends on:** T3.4
- **Steps:** Compare handcrafted features and image embeddings; build nearest-neighbor retrieval; test sensitivity to scale, rotation, damage, and writing variation.
- **Deliverable:** Retrieval index, evaluation script, and ranked-result report.
- **Acceptance:** Report Recall@K / mAP (as appropriate), query protocol, candidate-set construction, and hard negatives.

### T4.3 — Multimodal candidate generation
- **Priority:** P1 | **Depends on:** T3.5
- **Steps:** Test multimodal models on carefully scoped tasks such as describing visible structure or proposing candidate classes; require citations or explicit “no evidence” responses.
- **Deliverable:** Model evaluation set and error analysis.
- **Acceptance:** Separate visual observation from inferred reading; hallucinated strokes, unsupported certainty, and failure to abstain are measured.

### T4.4 — Contextual retrieval and reasoning
- **Priority:** P1 | **Depends on:** T1.4, T3.5
- **Steps:** Build a small retrieval corpus of citable scholarly material; test retrieval before generation; compare answers with and without retrieved context.
- **Deliverable:** RAG baseline, source index manifest, and evaluation report.
- **Acceptance:** Every generated scholarly claim is traceable to retrieved passages; retrieval errors and citation failures are reported.

## Experimental controls

- Record dataset version, split, code commit, model/provider/version, prompt, decoding settings, and compute cost.
- Use artifact/source-level splits; avoid near-duplicate leakage.
- Compare against simple baselines, not only large language models.
- Keep a held-out test set untouched during prompt/model iteration.
- Measure abstention and calibration; an unknown answer can be correct.
- Do not treat agreement among models as independent scholarly corroboration.

## Required report format

For each experiment: research question, data snapshot, method, baselines, metrics, results, error examples, limitations, cost, reproducibility instructions, and next decision.

## Phase exit gate
A third party can reproduce the principal baseline results from the recorded configuration and data manifest; limitations are explicit.
