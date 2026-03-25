# Promo analytical time behavior policy

**Document ID:** IQVIA-PROMO-INSIGHT-time-behavior-policy
**Entity type:** time_behavior_spec
**Status:** draft_candidate
**Source confidence:** medium_high
**Primary sources:** promo_oas_measure_inventory.csv; promo_oas_measure_migration_analysis.md; trusted_starschema_01 metadata

Observed time frames and comparison patterns used by internal promotional measures.

## Observed frames
- MON: direct month view
- MQTR: rolling 3-month moving quarter
- QTR: direct quarter view
- vs PY: previous-year comparator family

## Interpretation
These frames behave like part of the measure semantics, not only like report filters. The same measure family can appear as absolute, ratio, delta, and delta-percent depending on the chosen frame.

## Technical anchor
The natural technical anchor is `d_time` with `MONTH_ID`, `MONTH`, `QUARTER_ID`, `QUARTER`, and `YEAR_ID`. The promo fact is month-native, so MON and rolling-quarter semantics can be modeled on top of that monthly grain.

## Validation boundary
The exact null-handling and previous-year alignment policy is still not explicit for every derived family. Store those patterns as candidate semantics until the business team validates denominator and comparator rules.
