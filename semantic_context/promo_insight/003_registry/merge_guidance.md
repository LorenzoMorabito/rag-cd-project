# Merge guidance

This package is designed as a semantic-insight layer for promo internal measures.

Recommended merge target:
- join with the promo technical package (`iqvia_rag_promo_metadata`) on measure family bucket, fact table, and candidate dimensions
- keep this package separate from business-canonical documentation until business validation promotes candidate formulas to approved formulas
- use `measure_semantics_catalog.csv` for retrieval enrichment and `dimension_usage_catalog.csv` for dimension routing hints

Do not import the project-specific migration framing into the final user-facing semantic layer.
Use these artifacts as internal measure semantics and analytical-pattern knowledge.
