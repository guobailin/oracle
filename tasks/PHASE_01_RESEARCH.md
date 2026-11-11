# Phase 01 — Research landscape and resource audit

**Window:** Weeks 1–2  
**Goal:** Establish what is already known, what data can lawfully be used, and where a meaningful research gap exists.  
**Status:** TODO

## Work packages

### T1.1 — Define the unresolved-problem taxonomy
- **Priority:** P0 | **Depends on:** None
- **Steps:** Review representative scholarly discussions; distinguish graph-form uncertainty from reading disputes and inscription-level interpretation; define labels and boundary cases.
- **Deliverable:** `reports/problem_taxonomy.md`
- **Acceptance:** At least four distinct problem classes are defined with inclusion/exclusion rules and examples. Do not label a graph “unread” merely because it is absent from one database.

### T1.2 — Audit oracle-bone databases
- **Priority:** P0 | **Depends on:** T1.1
- **Steps:** Inventory institutional and scholarly databases; record coverage, search functions, image access, metadata, citation conventions, update status, and access restrictions.
- **Deliverable:** `reports/database_comparison.csv` plus a short analysis.
- **Acceptance:** Every entry has a stable URL, access date, institution/operator, coverage note, and known limitation.

### T1.3 — Audit machine-learning datasets
- **Priority:** P0 | **Depends on:** T1.1
- **Steps:** Record dataset size, image/annotation units, class coverage, annotation provenance, licensing, permitted use, known duplication, and split methodology.
- **Deliverable:** `datasets/source_register.csv`
- **Acceptance:** No dataset is marked reusable until its license and terms are checked. Distinguish research access from permission to redistribute or train commercial models.

### T1.4 — Literature review
- **Priority:** P0 | **Depends on:** T1.1
- **Steps:** Collect foundational paleography, corpus/digital humanities, imaging, computer vision, multimodal learning, and recent AI-assisted decipherment work; summarize claims and limitations.
- **Deliverable:** `reports/literature_review.md`
- **Acceptance:** Each key claim is tied to a bibliographic reference; separate peer-reviewed findings, preprints, database descriptions, and project claims.

### T1.5 — AI capability review
- **Priority:** P1 | **Depends on:** T1.3, T1.4
- **Steps:** Identify candidate OCR/detection, image embedding, visual-language, retrieval, and language models; note availability, license, inference cost, and reproducibility.
- **Deliverable:** `reports/model_landscape.md`
- **Acceptance:** Model selection is based on task fit and measurable baselines, not headline capability claims.

### T1.6 — Gap and differentiation analysis
- **Priority:** P1 | **Depends on:** T1.2–T1.5
- **Steps:** Compare existing resources and systems; identify under-served tasks, data bottlenecks, and feasible contribution; state what the project will not attempt.
- **Deliverable:** `reports/research_gap.md`
- **Acceptance:** One primary research question and no more than three secondary questions are stated, each with evidence and a feasibility rationale.

## Phase exit gate
A reviewer can trace the project's chosen problem to existing scholarship and resources, verify access constraints, and understand the specific contribution proposed.
