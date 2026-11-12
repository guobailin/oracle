# Pilot Source Register

Discovery resources are not automatically licensed datasets. Record access and reuse rights separately for metadata, image bytes, annotations, model training, and redistribution.

| Resource | Role | Established facts | Restriction / action | Link |
|---|---|---|---|---|
| HUST-OBC | Candidate source for known/unknown graph image examples | Paper reports 140,053 images: 77,064 in 1,588 deciphered categories and 62,989 in 9,411 undeciphered categories | Paper reports CC BY-NC 4.0; audit underlying source rights and current repository terms. Category count is not a ground-truth count of unique unknown graphs. | https://github.com/Pengjie-W/HUST-OBC |
| OBIMD | Context-rich images, graph annotations, sentence/context units | Paper reports 10,077 images, 93,652 annotated characters, 21,667 missing positions, and 21,941 sentence units | Confirm authoritative dataset card, license, third-party image rights, and model-training permissions before copying or training. Metadata-only discovery until cleared. | https://huggingface.co/datasets/BlueHan/OBIMD |
| Xiaoxuetang Oracle Bone Script Database | Cross-reference graph heads, forms, Heji numbers, old catalogue references, and groups | Official introduction reports 2,548 graph heads and 24,701 forms in its 2026 update; supports searches by graph head, form, page, Heji number, old catalogue, and group | Public search does not grant bulk extraction or image reuse rights. Use as manually inspected cross-reference unless terms authorize more. | https://xiaoxue.iis.sinica.edu.tw/jiaguwen/ |
| Open-Oracle | Literature and benchmark discovery index | Maintains a task-oriented index of papers, datasets, code, and benchmarks | Secondary index only; verify every candidate at original paper, repository, and data source. | https://github.com/Yuliang-Liu/Open-Oracle |
| Published catalogues and editions | Establish reference status and contested readings | Provide exact plate, inscription, page, and scholarly reading references | Access may be print/subscription-based; record edition and exact locator. Do not infer rights to digitized scans. | Record per candidate |


| Guoxuedashi character evolution entry | Cross-reference for specific known graph occurrences | The entry for 休 lists graph examples including 乙4779（合8167）, 乙484（合21722）, and 前5.26.2（合8154）, and describes the graph composition and reading | Secondary reference; use only to locate primary catalogue/database records. No image reuse rights inferred. | https://www.guoxuedashi.com/zixing/yanbian/1398vg/ |
| Xiaoxuetang teaching example (Education Bureau PDF) | Independent locator for the same 休 graph records | The example screenshot lists 21 graph records, including 甲55/合8163, 乙484/合21722, 乙4779/合8167, 前5.26.2/合8154, and associated group labels | Educational example is a locator, not a substitute for the underlying record or its image rights. | https://www.edb.gov.hk/attachment/tc/edu-system/primary-secondary/applicable-to-primary-secondary/it-in-edu/rtc/201920/EI0020190338/CC-190-Chi-Pri-PPT-S2.pdf |
| Hanyudian character entry: 休 | Secondary cross-check of the same graph-head identification | Lists 乙4779/合8167, 乙484/合21722, and 前5.26.2/合8154 among 休 graph forms | Secondary lexicographic source; do not treat as independent primary evidence if it derives from the same catalogue tradition. | https://www.zdic.net/hant/休 |

## First Track A candidate discovery (not admitted)
Three record-level candidates have been identified for the graph head 休:
- 乙4779 / 合集8167 / 賓組
- 乙484 / 合集21722 / 子組
- 前5.26.2 / 合集8154 / 賓組

These are **three graph occurrences of one known graph head**, not three independent decipherments or three independent graph classes. They are useful for testing whether the system can recover a known reading across distinct artifact occurrences, but they provide only one graph-type family for evaluation. All remain PROPOSED: exact image asset URLs and hashes, source-level image rights, full context packages, duplicate relationships, and model pretraining/retrieval leakage have not been audited. The public repository intentionally does not store a hidden answer key; however, the source records are publicly searchable, so these candidates must not be treated as leakage-resistant blind cases until a frozen, independently sourced image package and sealed key are prepared.

## Required rights dimensions
- metadata viewing/access;
- image viewing;
- local research copy;
- model training / embedding / indexing;
- derivative image publication;
- redistribution;
- commercial use.

Use unknown until a source explicitly establishes permission. The paper license and underlying artifact image license may differ.