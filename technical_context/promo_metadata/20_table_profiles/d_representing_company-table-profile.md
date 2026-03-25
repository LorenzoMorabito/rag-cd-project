# d_representing_company — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_representing_company`
- table role: `dimension`
- primary key: `REPRESENTING_COMPANY_ID`
- row count: `68306`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `REPRESENTING_COMPANY_ID`
- measures: none
- non-key attributes: `REPRESENTING_COMPANY`, `OUR_REPRESENTING_COMPANY`, `MENARINI_FLAG`

## Inbound relationships
- used by `f_channel_dynamic_data.REPRESENTING_COMPANY_ID` (declared_metadata_fk)

## Column inventory

|   position | column_name              | type_name   | nullable   | semantic_role       |
|-----------:|:-------------------------|:------------|:-----------|:--------------------|
|          0 | REPRESENTING_COMPANY_ID  | LONG        | False      | business_key        |
|          1 | REPRESENTING_COMPANY     | STRING      | False      | attribute           |
|          2 | OUR_REPRESENTING_COMPANY | STRING      | True       | attribute           |
|          3 | MENARINI_FLAG            | STRING      | True       | attribute           |
|          4 | _trusted_ts              | TIMESTAMP   | True       | technical_timestamp |