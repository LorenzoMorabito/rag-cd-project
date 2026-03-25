# Metadata Schema For Knowledge Objects

Each knowledge object in this package uses the following minimal fields in the registry:
- document_id
- title
- domain
- subdomain
- entity_type
- owner
- status
- version
- evidence_level
- audience
- language
- tags
- aliases
- filepath

## Status policy
- `draft`: generated from metadata and analysis; not yet business-approved
- `technical_validated`: directly supported by final SQL-based assessment
- `candidate`: useful for merge or migration analysis but not yet canonical
