# Recommended folder system for production RAG corpus

## Production layout
- `00_governance/`
  - metadata schema
  - release checklist
  - benchmark questions
  - change log
- `10_glossary/`
  - product taxonomy
  - brand and manufacturer definitions
  - channel and specialty dictionaries
- `20_channel_definitions/`
  - one canonical file per channel
- `30_attributes/`
  - qualitative attributes
  - channel-specific descriptors
  - controlled-value dictionaries
- `40_measures/`
  - one canonical file per measure
- `50_examples/`
  - worked examples
  - edge cases
- `registry/`
  - ingestion catalog
  - alias map
  - duplicate log

## Why this layout works
- separates canonical definitions from examples
- separates measures from dimensions and attributes
- makes chunking easier because each file is small and semantically coherent
- supports metadata filtering by entity type, source sheet, and business area
