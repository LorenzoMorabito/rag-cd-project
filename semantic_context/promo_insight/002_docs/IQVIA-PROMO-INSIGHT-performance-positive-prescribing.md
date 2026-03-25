# Performance and positive prescribing family

**Document ID:** IQVIA-PROMO-INSIGHT-performance-positive-prescribing
**Entity type:** measure_family_spec
**Status:** draft_candidate
**Source confidence:** high
**Primary sources:** promo_oas_measure_inventory.csv; promo_oas_measure_migration_analysis.md; trusted_starschema_01 metadata

Measures used to evaluate promotional execution quality and intention-to-prescribe outcomes.

## Included measures
- Contact Number
- Share of Contact Number
- Contact Number with intention to increase Rx
- % of Contact Number with intention to increase Rx
- Product Details with Positive Prescribing
- Contacts with Positive Prescribing
- Conversion rate on calls
- Conversion rate on contacts

## Base measures
- Contact Number
- Product Details
- Converted Contacts (candidate anchor where applicable)

## Observed logic
- Positive-prescribing and intention-to-increase-Rx variants behave like filtered versions of the base activity measures.
- Conversion measures behave like filtered numerator / base denominator * 100.

## Technical anchor
Fact anchors: `CONTACT_NUMBER`, `PRODUCT_DETAILS`, `CONVERTED_CONTACTS`, and `QUALITY_INDEX` in `f_channel_dynamic_data`. Strong candidate business filters come from prescription-state dimensions.

## Validation boundary
The exact operational definition of positive prescribing still needs business confirmation, especially where the source only implies the filter through captions and notes.
