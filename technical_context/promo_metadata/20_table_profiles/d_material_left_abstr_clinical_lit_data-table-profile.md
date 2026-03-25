# d_material_left_abstr_clinical_lit_data — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_material_left_abstr_clinical_lit_data`
- table role: `dimension`
- primary key: `MATERIAL_LEFT_ABSTR_CLINICAL_LIT_DATA_ID`
- row count: `15`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `MATERIAL_LEFT_ABSTR_CLINICAL_LIT_DATA_ID`
- measures: none
- non-key attributes: `MATERIAL_LEFT_ABSTR_CLINICAL_LIT_DATA`

## Inbound relationships
- used by `f_channel_dynamic_data.MATERIAL_LEFT_ABSTR_CLINICAL_LIT_DATA_ID` (declared_metadata_fk)

## Column inventory

|   position | column_name                              | type_name   | nullable   | semantic_role       |
|-----------:|:-----------------------------------------|:------------|:-----------|:--------------------|
|          0 | MATERIAL_LEFT_ABSTR_CLINICAL_LIT_DATA_ID | LONG        | False      | business_key        |
|          1 | MATERIAL_LEFT_ABSTR_CLINICAL_LIT_DATA    | STRING      | False      | attribute           |
|          2 | _trusted_ts                              | TIMESTAMP   | True       | technical_timestamp |