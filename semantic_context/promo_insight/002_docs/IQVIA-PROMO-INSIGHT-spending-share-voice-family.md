# Spending and share-of-voice family

**Document ID:** IQVIA-PROMO-INSIGHT-spending-share-voice-family
**Entity type:** measure_family_spec
**Status:** draft_candidate
**Source confidence:** high
**Primary sources:** promo_oas_measure_inventory.csv; promo_oas_measure_migration_analysis.md; trusted_starschema_01 metadata

Base and derived measures used to analyze promotional pressure, spend distribution, and share of voice.

## Included measures
- Investments
- % Share of Investments
- Product Details
- % Share of Voice
- Interaction/channel-split variants for spend and SOV

## Base measures
- Spending Total Euro
- Product Details

## Observed calculation patterns
- Share of Investments = spend / total spend in period * 100
- Share of Voice = product details / total product details in period * 100
- Interaction variants split the same logic by communication-channel grouping such as digital vs traditional

## Typical dimensions
- Communication channel / interaction group
- Product and brand slices
- Market slices where available

## Technical anchor
Primary fact anchor: `f_channel_dynamic_data.SPENDING_TOTAL_EUR` and `f_channel_dynamic_data.PRODUCT_DETAILS`. Candidate channel dimension: `d_comunication_channels.COMUNICATION_CHANNEL`.
