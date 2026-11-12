# Pilot Dataset v0.1 — Selection and Blinding Protocol

**Status:** Candidate selection protocol; no case is admitted until source, task unit, reference status, and rights are checked.
**Target:** 30 admitted cases: 15 concealed-known recovery and 15 unresolved/disputed discovery.

## 1. Purpose
The pilot tests whether Oracle can autonomously move from visual evidence to defensible reading hypotheses. It is not a representative census of all oracle-bone writing.

## 2. Tracks and sampling quotas
### Track A — concealed-known recovery (15)
Select cases with stable, traceable published readings and inspectable source evidence. Vary graph complexity, legibility, parallel occurrences, isolated-graph versus context evidence, and source provenance. Keep reference readings and adjudication notes in a sealed answer key unavailable to the model runner.

Concealing the answer in the case package does not prove a foundation model has never seen the character, publication, or image during pretraining. Record this limitation. Where feasible, use artifact/source-held-out cases and search retrieval indexes for duplicates and near-duplicates.

### Track B — unresolved/disputed discovery (15)

| Stratum | Target | Inclusion rule |
|---|---:|---|
| U1 — graph not securely identified | 3 | Published sources explicitly leave graph unidentified or unread |
| U2 — graph-form grouping disputed | 3 | Competing graph-family or variant assignments exist |
| U3 — damaged or visually ambiguous | 3 | Physical/image damage materially affects stroke interpretation |
| U4 — reading or lexical function unresolved | 3 | Identification and lexical interpretation are not conflated |
| U5 — phrase/inscription interpretation disputed | 2 | Multiple materially different contextual readings are documented |
| U6 — fragment joining/text reconstruction | 1 | Candidate join or sequence reconstruction is uncertain |

A case may have secondary tags, but receives one primary stratum for quota accounting. If a stratum cannot be populated with adequately documented cases, leave the slot vacant and report the shortfall; do not substitute an easier case.

## 3. Unit of analysis
The primary unit is a case package. Declare whether its target is a graph occurrence, graph type, reading hypothesis, phrase/context unit, or fragment relation. Multiple images or parallels may belong to one case, but duplicates are not independent observations.

## 4. Admission gates
1. Stable source locator and access date.
2. Artifact/catalogue identifier, or explicit note that it is unavailable.
3. Exact target unit and target region, or reason coordinates cannot yet be supplied.
4. Original asset provenance and transformation history.
5. Rights/access status. Unknown rights remain unknown.
6. Reference status: established, contested, unresolved, or damaged/insufficient.
7. Bibliographic evidence for reference status and competing readings.
8. Duplicate/near-duplicate relationships and source-family links.
9. Case-specific inclusion rationale and expected difficulty.
10. Plan for hiding labels and reference readings from the autonomous run.

Cases failing a critical gate remain PROPOSED or become UNSCORABLE; they are not silently counted as model errors.

## 5. Blinding and leakage controls
- Separate public case package from restricted answer key.
- Remove readings, labels, catalogue annotations, filenames, captions, and revealing metadata from Track A inputs.
- Keep answer keys out of model-facing retrieval corpora.
- Group all views, crops, rubbings, scans, duplicate impressions, and derivatives from one artifact/source family into one split.
- Search benchmark resources and available model-facing indexes for exact and perceptual duplicates.
- Record foundation-model pretraining leakage as partially auditable unless independently established otherwise.
- Freeze dataset version, case hashes, permitted retrieval resources, model IDs, and run budget before evaluation.

## 6. Rights policy
A scholarly paper's open-access license does not automatically license underlying archival images. A dataset license does not necessarily override third-party rights. Until the rights holder and terms are confirmed, store metadata and bibliographic pointers only; do not mirror image bytes or assume commercial training rights.

- HUST-OBC: the paper reports CC BY-NC 4.0 for the dataset. Non-commercial restriction applies; audit each underlying source and current repository terms.
- OBIMD: verify authoritative dataset card, third-party image rights, and model-training permissions at asset level. Treat reuse as REVIEW_REQUIRED until confirmed.
- Xiaoxuetang: useful for graph-head/form lookup and catalogue cross-reference; public search is not a bulk-download or image-reuse license.

## 7. Selection workflow
1. Discover candidates from scholarly databases, published catalogues, and research datasets.
2. Create metadata-only candidate records with stable source locators.
3. Verify reference status from primary scholarly sources, not dataset category labels alone.
4. Inspect artifact/source relationships and deduplicate.
5. Audit rights and access terms.
6. Assign primary stratum, difficulty rationale, and admission status.
7. Freeze case package and answer key separately.
8. Run leakage audit and publish a manifest with exclusions.

## 8. Pilot reporting
Publish admitted count and shortfall by track/stratum; excluded and unscorable cases with reasons; source and rights coverage; duplicate/leakage audit method and limitations; reference quality and disagreement; and frozen dataset version/hashes.

A 30-slot template is not a 30-case dataset. Only records marked ADMITTED count toward the target.