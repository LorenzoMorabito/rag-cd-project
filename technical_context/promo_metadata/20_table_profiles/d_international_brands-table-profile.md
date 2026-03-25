# d_international_brands — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_international_brands`
- table role: `dimension`
- primary key: `INTERNATIONAL_BRAND_ID`
- row count: `620665`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`
- source comment: Internaional Brands Dimension Table - Source Tables: INTERNATIONAL_BRANDS 

## Semantic interpretation
The source metadata comment suggests: Internaional Brands Dimension Table - Source Tables: INTERNATIONAL_BRANDS

## Column groups
- business keys: `INTERNATIONAL_BRAND_ID`
- measures: none
- non-key attributes: `INTERNATIONAL_BRAND`

## Inbound relationships
- used by `f_channel_dynamic_data.INTERNATIONAL_BRAND_ID` (declared_metadata_fk)

## Column inventory

|   position | column_name            | type_name   | nullable   | semantic_role       |
|-----------:|:-----------------------|:------------|:-----------|:--------------------|
|          0 | INTERNATIONAL_BRAND_ID | LONG        | False      | business_key        |
|          1 | INTERNATIONAL_BRAND    | STRING      | False      | attribute           |
|          2 | _trusted_ts            | TIMESTAMP   | True       | technical_timestamp |