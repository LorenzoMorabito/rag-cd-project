# Promo internal measure families overview

**Document ID:** IQVIA-PROMO-INSIGHT-measure-families-overview
**Entity type:** insight_overview
**Status:** draft_candidate
**Source confidence:** medium_high
**Primary sources:** promo_oas_measure_inventory.csv; promo_oas_measure_migration_analysis.md; trusted_starschema_01 metadata

High-level map of the internal promotional measure families observed in the insight sources.

## Purpose
Summarize the internal promotional measure families that recur across the source insight set, without keeping the project-specific migration framing.

## Core base measures
- Spending Total Euro
- Product Details
- Contact Number
- Weighted Calls

## Derived KPI families
- Share-of-investment measures
- Share-of-voice measures
- Share-of-contact measures
- Positive prescribing measures
- Conversion rate measures
- Delta-vs-prior-year measures
- Growth-vs-prior-year measures
- Weighted-calls analytical measures such as SOV, Index, and share-of-total

## Technical anchor
The strongest technical anchor for these families is `f_channel_dynamic_data`, which already contains the core base measures and links to the relevant promo dimensions through foreign-key style business keys.

## Use in RAG
Treat this object as an orientation layer that helps the retrieval system route user questions to the right measure-family spec before drilling into formulas, time logic, or dimensions.
