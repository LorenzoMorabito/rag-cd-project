# d_contact_quality — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_contact_quality`
- table role: `dimension`
- primary key: `CONTACT_QUALITY_ID`
- row count: `25`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `CONTACT_QUALITY_ID`
- measures: none
- non-key attributes: `CONTACT_QUALITY`

## Inbound relationships
- used by `f_channel_dynamic_data.CONTACT_QUALITY_ID` (declared_metadata_fk)

## Column inventory

|   position | column_name        | type_name   | nullable   | semantic_role       |
|-----------:|:-------------------|:------------|:-----------|:--------------------|
|          0 | CONTACT_QUALITY_ID | LONG        | False      | business_key        |
|          1 | CONTACT_QUALITY    | STRING      | False      | attribute           |
|          2 | _trusted_ts        | TIMESTAMP   | True       | technical_timestamp |