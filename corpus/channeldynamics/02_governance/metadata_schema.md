# Minimum metadata schema

Use these fields on every knowledge object before release:

| Field | Required | Purpose |
|---|---|---|
| document_id | yes | stable unique identifier |
| title | yes | canonical interrogable title |
| domain | yes | main knowledge domain |
| subdomain | yes | narrower information area |
| entity_type | yes | glossary_entry, attribute_definition, channel_definition, measure_definition, faq, example |
| owner | yes | content owner |
| status | yes | draft, approved, deprecated, ambiguous, archived |
| version | yes | logical content version |
| valid_from | recommended | start of validity |
| valid_to | recommended | end of validity |
| region | yes | country/region/business scope |
| business_unit | yes | organizational scope |
| source_system | yes | workbook, repository, or source platform |
| source_sheet | yes for spreadsheets | sheet-level provenance |
| source_row | yes for spreadsheets | row-level provenance |
| evidence_level | yes | source_extract, approved_policy, derived_note, etc. |
| audience | yes | intended users |
| language | yes | main language |
| tags | yes | retrieval cues |
| aliases | recommended | synonyms used by users |

## Default values used in this package
- `owner`: TO_BE_ASSIGNED
- `status`: draft
- `version`: 0.1
- `region`: multi-country
- `business_unit`: ChannelDynamics
- `evidence_level`: source_extract
