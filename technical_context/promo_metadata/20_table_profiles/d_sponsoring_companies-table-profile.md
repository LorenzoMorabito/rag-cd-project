# d_sponsoring_companies — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_sponsoring_companies`
- table role: `dimension`
- primary key: `SPONSORING_COMPANY_ID`
- row count: `68305`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `SPONSORING_COMPANY_ID`
- measures: none
- non-key attributes: `SPONSORING_COMPANY`, `OUR_REPRESENTING_COMPANY`, `MENARINI_FLAG`

## Inbound relationships
- used by `f_channel_dynamic_data.SPONSORING_COMPANY_ID` (validated_by_data_missing_metadata)

## Column inventory

|   position | column_name              | type_name   | nullable   | semantic_role       |
|-----------:|:-------------------------|:------------|:-----------|:--------------------|
|          0 | SPONSORING_COMPANY_ID    | LONG        | False      | business_key        |
|          1 | SPONSORING_COMPANY       | STRING      | False      | attribute           |
|          2 | OUR_REPRESENTING_COMPANY | STRING      | False      | attribute           |
|          3 | MENARINI_FLAG            | BOOLEAN     | True       | attribute           |
|          4 | _trusted_ts              | TIMESTAMP   | True       | technical_timestamp |