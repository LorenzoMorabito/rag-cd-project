# d_specialty — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_specialty`
- table role: `dimension`
- primary key: `SPECIALTY_ID`
- row count: `129`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `SPECIALTY_ID`
- measures: none
- non-key attributes: `SPECIALTY`, `GP_SPECIALTY`, `OUR_SPECIALTY`

## Inbound relationships
- used by `f_channel_dynamic_data.SPECIALTY_ID` (declared_metadata_fk)

## Column inventory

|   position | column_name   | type_name   | nullable   | semantic_role       |
|-----------:|:--------------|:------------|:-----------|:--------------------|
|          0 | SPECIALTY_ID  | LONG        | False      | business_key        |
|          1 | SPECIALTY     | STRING      | False      | attribute           |
|          2 | GP_SPECIALTY  | STRING      | True       | attribute           |
|          3 | OUR_SPECIALTY | STRING      | True       | attribute           |
|          4 | _trusted_ts   | TIMESTAMP   | True       | technical_timestamp |