# Phase 03 — Pilot corpus construction

**Window:** Weeks 5–6  
**Goal:** Build a small, well-documented corpus suitable for controlled experiments.  
**Status:** TODO

## Work packages

### T3.1 — Acquire permitted source material
- **Priority:** P1 | **Depends on:** Phase 02
- **Steps:** Obtain images and metadata through authorized sources; record terms, attribution, access date, and restrictions before use.
- **Deliverable:** Source manifest and rights register.
- **Acceptance:** Every asset has provenance and a documented permitted-use basis. Restricted images are not copied into the repository.

### T3.2 — Clean and normalize metadata
- **Priority:** P1 | **Depends on:** T3.1
- **Steps:** Normalize identifiers, dates, object references, bibliographic fields, encoding, and missing-value conventions; preserve original values.
- **Deliverable:** Validated metadata table and data dictionary.
- **Acceptance:** Validation reports identify duplicates, missing required fields, and unresolved identity conflicts.

### T3.3 — Prepare image derivatives
- **Priority:** P1 | **Depends on:** T3.1, T2.2
- **Steps:** Generate reproducible crops/normalizations; retain links to originals; record transformations and parameters; do not erase informative damage or surface texture.
- **Deliverable:** Processing manifest and derivative-generation scripts.
- **Acceptance:** Every derivative maps to an original asset and can be regenerated; originals remain unchanged.

### T3.4 — Annotate graph regions and forms
- **Priority:** P1 | **Depends on:** T3.3
- **Steps:** Annotate graph locations, boundaries, visibility, damage, and uncertain segmentation; capture independent annotations for a subset.
- **Deliverable:** Geometry annotations and disagreement log.
- **Acceptance:** Quality checks pass; inter-annotator agreement is reported with the metric and its limitations.

### T3.5 — Annotate readings and evidence
- **Priority:** P1 | **Depends on:** T2.3, T2.4, T3.4
- **Steps:** Attach published readings and references; record alternatives and uncertainty; distinguish transcription from interpretation and translation.
- **Deliverable:** Reading/interpretation records with citations.
- **Acceptance:** No unsupported “ground truth” is introduced; contested readings remain multi-valued.

### T3.6 — Audit corpus quality and splits
- **Priority:** P1 | **Depends on:** T3.1–T3.5
- **Steps:** Check annotation completeness, source leakage, duplicate images, class balance, rights, and split integrity; split by artifact/source where feasible.
- **Deliverable:** Corpus quality report and split manifest.
- **Acceptance:** Near-duplicate views or fragments from the same artifact cannot leak across train/test without an explicit documented reason.

## Pilot size and composition

Target an initial **500–1,000 graph instances**, subject to lawful access and annotation capacity. Include known forms, disputed readings, unidentified forms, and damaged/partial instances. This is a planning target, not a quota that justifies low-quality labels.

## Phase exit gate
A versioned corpus snapshot can be reconstructed from its manifest, rights are documented, quality limitations are reported, and evaluation splits prevent obvious source leakage.
