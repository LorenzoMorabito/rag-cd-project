# d_details_duration — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_details_duration`
- table role: `dimension`
- primary key: `DETAILS_DURATION_ID`
- row count: `303`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `DETAILS_DURATION_ID`
- measures: none
- non-key attributes: `DETAILS_DURATION`, `DETAILS_DURATION_MIN`

## Inbound relationships
- used by `f_channel_dynamic_data.DETAILS_DURATION_ID` (declared_metadata_fk)

## Column inventory

|   position | column_name          | type_name   | nullable   | semantic_role       |
|-----------:|:---------------------|:------------|:-----------|:--------------------|
|          0 | DETAILS_DURATION_ID  | LONG        | False      | business_key        |
|          1 | DETAILS_DURATION     | STRING      | False      | attribute           |
|          2 | DETAILS_DURATION_MIN | INT         | False      | attribute           |
|          3 | _trusted_ts          | TIMESTAMP   | True       | technical_timestamp |