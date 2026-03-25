# IQVIA ChannelDynamics – RAG corpus package

## What this package is
This package converts the source workbook **IQVIA CD Metrics  Measures Description.xlsx** into a first-pass, RAG-ready documentation corpus.

It is designed for retrieval and grounding, not for model weight training. Each knowledge object is a small, self-contained document with explicit metadata, source references, and retrieval cues.

## What is included
- `10_glossary/` – core business dimensions, classifications, and canonical glossary entries
- `20_channel_definitions/` – one file per multi-channel definition
- `30_attributes/` – qualitative, detailing, meeting, mailing, sample, and social-media attributes
- `40_measures/` – canonical metric definitions
- `50_examples/` – worked example separated from canonical definitions
- `01_governance/` – metadata schema, release checklist, benchmark seed, and recommended folder system
- `registry/` – flat catalog (`csv`) plus ingestion-ready `jsonl`

## Important limitations
This package is structurally ready for RAG ingestion, but **not yet business-approved**:
- owner is missing in the source workbook
- approval status is missing in the source workbook
- validity windows are missing in the source workbook
- source workbook wording is sometimes terse or inconsistent; light normalization was applied for readability
- some family definitions (for example ATC2-ATC4 and CHC2-CHC4) were normalized from a shared family description

## Release rule
Every file is therefore marked as `draft` until a business owner validates definition, applicability, and governance metadata.
