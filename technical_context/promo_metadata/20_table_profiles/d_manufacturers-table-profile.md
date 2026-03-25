# d_manufacturers — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_manufacturers`
- table role: `dimension`
- primary key: `MANUFACTURER_ID`
- row count: `68307`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `MANUFACTURER_ID`
- measures: none
- non-key attributes: `MANUFACTURER`, `OUR_MANUFACTURER`, `MENARINI_FLAG`

## Inbound relationships
- used by `f_channel_dynamic_data.MANUFACTURER_ID` (declared_metadata_fk)

## Column inventory

|   position | column_name      | type_name   | nullable   | semantic_role       |
|-----------:|:-----------------|:------------|:-----------|:--------------------|
|          0 | MANUFACTURER_ID  | LONG        | False      | business_key        |
|          1 | MANUFACTURER     | STRING      | False      | attribute           |
|          2 | OUR_MANUFACTURER | STRING      | True       | attribute           |
|          3 | MENARINI_FLAG    | STRING      | True       | attribute           |
|          4 | _trusted_ts      | TIMESTAMP   | True       | technical_timestamp |