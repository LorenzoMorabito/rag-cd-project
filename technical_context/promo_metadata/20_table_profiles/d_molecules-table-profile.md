# d_molecules — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_molecules`
- table role: `dimension`
- primary key: `MOLECULE_ID`
- row count: `187470`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `MOLECULE_ID`
- measures: none
- non-key attributes: `MOLECULE`, `CORPORATE_MOLECULE`

## Inbound relationships
- used by `f_channel_dynamic_data.MOLECULE_ID` (declared_metadata_fk)

## Column inventory

|   position | column_name        | type_name   | nullable   | semantic_role       |
|-----------:|:-------------------|:------------|:-----------|:--------------------|
|          0 | MOLECULE_ID        | LONG        | False      | business_key        |
|          1 | MOLECULE           | STRING      | False      | attribute           |
|          2 | CORPORATE_MOLECULE | STRING      | True       | attribute           |
|          3 | _trusted_ts        | TIMESTAMP   | True       | technical_timestamp |