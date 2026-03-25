# Validation boundaries for promo internal insights

**Document ID:** IQVIA-PROMO-INSIGHT-validation-boundaries
**Entity type:** validation_note
**Status:** draft_candidate
**Source confidence:** medium
**Primary sources:** promo_oas_measure_inventory.csv; promo_oas_measure_migration_analysis.md; trusted_starschema_01 metadata

What can be treated as strong candidate knowledge now, and what still needs business validation.

## High-confidence layer
- Core base measures: Spending Total Euro, Product Details, Contact Number, Weighted Calls
- Monthly/quarterly analytical frames
- Prescription, specialty, contact, channel, and corporation dimensions

## Medium-confidence layer
- Derived ratio families where the numerator and denominator are obvious from captions and notes
- Weighted-calls analytical variants such as SOV and share-of-total

## Needs-validation layer
- Placeholder-driven dynamic families
- Exact previous-year comparison policy
- Index-family denominator policy
- Full enumerations of dynamic measure parameters

## RAG rule
Store uncertain logic explicitly as candidate semantics instead of turning it into falsely authoritative formulas. This preserves usefulness without creating silent hallucination risk.
