# Phase 00 — Autonomous Decipherment Foundation

**Status:** IN_PROGRESS  
**Objective:** Turn Oracle's autonomous decipherment mission into testable definitions, a leakage-resistant pilot, and a reproducible evaluation protocol.

## T0.1 — Define decipherment success criteria

**Status:** REVIEW  
**Deliverable:** [Decipherment Success Criteria](../docs/DECIPHERMENT_SUCCESS_CRITERIA.md)

Acceptance:
- [x] Distinguish artifacts, images, graph occurrences, graph types, hypotheses, and context units.
- [x] Define outcome classes: known recovery, new hypothesis, evidence-supported, independently validated, abstention, unresolved, incorrect, and unscorable.
- [x] Define case-level autonomy and what counts as human intervention.
- [x] Define evidence dossier requirements and independent validation gates.
- [x] Separate evidence quality, confidence estimates, and outcome status.
- [x] Define blind-known, unresolved-discovery, and end-to-end autonomy tracks.
- [x] Define core metrics with denominators and safeguards against inflated claims.
- [ ] Review the protocol against selected pilot cases and revise ambiguous rules.
- [ ] Freeze v1.0 after pilot inventory and evaluation design are audited.

**Exit gate:** The protocol can classify pilot outcomes consistently, prevents candidate generation from being counted as decipherment, and specifies how an autonomous run is separated from post-run independent validation.

## T0.2 — Build the pilot case inventory

**Status:** TODO  
**Target:** Initial inventory of 30 candidate cases, subject to source/rights audit.

- [ ] 15 concealed-known cases with defensible reference readings.
- [ ] 15 unresolved/disputed/damaged cases, stratified by problem type.
- [ ] Record artifact, image, occurrence, context, source locator, reference status, rights, and duplicate relationships.
- [ ] Identify training/retrieval leakage risks and freeze split rules.
- [ ] Mark cases unscorable where source quality or reference status is inadequate.

**Exit gate:** Every included case has traceable provenance, rights/access notes, a declared task unit, and a documented reason for inclusion.

## T0.3 — Implement confidence and uncertainty records

**Status:** TODO

- [ ] Define operational rubrics for visual, structural, semantic, historical, and contextual evidence.
- [ ] Keep dimension-level scores separate; do not average them into an overall probability.
- [ ] Keep overall calibrated probability null until supported by held-out calibration data.
- [ ] Define abstention and selective-risk reporting.
- [ ] Version the schema and calibration dataset.

**Exit gate:** Every system output can expose evidence, uncertainty, alternatives, and abstention in a machine-readable form.

## T0.4 — Establish a minimal autonomous baseline

**Status:** TODO

- [ ] Build a deterministic case-package loader and provenance checks.
- [ ] Connect permitted image/graph retrieval and context retrieval.
- [ ] Generate competing hypotheses and explicit counter-evidence searches.
- [ ] Enforce a fixed run budget and log prompts, model IDs, tools, versions, and costs.
- [ ] Prohibit case-specific human intervention after the run begins.

**Exit gate:** A frozen case can be processed end-to-end and yields a complete, reproducible dossier or a justified abstention.

## T0.5 — Run and report the pilot

**Status:** TODO

- [ ] Run Track A blind recovery and Track B unresolved discovery separately.
- [ ] Run the autonomy track with no case-specific human intervention.
- [ ] Preserve raw outputs and run logs.
- [ ] Independently adjudicate results after autonomous runs are frozen.
- [ ] Report recovery, validated new readings, false discoveries, abstention, calibration, evidence completeness, and cost.

**Exit gate:** Publish a reproducible pilot report with failures, exclusions, limitations, and no unsupported decipherment claims.

## Operating rule

Do not train a bespoke model or scale corpus ingestion merely to create activity. First demonstrate that the protocol, data split, and minimal baseline can distinguish genuine progress from leakage, imitation, and plausible-sounding hallucination.
