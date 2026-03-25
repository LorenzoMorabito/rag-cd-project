# d_time — Table Profile

## Role
Dimension table used to slice the promotional fact.

## Structural metadata
- full name: `dev_iqvia_catalog.trusted_starschema_01.d_time`
- table role: `dimension`
- primary key: `MONTH_ID`
- row count: `51`
- owner: `ccantamaglia@ext.menarini.com`
- data format: `DELTA`

## Semantic interpretation
Interpretation is inferred from table name and column structure because no descriptive comment was present.

## Column groups
- business keys: `MONTH_ID`, `QUARTER_ID`, `SEMESTER_ID`, `YEAR_ID`
- measures: none
- non-key attributes: `MONTH`, `QUARTER`, `SEMESTER`, `YEAR`

## Inbound relationships
- used by `f_channel_dynamic_data.MONTH_ID` (validated_by_data_missing_metadata)

## Column inventory

|   position | column_name   | type_name   | nullable   | semantic_role       |
|-----------:|:--------------|:------------|:-----------|:--------------------|
|          0 | MONTH_ID      | DATE        | False      | business_key        |
|          1 | MONTH         | STRING      | False      | attribute           |
|          2 | QUARTER_ID    | DATE        | True       | business_key        |
|          3 | QUARTER       | STRING      | False      | attribute           |
|          4 | SEMESTER_ID   | DATE        | True       | business_key        |
|          5 | SEMESTER      | STRING      | False      | attribute           |
|          6 | YEAR_ID       | DATE        | True       | business_key        |
|          7 | YEAR          | INT         | True       | attribute           |
|          8 | _trusted_ts   | TIMESTAMP   | True       | technical_timestamp |