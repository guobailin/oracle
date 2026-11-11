# Oracle — AI-assisted Oracle Bone Script Research

**Mission:** build an open, evidence-grounded research workflow that uses modern AI and computational methods to help scholars investigate difficult and undeciphered Oracle Bone Script (OBS) inscriptions.

> **AI proposes; evidence constrains; scholars review.**

This project does not assume that current AI can translate all undeciphered inscriptions. “Unsolved” cases differ: a sign may be damaged or incomplete, its shape may be unknown, its reading may be disputed, or the inscription may remain unclear even when individual graphs are recognized. We keep these problems separate.

## Research pillars

1. **Corpus & provenance** — trace every image, rubbing, transcription, catalogue record, rights statement, and scholarly source.
2. **Visual understanding** — detect inscriptions, segment graph occurrences, describe morphology, and retrieve comparable forms.
3. **Graph identification** — rank candidate graphs and readings without silently forcing uncertain signs into known characters.
4. **Text and context** — compare parallel divinations, syntax, formulae, historical and archaeological context.
5. **Fragment relations** — investigate joins, duplicates, and relations between fragments with explicit evidence.
6. **Evaluation** — benchmark AI against documented scholarly readings and expert review, with uncertainty and abstention measured.

## Principles

- Preserve original assets; all preprocessing outputs are derived, versioned assets.
- Separate visual observation, transcription, reading, interpretation, and historical inference.
- Record competing hypotheses and counter-evidence.
- Never treat model confidence as historical truth.
- Respect source licenses. Public accessibility does not imply permission to download, train on, or redistribute data.
- Code licensing does not grant rights to third-party images or corpora.

## Repository map

- `docs/ROADMAP.md` — phased research plan
- `docs/METHODOLOGY.md` — evidence-first decipherment workflow
- `docs/TECHNICAL_ARCHITECTURE.md` — AI and data architecture
- `docs/DATA_MODEL.md` — provenance and annotation schema
- `docs/BENCHMARK.md` — evaluation protocol
- `docs/RESOURCES.md` — datasets, databases, papers, and rights notes
- `docs/CONTRIBUTING.md` — contribution and review rules
- `cases/README.md` — template for individual difficult cases

## First milestone

Create a legally usable pilot corpus with traceable provenance; define an annotation schema; establish retrieval and recognition baselines; then publish a small number of carefully documented case studies for independent scholarly review.

## Suggested licensing

The repository's original code may use MIT. Original documentation may use CC BY 4.0. Third-party datasets, photographs, rubbings, and transcriptions retain their own licenses and terms. Add explicit per-resource rights metadata before reuse.

## Status

Research framework initialized. No claim is made that the project has solved any undeciphered inscription.