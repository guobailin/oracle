# Evidence-first Methodology

## 1. Decompose the problem

Do not collapse all work into “translation.” Record these tasks separately:

1. **Detection:** locate inscriptional regions on an image.
2. **Segmentation:** isolate a graph occurrence or meaningful component.
3. **Visual description:** record strokes, structure, orientation, damage, and uncertainty.
4. **Recognition:** retrieve or rank graph-form candidates.
5. **Transcription:** represent the observed inscription, including gaps and uncertain signs.
6. **Reading:** propose a linguistic value or graph identity.
7. **Interpretation:** explain the wording and its function in context.
8. **Reconstruction:** infer missing portions or relations between fragments.
9. **Historical inference:** draw conclusions about people, events, institutions, or chronology.

A system may perform well at retrieval while remaining unable to justify a reading. Report task-specific results.

## 2. Evidence hierarchy

Keep source evidence distinct from model-generated suggestions.

- **Primary material:** artifact, authorized photograph, rubbing, excavation or catalogue record.
- **Scholarly documentation:** published facsimile, transcription, catalogue entry, edition, and commentary.
- **Comparative evidence:** occurrences of similar graph forms, parallel inscriptions, formulae, and related textual patterns.
- **Interpretive argument:** palaeographic, linguistic, archaeological, and historical reasoning.
- **AI output:** candidate matches, visual descriptions, rankings, and generated hypotheses. These are leads, not primary evidence.

Citations must point to the most precise available locator: artifact identifier, catalogue number, plate, page, graph occurrence, or stable URL.

## 3. Case workflow

1. **Intake:** assign a case ID; identify artifact, fragment, catalogue number, source, and rights.
2. **Asset verification:** confirm image identity, orientation, scale, completeness, and provenance.
3. **Observation:** describe visible marks without prematurely assigning a reading.
4. **Segmentation:** define graph boundaries and preserve alternate segmentations.
5. **Comparative retrieval:** search documented forms and parallel occurrences.
6. **Contextual analysis:** inspect syntax, divination formulae, parallel texts, and archaeological context.
7. **Hypothesis generation:** list candidate readings and the evidence each predicts.
8. **Adversarial review:** actively search for disconfirming evidence and plausible alternatives.
9. **Expert review:** obtain independent assessment where possible.
10. **Decision and versioning:** record current status, rationale, dissent, and what evidence could change the conclusion.

## 4. Hypothesis record

Every candidate should include:
- proposed graph identity and reading;
- visual features supporting the match;
- comparable occurrences with exact citations;
- linguistic and contextual fit;
- counter-evidence and alternative candidates;
- source and rights metadata;
- model/provider, exact model ID, prompt version, parameters, and timestamp if AI-assisted;
- reviewer identity or role, review date, and review status.

## 5. Uncertainty vocabulary

Use explicit statuses rather than a single uncalibrated confidence score:

- `unassessed`
- `candidate`
- `plausible`
- `contested`
- `expert_reviewed_tentative`
- `well_supported`
- `unresolved_due_to_evidence`
- `unreadable_or_lost`

These are workflow labels, not universal claims of truth. A model's self-reported confidence must never be treated as a historical fact.

## 6. Good practice

- Preserve the raw image and raw transcription.
- Mark lacunae, damage, uncertain boundaries, and editorial supplements explicitly.
- Never silently normalize an uncertain graph to a modern character.
- Keep distinct scholarly readings as separate records.
- Distinguish “not yet identified” from “not recoverable from surviving evidence.”
- Cite sources for claims; do not accept generated references without verification.
- Record negative results and failed hypotheses.

## 7. Publication standard

A public case report should make it possible for another researcher to inspect the source, reproduce the image processing, understand the alternatives, and challenge the conclusion.