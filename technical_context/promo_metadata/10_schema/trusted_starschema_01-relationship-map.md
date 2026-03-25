# trusted_starschema_01 — Relationship Map
## Declared joins from fact
- `f_channel_dynamic_data.CLINICAL_TRIAL_TYPE_ID -> d_clinical_trial_types.CLINICAL_TRIAL_TYPE_ID`
- `f_channel_dynamic_data.COMUNICATION_CHANNEL_ID -> d_comunication_channels.COMUNICATION_CHANNEL_ID`
- `f_channel_dynamic_data.CONTACT_QUALITY_ID -> d_contact_quality.CONTACT_QUALITY_ID`
- `f_channel_dynamic_data.CONTACT_TYPE_ID -> d_contact_types.CONTACT_TYPE_ID`
- `f_channel_dynamic_data.CORPORATION_ID -> d_corporations.CORPORATION_ID`
- `f_channel_dynamic_data.DETAILS_DURATION_ID -> d_details_duration.DETAILS_DURATION_ID`
- `f_channel_dynamic_data.INTERNATIONAL_BRAND_ID -> d_international_brands.INTERNATIONAL_BRAND_ID`
- `f_channel_dynamic_data.LOCAL_BRAND_ID -> d_local_brands.LOCAL_BRAND_ID`
- `f_channel_dynamic_data.MANUFACTURER_ID -> d_manufacturers.MANUFACTURER_ID`
- `f_channel_dynamic_data.MATERIAL_LEFT_ABSTR_CLINICAL_LIT_DATA_ID -> d_material_left_abstr_clinical_lit_data.MATERIAL_LEFT_ABSTR_CLINICAL_LIT_DATA_ID`
- `f_channel_dynamic_data.MATERIAL_LEFT_OTHER_ID -> d_material_left_other.MATERIAL_LEFT_OTHER_ID`
- `f_channel_dynamic_data.MATERIAL_LEFT_PATIENT_EDUCATIONAL_LIT_ID -> d_material_left_patient_educational_lit.MATERIAL_LEFT_PATIENT_EDUCATIONAL_LIT_ID`
- `f_channel_dynamic_data.MATERIAL_LEFT_PROMOTIONAL_PRODUCT_LIT_ID -> d_material_left_promotional_product_lit.MATERIAL_LEFT_PROMOTIONAL_PRODUCT_LIT_ID`
- `f_channel_dynamic_data.MATERIAL_LEFT_SAMPLE_ID -> d_material_left_samples.MATERIAL_LEFT_SAMPLE_ID`
- `f_channel_dynamic_data.MEETING_TYPE_ID -> d_meeting_types.MEETING_TYPE_ID`
- `f_channel_dynamic_data.MOLECULE_ID -> d_molecules.MOLECULE_ID`
- `f_channel_dynamic_data.PRESCRIPTION_CURRENT_ID -> d_prescription_current.PRESCRIPTION_CURRENT_ID`
- `f_channel_dynamic_data.PRESCRIPTION_FUTURE_ID -> d_prescription_future.PRESCRIPTION_FUTURE_ID`
- `f_channel_dynamic_data.PRESENTATION_POSITION_ID -> d_presentation_position.PRESENTATION_POSITION_ID`
- `f_channel_dynamic_data.PRODUCT_PRESENTED_ID -> d_products_presented.PRODUCT_PRESENTED_ID`
- `f_channel_dynamic_data.REPRESENTING_COMPANY_ID -> d_representing_company.REPRESENTING_COMPANY_ID`
- `f_channel_dynamic_data.SPECIALTY_ID -> d_specialty.SPECIALTY_ID`
- `f_channel_dynamic_data.VISIT_DURATION_ID -> d_visit_duration.VISIT_DURATION_ID`

## Validated joins missing formal FK metadata
- `f_channel_dynamic_data.ATC4_ID -> d_atcs.ATC4_ID` — validated by data, missing metadata FK
- `f_channel_dynamic_data.COUNTRY_ID -> d_countries.COUNTRY_ID` — validated by data, missing metadata FK
- `f_channel_dynamic_data.MARKET_ID -> d_reconstructed_markets.MARKET_ID` — validated by data, missing metadata FK
- `f_channel_dynamic_data.MONTH_ID -> d_time.MONTH_ID` — validated by data, missing metadata FK
- `f_channel_dynamic_data.NPS_SCALE_ID -> d_nps.NPS_SCALE_ID` — validated by data, missing metadata FK
- `f_channel_dynamic_data.SPONSORING_COMPANY_ID -> d_sponsoring_companies.SPONSORING_COMPANY_ID` — validated by data, missing metadata FK
