# f_channel_dynamic_data — Table Profile

## Role
Central promo fact table holding measures and slice keys.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.f_channel_dynamic_data`
- table role: `fact`
- primary key: `F_CDD_ID`
- row count: `10817381`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `F_CDD_ID`, `ATC4_ID`, `CONTACT_TYPE_ID`, `CONTACT_QUALITY_ID`, `SPECIALTY_ID`, `CLINICAL_TRIAL_TYPE_ID`, `MANUFACTURER_ID`, `MOLECULE_ID`, `MATERIAL_LEFT_SAMPLE_ID`, `REPRESENTING_COMPANY_ID`, `COMUNICATION_CHANNEL_ID`, `PRESENTATION_POSITION_ID`, `DETAILS_DURATION_ID`, `VISIT_DURATION_ID`, `SPONSORING_COMPANY_ID`, `MEETING_TYPE_ID`, `MATERIAL_LEFT_PROMOTIONAL_PRODUCT_LIT_ID`, `MATERIAL_LEFT_PATIENT_EDUCATIONAL_LIT_ID`, `MATERIAL_LEFT_OTHER_ID`, `INTERNATIONAL_BRAND_ID`, `LOCAL_BRAND_ID`, `CORPORATION_ID`, `COUNTRY_ID`, `NPS_SCALE_ID`, `PRODUCT_PRESENTED_ID`, `PRESCRIPTION_CURRENT_ID`, `MATERIAL_LEFT_ABSTR_CLINICAL_LIT_DATA_ID`, `PRESCRIPTION_FUTURE_ID`, `MONTH_ID`, `MARKET_ID`
- measures: `CONTACT_NUMBER`, `MENTIONS`, `NON_WEIGHTED_CALLS`, `PRODUCT_DETAILS`, `QUALITY_INDEX`, `SPENDING_TOTAL_EUR`, `WEIGHTED_CALLS`, `CONVERTED_CONTACTS`
- non-key attributes: none

## Outbound relationships
- `ATC4_ID -> d_atcs.ATC4_ID` (validated_by_data_missing_metadata)
- `CLINICAL_TRIAL_TYPE_ID -> d_clinical_trial_types.CLINICAL_TRIAL_TYPE_ID` (declared_metadata_fk)
- `COMUNICATION_CHANNEL_ID -> d_comunication_channels.COMUNICATION_CHANNEL_ID` (declared_metadata_fk)
- `CONTACT_QUALITY_ID -> d_contact_quality.CONTACT_QUALITY_ID` (declared_metadata_fk)
- `CONTACT_TYPE_ID -> d_contact_types.CONTACT_TYPE_ID` (declared_metadata_fk)
- `CORPORATION_ID -> d_corporations.CORPORATION_ID` (declared_metadata_fk)
- `COUNTRY_ID -> d_countries.COUNTRY_ID` (validated_by_data_missing_metadata)
- `DETAILS_DURATION_ID -> d_details_duration.DETAILS_DURATION_ID` (declared_metadata_fk)
- `INTERNATIONAL_BRAND_ID -> d_international_brands.INTERNATIONAL_BRAND_ID` (declared_metadata_fk)
- `LOCAL_BRAND_ID -> d_local_brands.LOCAL_BRAND_ID` (declared_metadata_fk)
- `MANUFACTURER_ID -> d_manufacturers.MANUFACTURER_ID` (declared_metadata_fk)
- `MARKET_ID -> d_reconstructed_markets.MARKET_ID` (validated_by_data_missing_metadata)
- `MATERIAL_LEFT_ABSTR_CLINICAL_LIT_DATA_ID -> d_material_left_abstr_clinical_lit_data.MATERIAL_LEFT_ABSTR_CLINICAL_LIT_DATA_ID` (declared_metadata_fk)
- `MATERIAL_LEFT_OTHER_ID -> d_material_left_other.MATERIAL_LEFT_OTHER_ID` (declared_metadata_fk)
- `MATERIAL_LEFT_PATIENT_EDUCATIONAL_LIT_ID -> d_material_left_patient_educational_lit.MATERIAL_LEFT_PATIENT_EDUCATIONAL_LIT_ID` (declared_metadata_fk)
- `MATERIAL_LEFT_PROMOTIONAL_PRODUCT_LIT_ID -> d_material_left_promotional_product_lit.MATERIAL_LEFT_PROMOTIONAL_PRODUCT_LIT_ID` (declared_metadata_fk)
- `MATERIAL_LEFT_SAMPLE_ID -> d_material_left_samples.MATERIAL_LEFT_SAMPLE_ID` (declared_metadata_fk)
- `MEETING_TYPE_ID -> d_meeting_types.MEETING_TYPE_ID` (declared_metadata_fk)
- `MOLECULE_ID -> d_molecules.MOLECULE_ID` (declared_metadata_fk)
- `MONTH_ID -> d_time.MONTH_ID` (validated_by_data_missing_metadata)
- `NPS_SCALE_ID -> d_nps.NPS_SCALE_ID` (validated_by_data_missing_metadata)
- `PRESCRIPTION_CURRENT_ID -> d_prescription_current.PRESCRIPTION_CURRENT_ID` (declared_metadata_fk)
- `PRESCRIPTION_FUTURE_ID -> d_prescription_future.PRESCRIPTION_FUTURE_ID` (declared_metadata_fk)
- `PRESENTATION_POSITION_ID -> d_presentation_position.PRESENTATION_POSITION_ID` (declared_metadata_fk)
- `PRODUCT_PRESENTED_ID -> d_products_presented.PRODUCT_PRESENTED_ID` (declared_metadata_fk)
- `REPRESENTING_COMPANY_ID -> d_representing_company.REPRESENTING_COMPANY_ID` (declared_metadata_fk)
- `SPECIALTY_ID -> d_specialty.SPECIALTY_ID` (declared_metadata_fk)
- `SPONSORING_COMPANY_ID -> d_sponsoring_companies.SPONSORING_COMPANY_ID` (validated_by_data_missing_metadata)
- `VISIT_DURATION_ID -> d_visit_duration.VISIT_DURATION_ID` (declared_metadata_fk)

## Notes / cautions
- Keep `MONTH_ID` as native time key.
- Treat `CONVERTED_CONTACTS` as conditionally nullable.
- Use validated joins for missing FK metadata columns such as `MONTH_ID`, `COUNTRY_ID`, `ATC4_ID`, `MARKET_ID`, `NPS_SCALE_ID`, `SPONSORING_COMPANY_ID`.

## Column inventory

|   position | column_name                              | type_name   | nullable   | semantic_role       |
|-----------:|:-----------------------------------------|:------------|:-----------|:--------------------|
|          0 | F_CDD_ID                                 | STRING      | False      | business_key        |
|          1 | ATC4_ID                                  | LONG        | True       | business_key        |
|          2 | CONTACT_TYPE_ID                          | LONG        | True       | business_key        |
|          3 | CONTACT_QUALITY_ID                       | LONG        | True       | business_key        |
|          4 | SPECIALTY_ID                             | LONG        | True       | business_key        |
|          5 | CLINICAL_TRIAL_TYPE_ID                   | LONG        | True       | business_key        |
|          6 | MANUFACTURER_ID                          | LONG        | True       | business_key        |
|          7 | MOLECULE_ID                              | LONG        | True       | business_key        |
|          8 | MATERIAL_LEFT_SAMPLE_ID                  | LONG        | True       | business_key        |
|          9 | REPRESENTING_COMPANY_ID                  | LONG        | True       | business_key        |
|         10 | COMUNICATION_CHANNEL_ID                  | LONG        | True       | business_key        |
|         11 | PRESENTATION_POSITION_ID                 | LONG        | True       | business_key        |
|         12 | DETAILS_DURATION_ID                      | LONG        | True       | business_key        |
|         13 | VISIT_DURATION_ID                        | LONG        | True       | business_key        |
|         14 | SPONSORING_COMPANY_ID                    | LONG        | True       | business_key        |
|         15 | MEETING_TYPE_ID                          | LONG        | True       | business_key        |
|         16 | MATERIAL_LEFT_PROMOTIONAL_PRODUCT_LIT_ID | LONG        | True       | business_key        |
|         17 | MATERIAL_LEFT_PATIENT_EDUCATIONAL_LIT_ID | LONG        | True       | business_key        |
|         18 | MATERIAL_LEFT_OTHER_ID                   | LONG        | True       | business_key        |
|         19 | INTERNATIONAL_BRAND_ID                   | LONG        | True       | business_key        |
|         20 | LOCAL_BRAND_ID                           | LONG        | True       | business_key        |
|         21 | CORPORATION_ID                           | LONG        | True       | business_key        |
|         22 | COUNTRY_ID                               | LONG        | True       | business_key        |
|         23 | NPS_SCALE_ID                             | LONG        | True       | business_key        |
|         24 | PRODUCT_PRESENTED_ID                     | LONG        | True       | business_key        |
|         25 | PRESCRIPTION_CURRENT_ID                  | LONG        | True       | business_key        |
|         26 | MATERIAL_LEFT_ABSTR_CLINICAL_LIT_DATA_ID | LONG        | True       | business_key        |
|         27 | PRESCRIPTION_FUTURE_ID                   | LONG        | True       | business_key        |
|         28 | CONTACT_NUMBER                           | DECIMAL     | True       | measure             |
|         29 | MENTIONS                                 | DECIMAL     | True       | measure             |
|         30 | NON_WEIGHTED_CALLS                       | DECIMAL     | True       | measure             |
|         31 | PRODUCT_DETAILS                          | DECIMAL     | True       | measure             |
|         32 | QUALITY_INDEX                            | DECIMAL     | True       | measure             |
|         33 | SPENDING_TOTAL_EUR                       | DECIMAL     | True       | measure             |
|         34 | WEIGHTED_CALLS                           | DECIMAL     | True       | measure             |
|         35 | CONVERTED_CONTACTS                       | DECIMAL     | True       | measure             |
|         36 | MONTH_ID                                 | DATE        | True       | business_key        |
|         37 | MARKET_ID                                | LONG        | True       | business_key        |
|         38 | _trusted_ts                              | TIMESTAMP   | True       | technical_timestamp |