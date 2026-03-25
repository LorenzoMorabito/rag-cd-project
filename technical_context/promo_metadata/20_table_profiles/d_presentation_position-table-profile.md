# d_presentation_position — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_presentation_position`
- table role: `dimension`
- primary key: `PRESENTATION_POSITION_ID`
- row count: `200`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `PRESENTATION_POSITION_ID`
- measures: none
- non-key attributes: `PRESENTATION_POSITION`, `ORDER_BY`

## Inbound relationships
- used by `f_channel_dynamic_data.PRESENTATION_POSITION_ID` (declared_metadata_fk)

## Column inventory

|   position | column_name              | type_name   | nullable   | semantic_role       |
|-----------:|:-------------------------|:------------|:-----------|:--------------------|
|          0 | PRESENTATION_POSITION_ID | LONG        | False      | business_key        |
|          1 | PRESENTATION_POSITION    | STRING      | False      | attribute           |
|          2 | ORDER_BY                 | INT         | True       | attribute           |
|          3 | _trusted_ts              | TIMESTAMP   | True       | technical_timestamp |