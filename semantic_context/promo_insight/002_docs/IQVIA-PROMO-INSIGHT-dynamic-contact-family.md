# Dynamic contact metric family

**Document ID:** IQVIA-PROMO-INSIGHT-dynamic-contact-family
**Entity type:** measure_family_spec
**Status:** draft_candidate
**Source confidence:** medium
**Primary sources:** promo_oas_measure_inventory.csv; promo_oas_measure_migration_analysis.md; trusted_starschema_01 metadata

Pattern for a parameterized contact-metric family with absolute, share, delta, and delta-percent variants.

## Observed family members
- Selected Contact Metric
- % of Selected Contact Metric
- Delta vs PY - Selected Contact Metric
- Delta% vs PY - Selected Contact Metric

## Critical caveat
The source exposes a placeholder-style expression such as `@{var_mea}{Contact Number}`. That is enough to infer a dynamic family, but not enough to enumerate every supported placeholder value with certainty.

## Typical dimensions
- Specialty
- GP/Specialty
- Presentation position
- Contact type
- Contact channel
- Corporation

## Technical anchor
Likely fact anchors are `CONTACT_NUMBER` and `WEIGHTED_CALLS` in `f_channel_dynamic_data`; candidate dimension anchors are `d_specialty`, `d_presentation_position`, `d_contact_types`, `d_comunication_channels`, and `d_corporations`.

## RAG treatment
Represent this as a family with parameters, not as a single fixed measure. Mark formula explicitness as `needs_validation` until the placeholder value set and exact denominator policy are confirmed.
