# d_countries — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_countries`
- table role: `dimension`
- primary key: `COUNTRY_ID`
- row count: `77`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `COUNTRY_ID`
- measures: none
- non-key attributes: `COUNTRY`, `ISO_COUNTRY_CODE`, `REGION`

## Inbound relationships
- used by `f_channel_dynamic_data.COUNTRY_ID` (validated_by_data_missing_metadata)

## Column inventory

|   position | column_name      | type_name   | nullable   | semantic_role       |
|-----------:|:-----------------|:------------|:-----------|:--------------------|
|          0 | COUNTRY_ID       | LONG        | False      | business_key        |
|          1 | COUNTRY          | STRING      | True       | attribute           |
|          2 | ISO_COUNTRY_CODE | STRING      | True       | attribute           |
|          3 | REGION           | STRING      | True       | attribute           |
|          4 | _trusted_ts      | TIMESTAMP   | True       | technical_timestamp |