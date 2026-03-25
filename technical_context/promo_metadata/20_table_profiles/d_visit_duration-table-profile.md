# d_visit_duration — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_visit_duration`
- table role: `dimension`
- primary key: `VISIT_DURATION_ID`
- row count: `995`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `VISIT_DURATION_ID`
- measures: none
- non-key attributes: `VISIT_DURATION`, `VISIT_DURATION_MIN`

## Inbound relationships
- used by `f_channel_dynamic_data.VISIT_DURATION_ID` (declared_metadata_fk)

## Column inventory

|   position | column_name        | type_name   | nullable   | semantic_role       |
|-----------:|:-------------------|:------------|:-----------|:--------------------|
|          0 | VISIT_DURATION_ID  | LONG        | False      | business_key        |
|          1 | VISIT_DURATION     | STRING      | False      | attribute           |
|          2 | VISIT_DURATION_MIN | INT         | False      | attribute           |
|          3 | _trusted_ts        | TIMESTAMP   | True       | technical_timestamp |