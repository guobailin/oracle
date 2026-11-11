# Decipherment Success Criteria

**Status:** Draft v0.1 — ready for pilot operationalization  
**Scope:** Defines what Oracle may count as a decipherment, how autonomy is measured, and what evidence is required before a result is called validated.

## 1. Mission-level objective

Oracle aims to maximize the number of genuinely unresolved Oracle Bone Script graph readings that can be proposed and substantiated autonomously, while minimizing human intervention.

The system must not optimize for the number of generated answers. It must optimize for new, independently testable, evidence-grounded readings subject to a controlled false-discovery rate.

## 2. Unit of evaluation

Do not mix these units:
- **Artifact:** a physical bone, shell, or fragment.
- **Image:** a photograph, scan, or rubbing of an artifact.
- **Graph occurrence:** one visible instance at a specific location on an artifact/image.
- **Graph type:** a proposed grouping of visually related occurrences.
- **Reading hypothesis:** a proposed identification, pronunciation, lexical value, or functional interpretation.
- **Inscription/context unit:** the surrounding sequence and its archaeological/linguistic context.

Every benchmark result must name its unit. Counts of graph types, occurrences, images, and missing positions are not interchangeable.

## 3. Outcome classes

Each evaluated case receives exactly one primary outcome:

| Outcome | Definition | Counts as a decipherment? |
|---|---|---:|
| KNOWN_RECOVERED | Correctly recovers a reference reading hidden from the system | No; measures capability |
| NEW_HYPOTHESIS | Produces a non-trivial candidate for an unresolved case | No |
| EVIDENCE_SUPPORTED | Candidate survives documented support and contradiction tests, but remains unconfirmed | Not yet |
| INDEPENDENTLY_VALIDATED | Candidate passes the validation protocol in §6, with no unresolved critical contradiction | Yes, provisionally |
| ABSTAINED | Explicitly declines to decide because evidence is insufficient or conflicting | No; may be correct behavior |
| UNRESOLVED | No defensible candidate is produced | No |
| INCORRECT | Candidate conflicts with the hidden reference or fails decisive tests | No |
| UNSCORABLE | Source, image quality, rights, or reference uncertainty prevents fair evaluation | Excluded from accuracy denominators; reported separately |

A candidate is not a decipherment merely because it resembles a modern character, receives a high model score, or is repeated by multiple models.

## 4. What counts as autonomous

A run is autonomous only when, after the case package and permitted resources are frozen:

1. No person selects or edits the target crop, graph segmentation, candidate list, prompt, retrieved evidence, or final answer for that case.
2. No person supplies case-specific hints, corrections, or intermediate decisions.
3. The system itself performs discovery/retrieval, generates competing hypotheses, searches for supporting and contradicting evidence, scores uncertainty, and chooses an outcome or abstains.
4. All model calls, tools, retrieved records, prompts, parameters, transformations, and outputs are logged.
5. The run terminates under a predeclared compute/time/cost budget.

Human-authored general software, schemas, and frozen evaluation rules do not by themselves invalidate autonomy. Any case-specific intervention does. Report intervention categories and counts rather than hiding them.

**Autonomous operation is not the same as scientific validation.** Independent external validation may occur after the autonomous run and must not feed back into that run.

## 5. Evidence requirements

Every NEW_HYPOTHESIS, EVIDENCE_SUPPORTED, or INDEPENDENTLY_VALIDATED result must include:
- Stable identifiers for artifact, image, graph occurrence, and context unit where available.
- Source locator, provenance, rights status, and image transformation history.
- A description of visible features separated from inferred interpretation.
- At least one candidate reading and meaningful alternatives, or an explicit reason alternatives could not be generated.
- Supporting evidence with exact source locators.
- Contradicting evidence and failed tests; an empty list must state what contradiction searches were run.
- The reasoning chain linking observations to the hypothesis.
- Model/tool versions, prompts, parameters, retrieval index and corpus versions.
- Dimension-level uncertainty and a calibrated probability only when calibration is supported by suitable held-out data.

Evidence must be traceable to source records. Model-generated statements, agreement among models, and similarity scores are not independent historical evidence.

## 6. Validation protocol for a new reading

A new reading may be labelled INDEPENDENTLY_VALIDATED only when all applicable gates pass:

1. **Source integrity:** the underlying artifact/image and provenance are sufficiently documented; rights permit the relevant research use.
2. **Visual adequacy:** the proposed graph is not an artefact of damage, imaging, cropping, enhancement, or segmentation.
3. **Discriminative explanation:** the hypothesis explains the observed form better than serious alternatives and identifies which features distinguish them.
4. **Contextual tests:** it is tested against relevant inscriptional contexts and parallel occurrences, without counting duplicated impressions as independent evidence.
5. **Diachronic/linguistic tests:** claimed phonetic, semantic, structural, or historical relationships are explicit and consistent with the evidence invoked.
6. **Adversarial search:** the system searches for counterexamples and reports contradictions, not only confirming examples.
7. **Independent holdout:** the hypothesis is tested on evidence not used to generate or select it, such as held-out occurrences, artifacts, contexts, or sources. The split unit and independence rationale are recorded.
8. **Reference adjudication:** where no objective ground truth exists, the result remains provisional until an independent validation process, separate from the generating run, assesses the dossier. The validation source, protocol, disagreements, and date are recorded.

If a gate is inapplicable, explain why. If a critical gate fails, do not use the validated label.

## 7. Confidence: probability, evidence quality, and status are distinct

Keep three concepts separate:
- **Evidence quality:** provenance, image quality, source reliability, independence, and completeness.
- **Confidence estimate:** a probability-like estimate of correctness, calibrated on held-out cases with defensible labels.
- **Outcome status:** the categorical state in §3, determined by validation gates as well as evidence.

Do not calculate an overall confidence by taking an unvalidated arithmetic mean of visual, structural, semantic, historical, and contextual scores. These dimensions may be dependent and may measure different things.

For each dimension, record the score, its operational definition, evidence references, model/version, and whether the score is calibrated. The overall calibrated probability must remain null until calibration has been demonstrated on an appropriate held-out set. Report calibration curves, Brier score or log loss, and coverage-versus-risk for abstention where sample size permits.

A high confidence score cannot override a failed validation gate. INDEPENDENTLY_VALIDATED is not synonymous with confidence >= 0.95.

## 8. Benchmark design

Maintain separate evaluation tracks.

### Track A — concealed-known blind recovery
- Use cases with defensible published readings.
- Hide readings and prevent target leakage through training data, prompts, retrieval indexes, duplicate images, and near-duplicate artifacts.
- Split by physical artifact/source/context as appropriate, never by random crops alone.
- Measure top-k recovery, evidence quality, calibration, abstention, and cost.
- Report contested or weak reference readings separately.

This track measures recovery of known scholarship; it does not prove discovery of new knowledge.

### Track B — unresolved-case discovery
- Include genuinely unresolved, disputed, damaged, and contextually difficult cases as separate strata.
- Freeze case packages and evaluation budgets before runs.
- Record candidate novelty against a dated literature/database snapshot.
- Score evidence quality, discriminative power, counter-evidence handling, holdout predictions, and abstention.
- Do not claim correctness solely from model confidence or internal consensus.

### Track C — autonomous end-to-end operation
- Measure the proportion of cases completed without case-specific human intervention.
- Record intervention events, tool failures, runtime, token/compute usage, and cost.
- Report autonomous resolution separately from autonomous abstention and autonomous failure.

## 9. Core metrics

| Metric | Definition |
|---|---|
| Validated New Readings (VNR) | Count of new reading hypotheses that pass §6 |
| Autonomous Validated New Readings (AVNR) | VNR completed without case-specific human intervention |
| Autonomous Resolution Rate | Autonomous validated resolutions / eligible cases |
| False Discovery Rate (FDR) | Incorrect accepted readings / all accepted readings with adjudicable outcomes |
| Known-case Recovery | Recovery performance on Track A, with exact split and reference quality |
| Calibration | Agreement between predicted probabilities and observed outcomes |
| Selective Risk | Error rate among cases the system chooses to answer, as coverage changes |
| Evidence Completeness | Share of required evidence/provenance fields present and verifiable |
| Cost per Validated Reading | Total attributable compute/tool cost / VNR; report when VNR > 0 |
| Novelty Rate | Share of candidates not found in the frozen reference snapshot; novelty is not correctness |

Always publish denominators, confidence intervals where feasible, exclusions, and error categories. If no new reading is validated, report zero rather than substituting candidate counts.

## 10. Pilot acceptance rules

The initial pilot is a protocol test, not a claim of archaeological breakthrough.
- Track A and Track B must be reported separately.
- The system must produce machine-readable case dossiers and a complete run log.
- The system must be allowed to abstain.
- No case-specific human intervention is permitted during the autonomous run; post-run independent adjudication is logged separately.
- Any leakage, rights violation, untraceable evidence, or hidden intervention invalidates the affected result.
- Pilot thresholds for accuracy, calibration, autonomy, and cost must be set only after the case inventory, reference quality, and baseline difficulty are audited. Do not invent thresholds before that audit.

## 11. Non-goals and safeguards

- Do not equate character recognition with decipherment.
- Do not equate a generated modern-form analogue with a lexical reading.
- Do not equate model consensus with independent corroboration.
- Do not equate novelty with truth.
- Do not silently turn damaged or unscorable cases into model failures.
- Do not claim that all unknown graphs are decipherable from currently available evidence.

## 12. Decision rule

Oracle's north-star result is the number of new, independently validated readings achieved autonomously, reported alongside false-discovery risk, abstention, evidence completeness, and cost.

When evidence is insufficient, abstention is a successful safety behavior—not a failure to produce text.
