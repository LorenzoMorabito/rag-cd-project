# Dimension usage patterns for promo measures

**Document ID:** IQVIA-PROMO-INSIGHT-dimension-usage-patterns
**Entity type:** dimension_usage_spec
**Status:** draft_candidate
**Source confidence:** medium_high
**Primary sources:** promo_oas_measure_inventory.csv; promo_oas_measure_migration_analysis.md; trusted_starschema_01 metadata

Observed analytical dimensions and their strongest candidate mappings into the promo semantic model.

## Most frequently observed dimensions
- Specialty / GP specialty
- Presentation position
- Contact type
- Contact quality
- Communication channel
- Corporation / manufacturer
- Prescription current / prescription future

## Design rule for RAG
Document not only which dimensions exist, but which measure families they are actually used with. This improves answerability when the user asks questions such as “weighted calls by specialty” or “spend by future prescribing”.

## Technical anchor
The strongest candidate dimensions all exist in `trusted_starschema_01`, so these usage patterns can be stored as first-class retrieval objects instead of being buried in dashboard-specific notes.
