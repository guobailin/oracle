# Phase 02 — Data model and annotation standards

**Window:** Weeks 3–4  
**Goal:** Define a versioned, auditable representation of source objects, graph instances, readings, interpretations, and AI hypotheses.  
**Status:** TODO

## Work packages

### T2.1 — Finalize the data schema
- **Priority:** P0 | **Depends on:** Phase 01
- **Steps:** Review `docs/DATA_MODEL.md`; define identifiers, required/optional fields, relationships, controlled vocabularies, and versioning rules.
- **Deliverable:** Versioned schema specification and example records.
- **Acceptance:** A source image, artifact, inscription, graph occurrence, scholarly reading, and AI hypothesis can be represented without conflating them.

### T2.2 — Define image annotation guidelines
- **Priority:** P1 | **Depends on:** T2.1
- **Steps:** Specify image orientation, crop provenance, region boundaries, uncertain/damaged regions, overlapping marks, scale, and annotation geometry format.
- **Deliverable:** `docs/ANNOTATION_GUIDE.md`
- **Acceptance:** Two annotators can independently annotate a sample and resolve disagreements using documented rules.

### T2.3 — Define paleographic and reading labels
- **Priority:** P1 | **Depends on:** T2.1
- **Steps:** Separate visible-form transcription, normalized graph identity, proposed reading, phonetic/semantic interpretation, and inscription translation; allow multiple competing readings.
- **Deliverable:** Label vocabulary and annotated examples.
- **Acceptance:** Unknown, damaged, disputed, and illegible are distinct states; uncertainty is explicit and never silently converted to a single label.

### T2.4 — Define evidence and provenance rules
- **Priority:** P1 | **Depends on:** T2.1, T2.3
- **Steps:** Specify source citations, page/plate/object identifiers, image rights, annotator identity or pseudonym, timestamp, tool/model version, and change history.
- **Deliverable:** Evidence/provenance policy.
- **Acceptance:** Every assertion can be traced to a source or explicitly marked as an unverified hypothesis.

### T2.5 — Select pilot cases
- **Priority:** P0 | **Depends on:** T1.6, T2.1
- **Steps:** Select representative graph instances and inscriptions across known, disputed, unidentified, and damaged classes; assess image quality and evidence availability.
- **Deliverable:** Pilot case register with selection rationale.
- **Acceptance:** Cases are diverse, legally accessible, citable, and feasible to annotate; selection is not biased toward easy examples only.

### T2.6 — Establish review and adjudication
- **Priority:** P1 | **Depends on:** T2.2–T2.5
- **Steps:** Define independent annotation, disagreement logging, adjudication, expert review, and correction workflow.
- **Deliverable:** Review protocol.
- **Acceptance:** Disagreement is preserved in the data; adjudication records who decided, on what evidence, and when.

## Required separation of layers

1. **Source layer:** immutable artifact metadata and original image/source reference.
2. **Scholarly annotation layer:** human-authored segmentation, transcription, readings, citations, and disagreements.
3. **Research output layer:** model predictions, ranked candidates, prompts, confidence estimates, and hypotheses.

AI output must never overwrite source material or silently replace scholarly annotations.

## Phase exit gate
Schema, annotation guide, evidence policy, pilot selection, and review workflow are versioned and tested on sample records.
