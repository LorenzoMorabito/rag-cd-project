# Prescription segmentation spend family

**Document ID:** IQVIA-PROMO-INSIGHT-prescription-segmentation
**Entity type:** measure_family_spec
**Status:** draft_candidate
**Source confidence:** high
**Primary sources:** promo_oas_measure_inventory.csv; promo_oas_measure_migration_analysis.md; trusted_starschema_01 metadata

Spend measures segmented by current and future prescribing states.

## Included measures
- Prescription Spend Absolute
- Prescription Spend %

## Base measure
- Spending Total Euro

## Observed segmentation axes
- Prescription Current
- Prescription Future

## Calculation patterns
- Absolute spend by prescribing segment
- Segment spend / total monthly spend * 100

## Technical anchor
Fact anchor: `f_channel_dynamic_data.SPENDING_TOTAL_EUR`. Dimension anchors: `d_prescription_current.PRESCRIPTION_CURRENT` and `d_prescription_future.PRESCRIPTION_FUTURE`.
