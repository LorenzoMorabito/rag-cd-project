# d_comunication_channels — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_comunication_channels`
- table role: `dimension`
- primary key: `COMUNICATION_CHANNEL_ID`
- row count: `45`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `COMUNICATION_CHANNEL_ID`
- measures: none
- non-key attributes: `COMUNICATION_CHANNEL`

## Inbound relationships
- used by `f_channel_dynamic_data.COMUNICATION_CHANNEL_ID` (declared_metadata_fk)

## Column inventory

|   position | column_name             | type_name   | nullable   | semantic_role       |
|-----------:|:------------------------|:------------|:-----------|:--------------------|
|          0 | COMUNICATION_CHANNEL_ID | LONG        | False      | business_key        |
|          1 | COMUNICATION_CHANNEL    | STRING      | False      | attribute           |
|          2 | _trusted_ts             | TIMESTAMP   | True       | technical_timestamp |