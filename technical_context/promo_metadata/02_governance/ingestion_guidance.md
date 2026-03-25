# Ingestion Guidance

## Recommended use in RAG
- index markdown knowledge objects as the primary retrieval layer
- keep CSV registries as operational support assets
- tag objects by `entity_type`, `table_role`, `status`, `evidence_level`

## Retrieval guidance
- prioritize `technical_validated` documents when a user asks about joins, fact grain, PK/FK behavior, or readiness
- prioritize business glossary documents when a user asks for meaning or definition of measures/attributes
- use OAS appendix documents for migration and coverage questions, not for canonical definitions
