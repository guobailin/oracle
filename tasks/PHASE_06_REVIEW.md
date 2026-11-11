# Phase 06 — Expert review, benchmark, and release

**Window:** Weeks 11–12  
**Goal:** Validate findings, publish a transparent benchmark and research report, and define the next iteration.  
**Status:** TODO

## Work packages

### T6.1 — Prepare blind evaluation
- **Priority:** P2 | **Depends on:** Phase 05
- **Steps:** Freeze evaluation items and instructions; hide model identity and prior predictions where feasible; define scoring and adjudication.
- **Deliverable:** Blind-review packet and protocol.
- **Acceptance:** Reviewers can assess evidence without being primed by model-generated conclusions.

### T6.2 — Obtain expert review
- **Priority:** P2 | **Depends on:** T6.1
- **Steps:** Invite qualified specialists; collect structured judgments, confidence, evidence references, and disagreements; agree attribution and consent.
- **Deliverable:** Expert review records.
- **Acceptance:** Reviewer qualifications and review scope are documented; disagreements are retained rather than averaged away.

### T6.3 — Analyze errors and limitations
- **Priority:** P2 | **Depends on:** T6.2
- **Steps:** Categorize errors by image quality, segmentation, graph variation, retrieval, context, hallucination, and evaluation ambiguity.
- **Deliverable:** Error analysis report.
- **Acceptance:** Report includes representative successes and failures and avoids cherry-picking.

### T6.4 — Revise cases and conclusions
- **Priority:** P2 | **Depends on:** T6.3
- **Steps:** Update dossiers based on evidence and review; preserve prior versions and rationale for changes.
- **Deliverable:** Versioned case dossiers and decision log.
- **Acceptance:** Every changed reading or status has a traceable reason and reviewer record.

### T6.5 — Publish benchmark and documentation
- **Priority:** P2 | **Depends on:** T6.3, T6.4
- **Steps:** Prepare benchmark card, task definitions, splits, metrics, data statement, model cards, and reproducibility instructions; release only assets permitted for release.
- **Deliverable:** Public benchmark release package.
- **Acceptance:** Rights, limitations, intended use, leakage controls, and known biases are clearly documented.

### T6.6 — Publish final report and next roadmap
- **Priority:** P2 | **Depends on:** T6.1–T6.5
- **Steps:** Summarize research question, methods, results, expert feedback, unresolved issues, and next experiments.
- **Deliverable:** `reports/12_week_research_report.md` and updated roadmap.
- **Acceptance:** Claims are supported by citations and benchmark results; negative results and uncertainty are reported.

## Release checklist

- [ ] All source assets have provenance and rights review.
- [ ] No restricted images or annotations are redistributed without permission.
- [ ] Dataset and benchmark splits are documented and leakage-checked.
- [ ] Model/provider versions and experiment settings are recorded.
- [ ] Human and AI contributions are distinguished.
- [ ] Expert review scope, consent, and attribution are documented.
- [ ] Uncertainty, disagreements, and failure cases are visible.
- [ ] Release notes identify limitations and intended use.

## Phase exit gate
The public release is reproducible, rights-aware, expert-reviewed to the extent stated, and explicit about what remains undeciphered.
