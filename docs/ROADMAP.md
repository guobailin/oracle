# Research Roadmap

## North-star objective

Maximize the number of genuinely unresolved Oracle Bone Script readings that can be proposed and substantiated autonomously, while minimizing case-specific human intervention.

The primary outcome is **Autonomous Validated New Readings**: new readings that pass a documented validation protocol without case-specific human intervention during the autonomous run. Candidate generation, known-answer recovery, model consensus, and high confidence scores alone do not count as new decipherments. Post-run independent validation remains separate from operational human intervention.

## Phase 00 — Autonomous decipherment foundation

- Define outcome classes, autonomy rules, evidence requirements, validation gates, and core metrics.
- Build a small, rights-audited pilot inventory with concealed-known and unresolved tracks.
- Define confidence and abstention records; do not report an overall calibrated probability before calibration data exists.
- Establish a minimal autonomous baseline with complete run logs.
- Run a frozen pilot and publish errors, exclusions, false discoveries, abstentions, and cost.

**Exit gate:** The protocol and pilot can distinguish candidate generation from validated decipherment, prevent known-answer leakage, and measure case-level autonomy.

See [Phase 00 tasks](../tasks/PHASE_00_FOUNDATION.md) and [success criteria](DECIPHERMENT_SUCCESS_CRITERIA.md).

## Workstreams after Phase 00

| Workstream | Deliverable | Key question |
|---|---|---|
| Corpus and rights | Source registry and pilot corpus | What can we lawfully access and reuse? |
| Discovery and image understanding | Detection, segmentation, visual descriptors | What graph occurrences exist, and what is actually visible? |
| Graph retrieval | Similar-form search and candidate ranking | Which documented forms are comparable? |
| Evidence reasoning | Parallel-text and formula retrieval | Which readings survive contextual tests? |
| Hypothesis ledger | Competing readings with evidence | Why should one interpretation be preferred? |
| Adversarial validation | Counter-evidence and holdout tests | What could falsify the candidate? |
| Autonomous evaluation | Leakage-resistant benchmark and run logs | Does the system solve cases without case-specific intervention? |

## First 90 days (revised sequencing)

### Weeks 1–2: foundation and pilot design
- Complete Phase 00 protocol and case inventory.
- Audit provenance, access, rights, reference quality, and duplicate relationships.
- Freeze artifact/source-level splits and permitted retrieval resources.

### Weeks 3–4: schema and pilot corpus
- Finalize artifact, fragment, image, graph-occurrence, reading, evidence, and run records.
- Build a small, rights-cleared dataset.
- Keep original images immutable; version every crop, enhancement, and annotation.

### Weeks 5–6: minimal autonomous baseline
- Establish visual similarity retrieval and context retrieval.
- Compare classical methods, open models, and frontier multimodal models.
- Generate competing hypotheses and explicit counter-evidence searches.
- Track exact model identifiers, prompts, parameters, latency, and cost.

### Weeks 7–8: blind and unresolved pilot
- Run concealed-known recovery and unresolved-case discovery as separate tracks.
- Freeze autonomous outputs before any external adjudication.
- Measure abstention, calibration where supportable, leakage, and failure categories.

### Weeks 9–10: improve the bottleneck
- Use pilot errors to prioritize data, retrieval, visual analysis, or reasoning improvements.
- Do not add agents or train bespoke models unless ablation shows a measurable benefit.

### Weeks 11–12: independent validation and release
- Independently assess frozen evidence dossiers after autonomous runs.
- Publish validated new readings separately from hypotheses and known-answer recovery.
- Release only assets and annotations whose rights permit release.

## Core success measures

- **Autonomous Validated New Readings:** primary north-star metric.
- **False Discovery Rate:** incorrect accepted readings / all accepted readings with adjudicable outcomes.
- **Autonomous Resolution Rate:** autonomous validated resolutions / eligible cases.
- **Known-case Recovery:** concealed-known blind performance, reported separately.
- **Calibration and selective risk:** probability reliability and error among answered cases as coverage changes.
- **Evidence completeness:** share of required provenance and evidence fields that are verifiable.
- **Cost per validated reading:** attributable compute/tool cost divided by validated new readings, when non-zero.
- **Reproducibility:** results reproducible from versioned data, code, models, and run metadata.

See [Decipherment Success Criteria](DECIPHERMENT_SUCCESS_CRITERIA.md) for operational definitions.

## Risks and mitigations

- **Data leakage:** split by artifact/source/context and exclude near duplicates from retrieval.
- **False certainty:** preserve alternatives, counter-evidence, and abstention.
- **Rights uncertainty:** do not scrape or redistribute restricted resources.
- **Model drift:** pin model IDs and rerun stable benchmarks when providers change models.
- **Reference uncertainty:** separate agreement with published readings from genuine correctness.
- **Overclaiming:** report unresolved outcomes, false discoveries, and failures.

## Decision gates

Do not scale corpus ingestion until rights are clear. Do not claim new decipherments based on model confidence alone. Do not label a new reading as independently validated until the documented validation gates are passed. Do not scale to complex multi-agent orchestration before a simpler baseline demonstrates what capability is missing.
