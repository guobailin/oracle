# Oracle — Autonomous Oracle Bone Script Decipherment

**Mission:** maximize the number of genuinely unresolved Oracle Bone Script readings that can be proposed and substantiated autonomously, while minimizing case-specific human intervention.

> **Autonomy proposes; evidence constrains; independent validation establishes.**

Oracle is designed to discover graph forms, generate competing reading hypotheses, retrieve supporting and contradicting evidence, quantify uncertainty, and test its own hypotheses. It must be allowed to abstain. Candidate generation, model consensus, or a high confidence score alone never counts as decipherment.

## North-star outcome

**Autonomous Validated New Readings:** new readings that pass the documented validation protocol without case-specific human intervention during the autonomous run.

Report this together with false-discovery risk, abstention, evidence completeness, calibration, and cost. Known-answer blind recovery measures capability but is not a new decipherment. Post-run independent validation is distinct from human intervention during system operation.

## Research pillars

1. **Corpus & provenance** — trace every artifact, image, rubbing, transcription, catalogue record, rights statement, and scholarly source.
2. **Discovery & visual understanding** — discover graph occurrences, cluster forms, segment graphs, and identify unknown or damaged cases.
3. **Graph and reading hypotheses** — rank candidates while preserving alternatives and uncertainty.
4. **Evidence reasoning** — compare parallel inscriptions, syntax, formulae, historical and archaeological context.
5. **Adversarial validation** — search for counter-evidence, test on independent holdouts, and calibrate uncertainty.
6. **Autonomous evaluation** — measure new validated readings, abstention, false discoveries, autonomy, reproducibility, and cost.

## Non-negotiable principles

- Separate visual observation, graph identification, reading, interpretation, and historical inference.
- Preserve competing hypotheses and counter-evidence.
- Never treat model confidence or multi-model agreement as historical truth.
- Do not count a candidate as a decipherment.
- Allow explicit abstention when evidence is inadequate.
- Keep autonomous operation separate from post-run independent validation.
- Preserve original assets; version all derived assets and transformations.
- Respect source licenses. Public accessibility does not imply permission to download, train on, or redistribute data.
- Code licensing does not grant rights to third-party images or corpora.

## Repository map

- docs/DECIPHERMENT_SUCCESS_CRITERIA.md — outcome definitions, autonomy, evidence gates, and metrics
- docs/ROADMAP.md — phased research plan
- docs/METHODOLOGY.md — evidence-first decipherment workflow
- docs/TECHNICAL_ARCHITECTURE.md — AI and data architecture
- docs/DATA_MODEL.md — provenance and annotation schema
- docs/BENCHMARK.md — evaluation protocol
- docs/RESOURCES.md — datasets, databases, papers, and rights notes
- tasks/PHASE_00_FOUNDATION.md — autonomous decipherment foundation work packages
- cases/README.md — template for individual difficult cases

## Current milestone

Phase 00 establishes measurable success criteria, a leakage-resistant pilot inventory, confidence/uncertainty records, and a minimal autonomous baseline. No claim is made that Oracle has solved any undeciphered inscription.

## Suggested licensing

The repository's original code may use MIT. Original documentation may use CC BY 4.0. Third-party datasets, photographs, rubbings, and transcriptions retain their own licenses and terms. Add explicit per-resource rights metadata before reuse.
