# Research Roadmap

## North-star objective

Improve the quality, speed, reproducibility, and auditability of research on difficult Oracle Bone Script inscriptions. The near-term deliverable is not an unsupported promise to translate every remaining sign; it is a traceable research system and a set of independently reviewable case studies.

## Workstreams

| Workstream | Deliverable | Key question |
|---|---|---|
| Corpus and rights | Source registry and pilot corpus | What can we lawfully access and reuse? |
| Image understanding | Detection, segmentation, visual descriptors | What is actually visible on the artifact? |
| Graph retrieval | Similar-form search and candidate ranking | Which documented forms are comparable? |
| Linguistic context | Parallel-text and formula retrieval | Which readings fit the inscriptional context? |
| Hypothesis ledger | Competing readings with evidence | Why should one interpretation be preferred? |
| Evaluation | Leakage-resistant benchmark and expert review | Does the system improve on baselines? |

## First 90 days

### Weeks 1–2: landscape and source audit
- Review major corpora, databases, publications, and recent AI research.
- Record access conditions, rights holder, license, attribution, and redistribution status.
- Identify overlapping projects and avoid duplicating existing databases.

### Weeks 3–4: schema and case selection
- Finalize artifact, fragment, image, graph-occurrence, reading, and citation records.
- Select a small set of cases with strong source documentation.
- Separate known readings, disputed readings, damaged signs, and genuinely unresolved cases.

### Weeks 5–6: pilot corpus
- Build a small, rights-cleared dataset.
- Keep original images immutable; version every crop, enhancement, and annotation.
- Obtain at least two independent annotations for a subset.

### Weeks 7–8: baseline systems
- Establish visual similarity retrieval and OCR/recognition baselines.
- Compare classical computer vision, open models, and frontier multimodal models.
- Track exact model identifiers, prompts, parameters, latency, and cost.

### Weeks 9–10: evidence dossiers
- Produce case dossiers with image observations, parallels, candidate readings, and counter-evidence.
- Use retrieval-augmented analysis to surface sources, not to manufacture citations.

### Weeks 11–12: independent review
- Ask qualified readers to assess a blinded sample.
- Record disagreements, corrections, abstentions, and unresolved cases.
- Publish a transparent pilot report and revise the roadmap.

## Success measures

- **Provenance completeness:** percentage of records with verifiable source and rights metadata.
- **Annotation agreement:** agreement by task and by graph, not one aggregate score alone.
- **Retrieval quality:** Recall@k, mAP, and nDCG for comparable forms.
- **Recognition quality:** top-k accuracy, macro-F1, and open-set performance.
- **Transcription quality:** CER/WER where a defensible reference transcription exists.
- **Calibration:** whether confidence estimates match observed correctness; quality of abstention.
- **Scholarly utility:** blinded expert assessment of evidence quality and time saved.
- **Reproducibility:** proportion of results reproducible from versioned data, code, and model metadata.

## Risks and mitigations

- **Data leakage:** split by physical artifact or source, not random image crops.
- **False certainty:** preserve alternatives and require evidence-backed review.
- **Rights uncertainty:** do not scrape or redistribute restricted resources.
- **Model drift:** pin model IDs and rerun a stable benchmark when providers change models.
- **Evaluation bias:** distinguish agreement with published readings from genuine correctness; published readings can themselves be contested.
- **Overclaiming:** report unresolved outcomes and failure cases.

## Decision gates

Do not scale corpus ingestion until rights are clear. Do not claim recognition progress until leakage-resistant baselines exist. Do not label a new reading as established without qualified review and a transparent evidence dossier.