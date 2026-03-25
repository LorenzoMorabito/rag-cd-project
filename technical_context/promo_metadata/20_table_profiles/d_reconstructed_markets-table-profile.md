# d_reconstructed_markets — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_reconstructed_markets`
- table role: `dimension`
- primary key: `MARKET_ID`
- row count: `104`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `MARKET_ID`
- measures: none
- non-key attributes: `MARKET`, `MARKET_CODE`, `MARKET_DEFINITION`

## Inbound relationships
- used by `f_channel_dynamic_data.MARKET_ID` (validated_by_data_missing_metadata)

## Notes / cautions
- This dimension has a known duplication problem on `MARKET_ID` and needs deduplication before clean semantic use.

## Column inventory

|   position | column_name       | type_name   | nullable   | semantic_role       |
|-----------:|:------------------|:------------|:-----------|:--------------------|
|          0 | MARKET_ID         | LONG        | False      | business_key        |
|          1 | MARKET            | STRING      | True       | attribute           |
|          2 | MARKET_CODE       | STRING      | True       | attribute           |
|          3 | MARKET_DEFINITION | STRING      | True       | attribute           |
|          4 | _trusted_ts       | TIMESTAMP   | True       | technical_timestamp |