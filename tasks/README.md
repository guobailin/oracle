# Research Work Breakdown Structure

This directory turns the 12-week research roadmap into executable work packages.

## Operating principles

1. Keep archaeological source material immutable; annotations and AI outputs are separate layers.
2. Every reading hypothesis must link to image evidence, bibliographic evidence, and a reviewer decision.
3. A model's confidence or agreement with other models is not scholarly proof.
4. Record provenance, rights, versions, prompts, model identifiers, and experiment settings.
5. Prefer a defensible negative result or abstention over an unsupported decipherment.

## Phases and dependencies

| Phase | Weeks | Focus | Exit gate |
|---|---:|---|---|
| 01 | 1–2 | Research landscape and resources | Research map, source register, gap statement |
| 02 | 3–4 | Data and annotation standards | Versioned schema, annotation guide, pilot cases |
| 03 | 5–6 | Pilot corpus | Audited corpus and split manifest |
| 04 | 7–8 | AI baselines | Reproducible baseline report |
| 05 | 9–10 | Difficult case studies | Evidence dossiers for 5–10 cases |
| 06 | 11–12 | Review and release | Expert review, benchmark, public report |

Phases 02–06 depend on the outputs of earlier phases. Phase 01 should continue to inform all later work.

## Priority

- **P0 — start first:** T1.1–T1.4, T2.1, T2.5.
- **P1 — build the research foundation:** T3.1–T3.6 and T4.1–T4.4.
- **P2 — research and release:** T5.1–T5.6 and T6.1–T6.6.

Priority is sequencing guidance, not a claim that lower-priority work is optional.

## Sprint 1: first two weeks

1. Create a source register for datasets, databases, publications, and digitized collections.
2. Define a taxonomy for unresolved problems: disputed reading, unidentified intact graph, damaged graph, and difficult inscription/context.
3. Review data access and reuse terms before downloading or redistributing anything.
4. Compare existing datasets by image quality, annotation scope, licensing, and train/test leakage risk.
5. Produce a concise gap analysis that identifies a tractable first research question.

**Sprint 1 acceptance:** every reviewed resource has a citation, access route, rights note, coverage description, and relevance assessment; the unresolved-problem taxonomy is documented; the team can explain what the project will add beyond existing databases and AI systems.

## Sprint 1 result (2026-11-11)

Desk research artifacts are committed; Phase 01 is in **REVIEW**, not DONE, because source-level sampling, rights verification, and expert validation remain open.

- [Sprint 1 report](../reports/SPRINT_01_REPORT.md)
- [Unresolved-problem taxonomy](../reports/problem_taxonomy.md)
- [Database comparison](../reports/database_comparison.csv)
- [Dataset source register](../datasets/source_register.csv)
- [Literature review](../reports/literature_review.md)
- [Research gap and proposed positioning](../reports/research_gap.md)

## Status convention

Use `TODO`, `IN_PROGRESS`, `BLOCKED`, `REVIEW`, and `DONE` for task status. Do not mark a task done until its deliverables and acceptance criteria are met.

## Task files

- [Phase 01 — Research landscape](PHASE_01_RESEARCH.md)
- [Phase 02 — Data and annotation standards](PHASE_02_SCHEMA.md)
- [Phase 03 — Pilot corpus](PHASE_03_CORPUS.md)
- [Phase 04 — AI baselines](PHASE_04_AI_BASELINE.md)
- [Phase 05 — Difficult case studies](PHASE_05_CASE_STUDIES.md)
- [Phase 06 — Expert review and release](PHASE_06_REVIEW.md)

## Cross-cutting deliverables

- `datasets/`: dataset manifests, provenance, licenses, and split definitions; never commit restricted source data.
- `experiments/`: configurations, code references, model/version details, and reproducible results.
- `cases/`: evidence dossiers for individual inscriptions or graph instances.
- `reports/`: phase reports, benchmark cards, and final findings.
