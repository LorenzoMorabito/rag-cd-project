# Weighted calls analytical family

**Document ID:** IQVIA-PROMO-INSIGHT-weighted-calls-analytical-family
**Entity type:** measure_family_spec
**Status:** draft_candidate
**Source confidence:** medium_high
**Primary sources:** promo_oas_measure_inventory.csv; promo_oas_measure_migration_analysis.md; trusted_starschema_01 metadata

Analytical family built on weighted calls with share, growth, index, and share-of-total variants.

## Included measures
- Weighted Calls
- SOV% on Weighted Calls
- Growth % on Weighted Calls vs PY
- Index family
- % Corp on total / % Market on total

## Why it matters
This is not just one additive KPI. It behaves like a governed analytical family used for comparative and ranking-style views.

## Observed dimensions
- Corporation / promoter / manufacturer
- Specialty / GP specialty
- Contact type
- Contact quality
- Channel split

## Technical anchor
Primary fact anchor: `f_channel_dynamic_data.WEIGHTED_CALLS`. Candidate dimension anchors: `d_corporations`, `d_manufacturers`, `d_specialty`, `d_contact_types`, `d_contact_quality`, and `d_comunication_channels`.

## Validation boundary
Index-family denominator and market-total policies are still inferred patterns, not fully explicit formulas. Store them as candidate semantics until reviewed.
