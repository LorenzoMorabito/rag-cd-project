# d_products_presented — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_products_presented`
- table role: `dimension`
- primary key: `PRODUCT_PRESENTED_ID`
- row count: `165`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `PRODUCT_PRESENTED_ID`
- measures: none
- non-key attributes: `PRODUCT_PRESENTED`, `ORDER_BY`

## Inbound relationships
- used by `f_channel_dynamic_data.PRODUCT_PRESENTED_ID` (declared_metadata_fk)

## Column inventory

|   position | column_name          | type_name   | nullable   | semantic_role       |
|-----------:|:---------------------|:------------|:-----------|:--------------------|
|          0 | PRODUCT_PRESENTED_ID | LONG        | False      | business_key        |
|          1 | PRODUCT_PRESENTED    | STRING      | False      | attribute           |
|          2 | ORDER_BY             | INT         | True       | attribute           |
|          3 | _trusted_ts          | TIMESTAMP   | True       | technical_timestamp |