# d_clinical_trial_types — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_clinical_trial_types`
- table role: `dimension`
- primary key: `CLINICAL_TRIAL_TYPE_ID`
- row count: `45`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `CLINICAL_TRIAL_TYPE_ID`
- measures: none
- non-key attributes: `CLINICAL_TRIAL_TYPE`

## Inbound relationships
- used by `f_channel_dynamic_data.CLINICAL_TRIAL_TYPE_ID` (declared_metadata_fk)

## Column inventory

|   position | column_name            | type_name   | nullable   | semantic_role       |
|-----------:|:-----------------------|:------------|:-----------|:--------------------|
|          0 | CLINICAL_TRIAL_TYPE_ID | LONG        | False      | business_key        |
|          1 | CLINICAL_TRIAL_TYPE    | STRING      | False      | attribute           |
|          2 | _trusted_ts            | TIMESTAMP   | True       | technical_timestamp |