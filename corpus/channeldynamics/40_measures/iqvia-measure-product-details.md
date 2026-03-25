---
document_id: IQVIA-MEASURE-product-details
title: Product Details
domain: IQVIA ChannelDynamics
subdomain: Measures applying to DETAILING CHANNELS only
entity_type: measure_definition
owner: TO_BE_ASSIGNED
status: draft
version: '0.1'
valid_from: null
valid_to: null
region: multi-country
business_unit: ChannelDynamics
source_system: IQVIA CD Metrics Measures Description.xlsx
source_sheet: Metrics & Measures
source_row: 230
evidence_level: source_extract
audience: business,data,analytics,ai_engineering
language: en
tags:
- applying
- channels
- detailing
- details
- measure-definition
- measures
- metrics-measures
- only
- product
aliases: []
---

# Product Details

## Canonical definition
Each product/brand that is mentioned during a Rep CALL receives 1 product detail. (no matter if different forms/dosage are presented) If the product X 50MG and 100MG are presented within one call, this product will get 1 product detail Example: - If Product X is presented alone during the call, the product details will be equal to 1 - If 2 forms of the product X are presented during the call, each form of this product will get an half of the product details (= 0.5) - If 2 different products are presented during the call, the product details will be equal to 1 for each product - If 3 forms of the product X are presented during the call, each form will get the third part of the product details (= 0.33)

## Retrieval cues
- Suggested aliases: None explicitly identified
- Suggested tags: applying, channels, detailing, details, measure-definition, measures, metrics-measures, only, product

## Example user questions
- What does Product Details measure in IQVIA ChannelDynamics?
- How should Product Details be interpreted by business users?
- When should I use Product Details instead of another metric?

## Source note
Extracted from sheet 'Metrics & Measures', row 230.
This knowledge object is in draft status because the source workbook does not provide owner, approval state, validity window, or release governance.