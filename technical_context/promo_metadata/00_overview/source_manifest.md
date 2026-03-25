# Source Manifest

| source_file                                                              | source_role                       | used_for                                   |
|:-------------------------------------------------------------------------|:----------------------------------|:-------------------------------------------|
| catalog.json                                                             | catalog_metadata                  | catalog owner and scope                    |
| schemas.json                                                             | schema_metadata                   | schema owner and scope                     |
| tables.csv                                                               | table_list                        | table inventory                            |
| tables_trusted_starschema_01.json                                        | table_metadata_export             | table profile generation                   |
| columns.csv                                                              | column_metadata_export            | column catalog and semantic role inference |
| constraints.csv                                                          | constraint_metadata_export        | PK/FK catalog                              |
| table_stats.csv                                                          | table_statistics                  | row counts and storage metadata            |
| inventory_report.md                                                      | inventory_summary                 | scope verification                         |
| dev_iqvia_catalog.trusted_starschema_01_technical_functional_analysis.md | technical_analysis                | schema interpretation                      |
| dev_iqvia_catalog.trusted_starschema_01_final_assessment.md              | validated_assessment              | quality/readiness register                 |
| promo_oas_measure_inventory.csv                                          | oas_promo_inventory               | coverage/migration appendix                |
| promo_oas_measure_migration_analysis.md                                  | oas_promo_analysis                | coverage/migration appendix                |
| iqvia_rag_corpus/registry/knowledge_objects.csv                          | existing_business_corpus_registry | candidate overlap generation               |