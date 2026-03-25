# trusted_starschema_01 — Schema Overview

## Positioning
This schema is the **promotional / channel-dynamics** schema of `dev_iqvia_catalog`.

## Core shape
- 1 fact table: `f_channel_dynamic_data`
- 29 dimension tables
- monthly-native time model via `MONTH_ID` and `d_time`
- central measures stored in the fact:
  - CONTACT_NUMBER
  - MENTIONS
  - NON_WEIGHTED_CALLS
  - PRODUCT_DETAILS
  - QUALITY_INDEX
  - SPENDING_TOTAL_EUR
  - WEIGHTED_CALLS
  - CONVERTED_CONTACTS

## Semantic interpretation
This schema is suited to promotional performance analysis across:
- product / brand / molecule / ATC
- company and sponsorship roles
- communication channel and contact setup
- specialty and market slices
- response / prescribing / NPS style attributes
- spend, contacts, details, calls, quality, and conversion signals

## Readiness posture
- functionally strong
- technically strong after `d_reconstructed_markets` deduplication
- good candidate for direct semantic-model use and for a RAG technical layer
