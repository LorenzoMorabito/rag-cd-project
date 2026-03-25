# d_atcs — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_atcs`
- table role: `dimension`
- primary key: `ATC4_ID`
- row count: `1353`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`
- source comment: Atcs Dimension Table - Source Table: ATC1, ATC2, ATC3, ATC3_PIE_GROUPS, ATC4 

## Semantic interpretation
The source metadata comment suggests: Atcs Dimension Table - Source Table: ATC1, ATC2, ATC3, ATC3_PIE_GROUPS, ATC4

## Column groups
- business keys: `ATC4_ID`
- measures: none
- non-key attributes: `ATC1_CODE`, `ATC1`, `ATC2_CODE`, `ATC2`, `ATC3_CODE`, `ATC3`, `ATC3_PIE_GROUP`, `ATC4_CODE`, `ATC4`

## Inbound relationships
- used by `f_channel_dynamic_data.ATC4_ID` (validated_by_data_missing_metadata)

## Column inventory

|   position | column_name    | type_name   | nullable   | semantic_role       |
|-----------:|:---------------|:------------|:-----------|:--------------------|
|          0 | ATC1_CODE      | STRING      | False      | attribute           |
|          1 | ATC1           | STRING      | False      | attribute           |
|          2 | ATC2_CODE      | STRING      | False      | attribute           |
|          3 | ATC2           | STRING      | False      | attribute           |
|          4 | ATC3_CODE      | STRING      | False      | attribute           |
|          5 | ATC3           | STRING      | False      | attribute           |
|          6 | ATC3_PIE_GROUP | STRING      | True       | attribute           |
|          7 | ATC4_ID        | LONG        | False      | business_key        |
|          8 | ATC4_CODE      | STRING      | False      | attribute           |
|          9 | ATC4           | STRING      | False      | attribute           |
|         10 | _trusted_ts    | TIMESTAMP   | True       | technical_timestamp |