# IQVIA Promo Technical Metadata Corpus (RAG-ready)

This package converts `dev_iqvia_catalog.trusted_starschema_01` into a RAG-ready technical corpus for the **promotional / channel-dynamics** domain.

## What this package is
- technical-semantic layer for promo
- table profiles for the Databricks star schema
- relationship catalog with declared and validated-but-missing FK metadata
- quality/readiness register
- appendix for OAS promo coverage and migration gaps

## What this package is not
- not the final business-approved glossary
- not the quality-evidence raw SQL layer
- not a full canonical promo metric universe on its own

## Intended merge target
This package is designed to be merged with:
1. the existing business glossary corpus created from `IQVIA CD Metrics  Measures Description.xlsx`
2. the future quality-evidence layer

## Core schema
- catalog: `dev_iqvia_catalog`
- schema: `trusted_starschema_01`
- role: promotional / channel-dynamics star schema
- fact table: `f_channel_dynamic_data`
- dimension tables: 29
