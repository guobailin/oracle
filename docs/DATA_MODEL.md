# Data Model and Annotation Schema

## Core entities

| Entity | Purpose |
|---|---|
| `Source` | Database, publication, collection, excavation record, or website |
| `Artifact` | Physical object or inscribed bone/shell |
| `Fragment` | A physical fragment and its known relationships |
| `ImageAsset` | Photograph, rubbing, scan, crop, or derived image |
| `Inscription` | Inscriptional sequence or catalogue unit |
| `GlyphOccurrence` | A graph occurrence at a specific location |
| `GraphForm` | Abstract/documented graph form and variants |
| `Reading` | Proposed phonetic/linguistic reading or identification |
| `Interpretation` | Contextual interpretation of an inscription |
| `Citation` | Precise bibliographic or catalogue locator |
| `Hypothesis` | A claim with supporting and opposing evidence |
| `Annotation` | Human or machine annotation with provenance |
| `Experiment` | Reproducible model or algorithm run |

## Provenance fields

Every externally sourced record should capture, where available:

- `source_id`, `source_title`, `source_url`
- `catalogue_identifier`, `artifact_identifier`
- `accessed_at`
- `rights_holder`, `license`
- `redistribution_allowed`, `training_use_allowed`
- `attribution_text`, `access_conditions`, `notes`

Unknown rights must be represented as unknown, not assumed permissive.

## Example glyph occurrence

```json
{
  "id": "case-0001-glyph-03",
  "artifact_id": "artifact-id",
  "image_asset_id": "asset-id",
  "sequence_index": 3,
  "region": {
    "coordinate_system": "normalized_0_to_1",
    "polygon": [[0.12, 0.18], [0.31, 0.18], [0.32, 0.39], [0.13, 0.40]]
  },
  "visual_observation": "Description of visible strokes and structure; no reading asserted.",
  "damage_status": "partially_damaged",
  "candidate_graph_forms": [],
  "candidate_readings": [],
  "annotation_status": "needs_review",
  "annotator_type": "human",
  "source_citation_ids": [],
  "rights_status": "review_required"
}
```

## Controlled values

Suggested `damage_status`:
- `intact`, `partially_damaged`, `severely_damaged`, `lacuna`, `uncertain`

Suggested `annotation_status`:
- `unannotated`, `draft`, `needs_review`, `reviewed`, `disputed`

Suggested `rights_status`:
- `open`, `restricted`, `permission_required`, `unknown`

Suggested hypothesis status is defined in the methodology document.

## Versioning rules

- Never overwrite a scholarly reading; create a new version or a new competing record.
- Preserve original text and diplomatic transcription separately from normalized forms.
- Mark editorial supplements and uncertain signs explicitly.
- Store coordinates relative to a named image asset and coordinate system.
- Link every model annotation to an experiment record.
- Keep human corrections and machine outputs distinguishable.

## Interoperability

Use stable IDs and documented schemas. Export formats should include JSONL for records and CSV for simple tabular views. Do not export third-party image bytes unless redistribution is explicitly permitted.