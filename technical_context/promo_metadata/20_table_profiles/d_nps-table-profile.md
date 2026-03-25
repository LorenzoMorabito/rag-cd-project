# d_nps — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_nps`
- table role: `dimension`
- primary key: `NPS_SCALE_ID`
- row count: `60`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `NPS_SCALE_ID`
- measures: none
- non-key attributes: `NPS_SCALE`, `NPS_CATEGORY`

## Inbound relationships
- used by `f_channel_dynamic_data.NPS_SCALE_ID` (validated_by_data_missing_metadata)

## Column inventory

|   position | column_name   | type_name   | nullable   | semantic_role       |
|-----------:|:--------------|:------------|:-----------|:--------------------|
|          0 | NPS_SCALE_ID  | LONG        | False      | business_key        |
|          1 | NPS_SCALE     | STRING      | False      | attribute           |
|          2 | NPS_CATEGORY  | STRING      | False      | attribute           |
|          3 | _trusted_ts   | TIMESTAMP   | True       | technical_timestamp |